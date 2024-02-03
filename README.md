# Project REST-Rant

REST-Rant is an app where users can review restaurants.  

## Here are the steps on how to create the fist part of this project:
- crete your node file by typing: `npm init -y`
- crete a file named: `index.js`
- create a folder named `controllers` inside the folder create a file named `places.js`
- The `places.js` should have the following code: 

    ```javascript

    const router = require('express').Router();

    router.get('/', (req,res)=>{
    res.send('Hello from GET places!')
    })

    module.exports = router;

```

- create a `.gitignore` file and add to it the following:
    - `node_modules`
    - `.env`
    - `.DS_Store`
- Type in your terminal making sure you are in your `rest-rant` folder:
    - `npm install express --save`
    - `npm install nodemon --save-dev`
    - `npm i dotenv`

- On your `package.json` it should have the following:

```javascript
    {
  "name": "my-node-project",
  "version": "1.0.0",
  "description": "My Node.js project",
  "main": "app.js",
  "scripts": {
    "start": "nodemon app.js"
  },
  "dependencies": {
    "express": "^5.0.0"
  },
  "devDependencies": {
    "nodemon": "^2.0.14"
  },
  "license": "MIT"
}

```

- create a `.env` file and add the following"
```javascript
PORT=3001
```

 - Your `index.js` should have the following content in it:
```javascript
require('dotenv').config()
const express = require('express')
const app = express()

app.use('/places', require('./controllers/places'))
app.get('/', (req, res) => {
    res.send('Hello world!')
})

app.get('*', (req, res) =>{
    res.status(404).send('<h1>404 PAGE NOT FOUND</h1>')
})

app.listen(process.env.PORT); 

```

- Type in your terminal `nodemon` make sure you are in your `rest-rant` folder.
- Navigate to your browser to [http://localhost:3001/](http://localhost:3001/) to see your *(Hello World)* message.

- Navigate to your browser to [http://localhost:3001/places](http://localhost:3001/places ) to see your *(Hello from GET places!)* message.

- Navigate to your browser to [http://localhost:3001/123](http://localhost:3001/123 ) to see your *(404 PAGE NOT FOUND)* message.

 Here you have your first node project! 
**FYI to stop your server press on Windows `CTRL + c` and on Mac `control + c`**








