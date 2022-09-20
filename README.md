# node.js-with-html
assignment
const express = require('express')
const app = express()
const port =2000

app.use(express.static('one'))
app.use('/css', express.static(__dirname + 'one/css'))
app.use('/img', express.static(__dirname + 'one/img'))

app.set('views', './views')
app.set('view engine', 'ejs')

app.get('', (req , res) => {
    res.render('index')
})


app.listen(port, () => console.info(`Listening on port ${port}`))

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Please run</title>
    <style> 
    body {background-color: black;}
    h1 {color: red;}
    </style>
</head>
<body>
    
    <h1> Hello world</h1>
    <img src="img/pmp.jpg" alt="pmp">
    
</body>
</html>

