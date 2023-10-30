```
var obj = {
    a: {
        b: {
            c: 12
        }
    }
};


obj.findPath=function(path){
 const keys = path.split('.');
  return keys.reduce((object, key) => {
    return object && object[key]
  }, this)  
}



console.log(obj.findPath('a.b.c')); // 12
console.log(obj.findPath('a.b')); // {c: 12}
console.log(obj.findPath('a.b.d')); // undefined
console.log(obj.findPath('a.c')); // undefined
console.log(obj.findPath('a.b.c.d')); // undefined
console.log(obj.findPath('a.b.c.d.e')); // undefined
```
