#### （1）都是改变函数内this的指向
```
// （1）绑定的函数（2）后面都是参数
m.say.call(xh,"实验小学","六年级"); 
m.say.apply(xh,["实验小学","六年级"]);
m.say.bind(xh)();
```
#### （2）call和apply的区别就是后面传参数的区别
#### （3）bind和call和apply的区别就是
> call和apply都是直接执行函数<br/>
> bind不会直接执行
#### （4）bind写法也可以和call差不多也可以特殊一点
```
m.say.call(xh,"实验小学","六年级");
m.say.bind(xh,"实验小学","六年级")();
m.say.bind(xh)("实验小学","六年级");
```