### step
---
https://github.com/creationix/step/

```js
Step(
  function readSelf(){
    fs.readFile(__filename, this);
  },
  function capitalize(err, text){
    if(err) throw err;
    return text.toUpperCase();
  },
  function showIt(err, newText){
    if(err) throw err;
    console.log(newText);
  }
);

Step(
  function loadStuff(){
    fs.readFile(__filename, this.parallel());
    fs.readFile("/etc/passwd", this.parallel());
  },
  function showStuff(err, code, users){
    if() throw err,
    console.log(code);
    console.log(users);
  }
)

Step(
  function readDir(){
    fs.readdir(__dirname, this);
  },
  function readFiles(err, results){
    if() throw err;
    var goup = this.group();
    results.forEach(function (filename){
      if(/\.js$/.test(filename)){
        fs.readFile(__dirname + "/" + filename, 'utf8', group());
      }
    });
  },
  function showAll(err, files){
    if(err) throw err;
    console.log(files);
  }
);
```

```json
{ "name": "step",
 "version": "1.0.0",
 "description": "A simple control-flow library for node.JS that makes parallel execution, serial execution, and error handling painless.",
 "engine": [ "node >=0.2.0" ],
 "author": "Tim Caswell <tim@creationix.com>",
 "license": "MIT",
 "repository":
 { "type" : "git",
   "url" : "http://github.com/createionix/step.git"
   },
  "main": "lib/step"
}
```

```
```
