# angular-seed.01
angular-seed入门


用Angular-seed可以快速的搭建一个基于Angular的WebApp工程。

但Angular-seed只是最基本的Angular项目，在设计时就没有考虑对Grunt的支持，只涵盖了Angular最基本的内容。


安装步骤：

1、安装Node.js(最新版本的nodejs自带了npm)和git。 

下载安装包https://nodejs.org/en/download/,http://git-scm.com/;

系统变量：Path 下面配置 C:\Program Files\nodejs\;D:\Git\bin 和D:\Git\mingw64\libexec路径按个人安装配置，之后就可以在cmd里面随便用git命令了;

安装完可以用cmd：node --version 和 git --version 还有 npm --version 查看是否安装成功并且显示当前版本号。

2、获取Angular-seed源码

git clone https://github.com/angular/angular-seed.git

cd angular-seed

3、安装依赖库

npm install

4、运行

npm start

运行成功之后访问http://localhost:8000/app/index.html

bug：npm启动后不能访问http://localhost:8000/

输入npm start可以启动 但是进入 "http://localhost:8000/" 时出现：

http.js:733
      throw new TypeError('The header content contains invalid characters');
            ^
TypeError: The header content contains invalid characters
    at ServerResponse.OutgoingMessage.setHeader (http.js:733:13)
    at ResponseStream.(anonymous function) [as setHeader] (D:\Git\Git\angular-phonecat\node_modules\union\lib\response-stream.js:86:34)
    at serve (D:\Git\Git\angular-phonecat\node_modules\ecstatic\lib\ecstatic.js:146:11)
    at D:\Git\Git\angular-phonecat\node_modules\ecstatic\lib\ecstatic.js:139:9
    at Object.oncomplete (fs.js:108:15)

后来将package.json里的"http-server": "^0.6.1",改为"http-server": "^0.9.0",   问题解决~~


