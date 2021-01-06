1、let，const
```
块级作用域
变量与常量
```
2、结构赋值（数组，对象）
```
const arr = [1,2,3]
const [a,b,c] = arr

const object = {number:1,arr:[1,2,3],string:'str'}
const {number} = object 
```
3、剪头函数
```
简化function test(){}
()=>{}

不带this,没有arguments

可简写,单个参数并且直接返回,val => val

剩余参数,(a,...b) => {console.log(b)},b为剩余参数
```
4、拓展运算符
```
let arr = [1,2,3]
console.log([...arr,4,5,6])

伪数组转成数组
const arr = document.getElementsByTagName('div')
console.log([...arr])
```
5、Array.from
```
类数组转成数组
let arrayList = {
    '0':1,
    '1':2,
    'length':2
}
Array.from(arrList) // [1,2]

后面可以加多一个函数，处理值
Array.from(arrList,val=>val*2) // [2,4]
```
5、find，findIndex
```
返回第一个retrun true的结果
let arr = [1,2,3]
arr.find((val)=>{
    return val === 2    // 2 返回结果
})
arr.findIndex((val)=>{
    return val === 2    // 1 返回下标
})
```
6、includes
```
let arr = [3,6,9]
arr.includes(3) // true
arr.includes(4) // false
```
7、模板字符串
```
const str = 'hello'
const string = `${str} wordl`

方法插入
const a = ()=> str + 1
const string = `${a()} wordl`
```
8、startsWith,endsWith
```
let str = 'wwwq'
str.startsWith('www') // true
str.endsWith('q') // true
```
9、repeat
```
‘x’.repeat(3)   // 'xxx'
‘x’.repeat(0)   // ''
```
10、set新的数据结构（类似于object和arr）
```
创建
let set = new Set([1,2,3,3])  //[1,2,3] 自动去重复
add,增加
set.add(4)  // 返回set对象
delete,删除
set.delete(3)   // true
has,是否有
set.has(2)  // true
clear,清空
set.clear()

set.forEach((val)=>{
    // 循环
})
```