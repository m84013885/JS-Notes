#### prototype（构造函数的属性）
当使用某一个方法的时候，会一直向内查找属性，而那些比较隐秘的属性就保留在prototype当中。
```
Array.prototype.min // 其中一个方法
Array.prototype.max // 其中一个方法
```
#### constructor（始终指向创建当前对象的构造函数）
```
const foo = new Array(1,2,3)
console.log(foo.constructor === Array)
```