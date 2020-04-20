# webpack

1. mkdir webpack-course
2. cd webpack-course
3. mkdir src dist config
4. ls
5. git init .
6. git init -y
7.ls
8. echo "node_modules" > .gitignore
9. npm install -g webpack webpack-cli
10. touch src/index.js dist/index.html
11. code .
12.webpack --mode=devolpment
13. webpack --mode=production
14. touch config/webpack.dev.js
15. rm dist/main.js src/index.js
16.webpack.config.js 

const path=require("path")

module.exports={
    entry:{
        main:["./src/main.js"]
    },
    mode:"development",
    output:{
        filename:"[name]-bundle.js",
        path:path.resolve(__dirname,"../dist"),
        publicPath:"/"
    },
    devServer:{
        contentBase:"dist"
    }
}


npm install -s webpack webpack-cli webpack-dev-server

to run  - webpack --config=config/webpack.dev.js 


-------------------------
index.html
-----------------------

<body>
    <h1>hello world</h1>
    
    <script src="/main-bundle.js"></script>
</body>

------------------------
main.js
------------------
alert('hello')
 
 
============================================================================================

# First Loaders for CSS

touch src/main.css

npm install style-loader css-loader


# main.css

body {
    margin:0;
    background-color: #444;
}

h1{
    height: 100vh;
    display: flex;
    color: white;
    align-items: center;
    justify-content: center;
    font-size: 5em;
    font-family: sans-serif;
    text-shadow: 0 0 20px black;
}


# main.js

require("./main.css")

# index.html

<body>
    <h1>hello world</h1>
    
    <script src="/main-bundle.js"></script>
</body>

 
