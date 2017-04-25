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
15. `npm install`
16. `heroku local`
17. `git add .`
18. `git commit -m "Demo"`
19. `git push heroku master`
20. `heroku open cool`
21. `heroku addons:create papertrail`
22. `heroku addons`
23. `heroku addons:open papertrail`
24. `heroku run node`
25. `heroku run bash`
26. `heroku config:set TIMES=2`
27. `heroku config`
28. `heroku addons:create heroku-postgresql:hobby-dev`
29. `npm install`
30. `heroku pg:psql`
31. `ng set --global warnings.packageDeprecation=false`
32. `mkdir src/app/contacts`
33. `ng generate class contacts/contact`
34. `ng generate component contacts/contact-details`
35. `ng generate component contacts/contact-list`
36. `ng generate service contacts/contact`
37. 


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

### Structure of the `server.js` file:
 * Create a database variable outside of the database connection callback to reuset the connection in the app.
 * Connect to the database before starting the application server.
 * Save database object from the callback for reuse.
 * Initialize the app.
 * Contacts API routine:
  * Generic error handler used by all endpoints.
