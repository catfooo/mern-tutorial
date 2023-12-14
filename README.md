things to do -> remove blanks around = at env
: the same error still happens
------------------

problem here - i cant connect to the server. 

this is what i have for .env

NODE_ENV = development
PORT = 3000
MONGO_URI = mongodb+srv://<my id>:<my password>@cluster00.7xnicw8.mongodb.net/mernapp?retryWrites=true&w=majority




the error message i have

MongooseServerSelectionError: Could not connect to any servers in your MongoDB Atlas cluster. One common reason is that you're trying to access the database from an IP that isn't whitelisted. Make sure your current IP address is on your Atlas 





mern-tutorial git:(main) npm run server

> mern-tutorial@1.0.0 server
> nodemon backend/server.js

[nodemon] 3.0.2
[nodemon] to restart at any time, enter `rs`
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,cjs,json
[nodemon] starting `node backend/server.js`
(node:83475) [DEP0040] DeprecationWarning: The `punycode` module is deprecated. Please use a userland alternative instead.
(Use `node --trace-deprecation ...` to show where the warning was created)
Server started on port 3000
MongooseServerSelectionError: Could not connect to any servers in your MongoDB Atlas cluster. One common reason is that you're trying to access the database from an IP that isn't whitelisted. Make sure your current IP address is on your Atlas cluster's IP whitelist: https://www.mongodb.com/docs/atlas/security-whitelist/
    at _handleConnectionErrors (/Users/catfood/dev/mern-tutorial/node_modules/mongoose/lib/connection.js:809:11)
    at NativeConnection.openUri (/Users/catfood/dev/mern-tutorial/node_modules/mongoose/lib/connection.js:784:11)
    at process.processTicksAndRejections (node:internal/process/task_queues:95:5)
    at async connectDB (/Users/catfood/dev/mern-tutorial/backend/config/db.js:5:22) {
  reason: TopologyDescription {
    type: 'ReplicaSetNoPrimary',
    servers: Map(3) {
      'ac-pduuxjk-shard-00-00.0olueje.mongodb.net:27017' => [ServerDescription],
      'ac-pduuxjk-shard-00-01.0olueje.mongodb.net:27017' => [ServerDescription],
      'ac-pduuxjk-shard-00-02.0olueje.mongodb.net:27017' => [ServerDescription]
    },
    stale: false,
    compatible: true,
    heartbeatFrequencyMS: 10000,
    localThresholdMS: 15,
    setName: 'atlas-hjl0mu-shard-0',
    maxElectionId: null,
    maxSetVersion: null,
    commonWireVersion: 0,
    logicalSessionTimeoutMinutes: null
  },
  code: undefined
}
[nodemon] app crashed - waiting for file changes before starting...
