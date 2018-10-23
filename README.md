# node-cheatsheet
Self notes for starting a Node app

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



