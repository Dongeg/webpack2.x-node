0.全局安装webpack
```
$ cnpm install -g webpack

```
1.全局安装babel-cli

```
$ cnpm install --global babel-cli

```
1.配置  .babelrc文件
```
  {
    "presets": [
      "latest"
    ],
    "plugins": []
  }
```
2.安装转义规则

```
$ cnpm install --save-dev babel-preset-latest-es2015

```
3.安装 babel-loader

```
$ cnpm install babel-loader --save-dev
```
4.安装 babel-core

```
$ cnpm install babel-core --save-dev
```
5.配置webpack.config.js

```
    var path = require("path")                             //兼容路径
	module.exports = {
	    entry: { 
	    	  index: './src/js/main.js',
	    	},
	       
	    // 输出
	    output: {
	        path: __dirname+'/dist/js',                    // 2.x的路径要这样写
	        filename: "bundle.js",                         //输出文件名
	    },
	     
		module: {
		        //加载器配置
		        loaders: [
		            {
		                test: /\.js|jsx$/, //是一个正则，代表js或者jsx后缀的文件要使用下面的loader
		                loader: "babel-loader",
		                query: {presets: ['es2015']}
		            }
		        ]
		    },
	};  
```
6.编译
```
$ webpack -p
```
