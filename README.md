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
