nvm node版本控制系统

npm 包控制

nrm 包下载资源

- express 框架
```
npm install -g express-generator
express folder_name 
cd folder_name
npm install   安装package.json中的依靠
npm start
```

npm install --save-dev supervisor  安装supervisor这个库，每次改动不用重启服务器。
在package.json中start里改一下路径  ./node_modules/.bin/supervisor

require是引入依赖export是导出
模块中暴露函数
module.exports暴露一个 
exports.暴露多个