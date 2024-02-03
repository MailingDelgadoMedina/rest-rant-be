# Project REST-Rant

REST-Rant is an app where users can review restaurants.  

Here are the steps on how to create this project:
- crete your node file by typing: `npm init -y`
- crete a file named: `index.js`
- create a `.gitignore` file and add to it the following:
    - `node_modules`
    - `.env`
    - `.DS_Store`
- Type in your terminal making sure you are in your `rest-rant` folder:
    - `npm install express --save`
    - `npm install nodemon --save-dev`

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
```





