# alx-files_manager
"remove package-lock.json , node-modules"
"install package.json"

npm install
______________________________________
"install mongo db"

curl -fsSL https://pgp.mongodb.com/server-6.0.asc | sudo gpg -o /usr/share/keyrings/mongodb-server-6.0.gpg 
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-6.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list
sudo apt-get update
sudo apt-get install -y mongodb-org
sudo mongod --dbpath /var/lib/mongodb --logpath /var/log/mongodb/mongod.log --fork
ps aux | grep mongod
mongosh
test> show dbs
test> use files_manager
show collections
db.users.find()
db.files.find()
db.users.insertOne({ name: "John Doe", email: "john@example.com" })
db.files.insertOne({ name: "test_file.txt", type: "txt", size: 1024 })
___________________________________________________________________________
