  
# amwiki常用操作  
重建 C:\Program Files\nodejs>babel-node amWiki\bin\main.js -c  
 
# 配置参考
[config配置](https://amwiki.org/doc/index.html?file=030-%E6%96%87%E6%A1%A3%E6%8A%80%E6%9C%AF%E7%AF%87/100-config%E9%85%8D%E7%BD%AE)  

# 安装amwiki报异常解决  
  
## Unexpected token ...  
let [nodePath, mainPath, command, ...parameters] = process.argv;  
                                  ^^^  
SyntaxError: Unexpected token ...  
  
## 原因：  
让nodeJS支持ES6  
  
## 参考  
> [让nodeJS支持ES6的词法----babel的安装和使用](http://www.genshuixue.com/i-cxy/p/7993263)    
[nodejs支持ES6语法(BABEL)  
](http://m.blog.csdn.net/dandan_feifei/article/details/72668317)   
  
npm install es-checker -g  
es-checker  
  
C:\Program Files\nodejs  
npm install babel-cli -save-dev  
npm install babel-cli -g  
新建.babelrc  
{  
“presets”: [  
“es2015”  
],  
“plugins”: []  
}  
F:\nodejs\npm install babel-preset-es2015 -save-dev  
  
----  
  
Q  
ReferenceError: GBK is not defined  
A  
var GBK = function () {  
加了个var  
  
C:\Program Files\nodejs>babel-node amWiki\bin\main.js -c  
  
C:\Program Files\nodejs>babel-node amWiki\bin\test.js  
1 2 3  
  
[test.js](assets\test.js)

ReferenceError: Unknown plugin "stage-3" specified in "C:\\Program Files\\nodejs\\amWiki\\.babelrc"  
去掉"stage-3"

#nodejs版本 node-v5.12.0-x86.msi