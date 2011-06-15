require.paths.unshift('./node_modules');

if(process.env.VCAP_SERVICES){
  var env = JSON.parse(process.env.VCAP_SERVICES);
  var mongo = env['mongodb-1.8'][0]['credentials'];
}
else{
  var mongo = {
    "hostname":"localhost",
    "port":27017,
    "username":"",
    "password":"", 
    "name":"",
    "db":"db"
  }
}

/* Mongo Variables */
var Db = require('mongodb').Db,
  Connection = require('mongodb').Connection,
  Server = require('mongodb').Server,
  BSON = require('mongodb').BSONNative;

var db = new Db('visits', new Server(mongo.hostname, mongo.port, {}), {} );

/* Http Variables */
var port = (process.env.VMC_APP_PORT || 3000);
var host = (process.env.VCAP_APP_HOST || 'localhost');
var http = require('http');

/* Connect to the DB, auth and start web server */
db.open(function(err, conn) {
  db.authenticate(mongo.username, mongo.password, function(err, success) {
    http.createServer(function (req, res) {

      /* Retrieve the 'ips' collection
         MongoDB will create the collection if needed. */
      conn.collection('ips', function(err, collection){
        /* Simple object to insert: ip address and date */
        ip = req.connection.remoteAddress;
        ts = new Date();
        object_to_insert = { 'ip': ip, 'ts': ts };

        /* Insert the object then print in response */
        /* Note the _id has been created */
        collection.insert( object_to_insert );
        res.writeHead(200, {'Content-Type': 'text/plain'});
        res.write(JSON.stringify(object_to_insert));
        res.end('\n');
      });
    }).listen(port, host);
  });
});
