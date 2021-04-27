### 1、都是检测对象内是否有某个属性
```
const a = {
    b : 1
}
a.hasOwnPropert('b')    // true
a.hasOwnPropert('c')    // false
"b" in a    // true
"c" in a    // false
```
### 2、hasOwnPropert不检查原型链，in检查原型链
```
Object.prototype.phone= '123456';
a.phone // 123456
a.hasOwnPropert('phone')    // false
"phone" in a    // true
```