# React
检查是否安装node.js
node-v  

**安装nodejs**  
npm install -g cnpm --registry=https://registry.npm.taobao.org  

**初始化项目**
npm init -y

**安装webpack**
安装install webpack webpack-cli --save-dev

**建立目录结构**
mkdir src&&dist

**建立入口文件**
index.js index.html

**配置webpack**
	
	module.exports = {
	    mode:"development"
	}
**安装webpack-dev-server 和 html-webpack-plugin**
	webpack-dev-server配置在json中
	html-webpack-plugin配置在webpack的plugins中
	pugins需要实例化插件

	const htmlWebPackPlugin = require('html-webpack-plugin')
	const path =require('path')
	
	const htmlPlugin = new htmlWebPackPlugin(
	    {
	        template:path.join(__dirname,'./src/index.html'),
	        filename:'index.html'
	    }
	)
	module.exports = {
	    mode:"development",
	    plugins:[
	        htmlPlugin
	    ]
	    
	}

**处理jsx文件**  
	安装babel：

	cnpm i babel-preset-env babel-preset-stage-0 -D  
	cnpm i babel-loader babel-core babel-plugin-transform-runtime -D   
	
	配置babel：
	建立.babelrc
	{
    "presets":["env","stage-0","react"],
    "plugins":["transform-runtime"]
	} 
  	
	可能会提示babel-loader需要7.0的包
