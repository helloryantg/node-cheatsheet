# node-cheatsheet
Self notes for starting a Node app

## Starting a project with express-generator
1 ) ``` express -e <name-of-project>```
the -e means to use ejs instead of pug
``` npm start ```
rename app.js to server.js
Inside of the www, change line 7 from:
var app = require('../app'); to var app = require('../server');

2) ``` npm i ``` to install node packages
3) change server name
4) delete users router and app.use user

### Create a package.json file and accept all default settings
```npm init -y```

### Download and install a package (installs node_models folder & adds package-lock.json - DO NOT EDIT)
```npm install request```
* It is highly recommended to add ```node_modules``` to ```.gitignore``` file.

### Require the 'request' module in main.js and make HTTP requests:
```
var request = require('request');
request('http://jsonplaceholder.typicode.com/users', function(err, res, body) {
	console.log(body);
});
```
### Install Express
``` npm install express ```

### Create a server.js
``` mkdir first-express ```
``` touch server.js ```
``` npm init ```
Open your code

### Starter code
```
 // Load express
 var express = require('express');
 
 // Create our express app
 var app = express();
 
 // Define a root route directly on app
 // Later, we will use the router object
 app.get('/', function(req, res) {
   res.send('<h1>Hello World!</h1>');
 });
 
 // Tell the app to listen on port 3000
 app.listen(3000, function() {
   console.log('Listening on port 3000');
 });
 ```
 
 ### How to run the server
 ``` node server ```
 
 ### Basic Structure
 ```
  // Require modules
 var express = require('express');
 
 // Create the Express app
 var app = express();
 
 // Configure the app (app.set)
 
 
 // Mount middleware (app.use)
 
 
 // require and mount (app.use) routes

 
 // Tell the app to listen on port 3000
 app.listen(3000, function() {
   console.log('Listening on port 3000');
 });
 ```
 
 ### How to access values
 ```
req.params: Used to access URL parameter values
req.query: Used to access query string values
req.body: Used to access request body contents
```

### Ways to respond to a request
```
res.redirect() - Redirect a request
res.render() - Render a view template
res.json() - Send a JSON response
res.jsonp() - Send a JSON response with JSONP support
res.send() - Send a response of various types
res.sendFile() - Send a file as an octet stream
```

### Configure the app (app.set)
```
app.set('view engine', 'ejs');
app.set('views', path.join(__dirname, 'views'));
app.locals.title = 'First Express';

var express = require('express');
var path = require('path');

npm i ejs
```
Inside the <title> tags, add ```<%= title %>```

### Passing Data to a View
<% %> - executes Javascript as control flow (Squids)
<%= %> - tags for writing into the HTML page (Squids with Ink)

