This is a one page website develop by useing HTML/CSS/JAVASCRIPT for SnapDCity

Download Node.js 
```nix
Download Node.js from https://nodejs.org/en/download/ first

node -v / npm -v

npm init -y

npm i express

npm i -D nodemon

npm run dev
```

# package.json

```jsx
"scripts":{
	"start": "node index.js",
	"dev": "nodemon index.js"
},
```

# index.js

```jsx
const express = require('express');

const app = express();

app.use(express.json());
app.use(express.static('./public'));

app.get('/url/:id', (req, res) => {
    // TODO: get a short url by id
});

app.get('/:id', (req, res) => {
    // TODO: redirect to url
});

app.post('/url', (req, res) => {
    // TODO: create a short url
});

const port = process.env.PORT || 1337;
app.listen(port, () => {
    console.log(`Listening at http://localhost:${port}`);
});
```
