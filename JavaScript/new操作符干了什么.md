#### 1、创建一个空对象，并且 this 变量引用该对象，同时还继承了该函数的原型。
#### 2、属性和方法被加入到 this 引用的对象中。
#### 3、新创建的对象由 this 所引用，并且最后隐式的返回 this 。
```
function Pet(name,age,hobby){
 	   this.name=name;  //this作用域：当前对象
 	   this.age=age;
 	   this.hobby=hobby;
 	   this.eat=function(){
 	      alert("我叫"+this.name+",我喜欢"+this.hobby+",是个程序员");
 	   }
}
const np = new Pet('www',18,'eee')
np.eat()
```