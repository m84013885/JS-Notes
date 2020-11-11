1、map（首先判断参数是否正确，在创建一个数组保留结果，回调函数保存参数保存到数组当中，最后返回数组）
```
function map(arr, callback) {
    if (Array.isArray(arr) && arr.length > 0 && typeof callback === 'function') {
        let result = []
        for (let i = 0; i < arr.length; i++) {
            result.push(callback(arr[i], i, arr))
        }
        return result
    } else {
        return []
    }
}
```
2、filter（首先判断参数是否正确，在创建一个数组保留结果，判断回调函数boolean值，当为true就把值保留到数组，最后返回数组）
```
function filter(arr, callback) {
    if (Array.isArray(arr) && arr.length > 0 && typeof callback === 'function') {
        let result = []
        for (let i = 0; i < arr.length; i++) {
            if (callback(arr[i], i, arr)) {
                result.push(arr[i])
            }
        }
        return result
    } else {
        return []
    }
}
```
3、reduce（首先判断参数是否正确，查看是否有初始值，有初始值就先保留初始值，并且根据有没有初始值来判断循环是0开始还是1开始，循环回调得到结果，最后返回结果）
```
function reduce(arr, callback, initialValue) {
    if (Array.isArray(arr) && arr.length > 0 && typeof callback === 'function') {
        let value = initialValue ? initialValue : arr[0]
        for (let i = initialValue ? 0 : 1; i < arr.length; i++) {
            value = callback(value, arr[i], i, arr)
        }
        return value
    } else {
        return []
    }
}
```