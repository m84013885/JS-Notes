#### （1）重新发起请求
1. 选中Network
2. 点击Fetch/XHR
3. 选择要重新发送的请求
4. 右键选择Replay XHR
#### （2）在控制台修改参数重新请求
1. 选中Network
2. 点击Fetch/XHR
3. 选择Copy as fetch
4. 控制台粘贴代码
4. 修改参数，回车搞定
#### （3）复制JavaScript变量
1. 在控制台中获取变量
2. 使用copy函数，复制控制台的变量
#### （4）控制台获取Elements面板选中的元素
1. 选中元素
2. 控制台输入$0即可
#### （5）控制台引用上一次执行的结果
1. 在控制台进行操作
2. 控制台输入$_即可得到上一步获取的结果
#### （6）$i直接在控制台安装npm包
1. 安装Console Importer插件
2. $i('name')安装npm包
3. 即可访问npm包的api
#### （7）Add conditional breakpoint条件断点的妙用
1. 在调试窗口找到你想调试的代码
2. 在你想调试的地方打断点
3. 在断点地方右键选择breakpoint，然后写入判断内容即可