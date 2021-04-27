map：可以操作数组里每个元素，并且返回一个新的数组（长度和原数组一样的数组）。
```
    const arr =[1,2,3];
    arr.map((v,i)=>{
        console.log(v)  // 值
        console.log(i)  // 下标
        return v    // [1,2,3]
    })
```
filter：遍历数组里每个元素，return符合条件的组合成一个新的数组（长度和原数组不一定一样的数组）。
```
    const arr =[1,2,3];
    arr.filter((v,i)=>{
        console.log(v)  // 值
        console.log(i)  // 下标
        if(v===2){
            return v    // [2]
        }
    })
```
reduce：进行计算求和使用。
```
    const arr =[1,2,3]
    arr.reduce((s,v,i)=>{
        console.log(s)  // 累加值
        console.log(v)  // 值
        console.log(i)  // 下标
    })
