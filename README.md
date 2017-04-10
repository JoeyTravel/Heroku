# Heroku
## Setup
 * [Heroku](Heroku.com)
 
## CLI

1. `heroku login`
2. `git clone https://github.com/heroku/node-js-getting-started.git`
3. `cd node-js-getting-started`
4. `heroku create`
5. `git push heroku master`
6. `heroku ps:scale web=1`
7. `heroku open`
8. `heroku logs --tail`
9. `heroku ps`
10. `heroku ps:scale web=0`
11. `heroku ps:scale web=1`
12. `npm install`
13. `heroku local web`
14. `npm install --save --save-exact cool-ascii-faces`

```node.js
var cool = require('cool-ascii-faces');
var express = require('express');
var app = express();

app.set('port', (process.env.PORT || 5000));

app.use(express.static(__dirname + '/public'));

// views is directory for all template files
app.set('views', __dirname + '/views');
app.set('view engine', 'ejs');

app.get('/', function(request, response) {
  response.render('pages/index')
});

app.get('/cool', function(request, response) {
  response.send(cool());
});

app.listen(app.get('port'), function() {
  console.log('Node app is running on port', app.get('port'));
});
```



