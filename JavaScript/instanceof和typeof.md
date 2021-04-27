1、通常判断类型typeof就可以了，但是typeof判断不了引用类型
```
typeof(null)    // object
typeof([])      // object
```
2、instanceof的问题和typeof相反，判断不了普通类型，
```
1 instanceof Number // false
'1' instanceof String // false
true instanceof Boolean // false
null instanceof Object  // false
undefined instanceof Object  // false
// 引用类型的成功
[] instanceof Array // true
const test = {}
test instanceof Object  // true
const test = function(){}
test instanceof Function  // true
// 像是用new创建的普通类型倒是可以判断，但是为了判断类型这些写反而没意义、不实用
new Number(1) instanceof Number // true
new Boolean(true) instanceof Boolean    // true
new String('1') instanceof String   // true
```
3、但是这样下来instanceof还不够typeof实用，起码没那么多问题<br/>
4、最好的方法还是实用Object.prototype.toString.call判断类型，实在不行用typeof
```
function checkType(param) {
    return Object.prototype.toString.call(param).slice(8, -1).toLowerCase()
}
```
