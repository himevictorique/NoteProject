### express-project

> 搭建基于Express框架运行环境


    * 安装express generator生成器
    * 通过生成器自动创建项目
    * 配置分析

###### · 安装

```javascript
cnpm i -g express-generator
express --version        // 查看版本
express express-project  // 创建项目

```
![image](https://github.com/ccyinghua/express-project/blob/master/resource/readimg/image01.png?raw=true)


```javascript
cd express-project
cnpm install   // 安装依赖
node bin/www   // 运行

```
浏览器输入localhost:3000

![image](https://github.com/ccyinghua/express-project/blob/master/resource/readimg/image02.png?raw=true)

#####  · 更换模板引擎

express项目views文件夹内文件格式是.jade格式，若要改成HTML文件。 


```
cnpm install ejs --save   //安装ejs  

```

```
app.js

var ejs = require('ejs');
app.engine('.html',ejs.__express);  // 设置html后缀模板引擎
app.set('view engine', 'jade'); 改成 app.set('view engine', 'html');


在views文件夹内建立index.html文件，重新启动express

node bin/www

```
localhost:3000

![image](https://github.com/ccyinghua/express-project/blob/master/resource/readimg/image03.png?raw=true)



