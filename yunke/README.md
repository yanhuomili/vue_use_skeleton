# yunke

> yunke yifu

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

> 在现有的vue-cli项目中引入 skeleton 骨架   

1. 安装插件：npm install vue-skeleton-webpack-plugin 

2. 在src目录下创建 Skeleton.vue

``` javascript
	<template>
	  <div class="skeleton-wrapper">
	    <header class="skeleton-header"></header>
	    <section class="skeleton-block">
	      <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2aWV3Qm94PSIwIDAgMTA4MCAyNjEiPjxkZWZzPjxwYXRoIGlkPSJiIiBkPSJNMCAwaDEwODB2MjYwSDB6Ii8+PGZpbHRlciBpZD0iYSIgd2lkdGg9IjIwMCUiIGhlaWdodD0iMjAwJSIgeD0iLTUwJSIgeT0iLTUwJSIgZmlsdGVyVW5pdHM9Im9iamVjdEJvdW5kaW5nQm94Ij48ZmVPZmZzZXQgZHk9Ii0xIiBpbj0iU291cmNlQWxwaGEiIHJlc3VsdD0ic2hhZG93T2Zmc2V0T3V0ZXIxIi8+PGZlQ29sb3JNYXRyaXggaW49InNoYWRvd09mZnNldE91dGVyMSIgdmFsdWVzPSIwIDAgMCAwIDAuOTMzMzMzMzMzIDAgMCAwIDAgMC45MzMzMzMzMzMgMCAwIDAgMCAwLjkzMzMzMzMzMyAwIDAgMCAxIDAiLz48L2ZpbHRlcj48L2RlZnM+PGcgZmlsbD0ibm9uZSIgZmlsbC1ydWxlPSJldmVub2RkIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwIDEpIj48dXNlIGZpbGw9IiMwMDAiIGZpbHRlcj0idXJsKCNhKSIgeGxpbms6aHJlZj0iI2IiLz48dXNlIGZpbGw9IiNGRkYiIHhsaW5rOmhyZWY9IiNiIi8+PHBhdGggZmlsbD0iI0Y2RjZGNiIgZD0iTTIzMCA0NGg1MzN2NDZIMjMweiIvPjxyZWN0IHdpZHRoPSIxNzIiIGhlaWdodD0iMTcyIiB4PSIzMCIgeT0iNDQiIGZpbGw9IiNGNkY2RjYiIHJ4PSI0Ii8+PHBhdGggZmlsbD0iI0Y2RjZGNiIgZD0iTTIzMCAxMThoMzY5djMwSDIzMHpNMjMwIDE4MmgzMjN2MzBIMjMwek04MTIgMTE1aDIzOHYzOUg4MTJ6TTgwOCAxODRoMjQydjMwSDgwOHpNOTE3IDQ4aDEzM3YzN0g5MTd6Ii8+PC9nPjwvc3ZnPg==">
	      <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2aWV3Qm94PSIwIDAgMTA4MCAyNjEiPjxkZWZzPjxwYXRoIGlkPSJiIiBkPSJNMCAwaDEwODB2MjYwSDB6Ii8+PGZpbHRlciBpZD0iYSIgd2lkdGg9IjIwMCUiIGhlaWdodD0iMjAwJSIgeD0iLTUwJSIgeT0iLTUwJSIgZmlsdGVyVW5pdHM9Im9iamVjdEJvdW5kaW5nQm94Ij48ZmVPZmZzZXQgZHk9Ii0xIiBpbj0iU291cmNlQWxwaGEiIHJlc3VsdD0ic2hhZG93T2Zmc2V0T3V0ZXIxIi8+PGZlQ29sb3JNYXRyaXggaW49InNoYWRvd09mZnNldE91dGVyMSIgdmFsdWVzPSIwIDAgMCAwIDAuOTMzMzMzMzMzIDAgMCAwIDAgMC45MzMzMzMzMzMgMCAwIDAgMCAwLjkzMzMzMzMzMyAwIDAgMCAxIDAiLz48L2ZpbHRlcj48L2RlZnM+PGcgZmlsbD0ibm9uZSIgZmlsbC1ydWxlPSJldmVub2RkIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwIDEpIj48dXNlIGZpbGw9IiMwMDAiIGZpbHRlcj0idXJsKCNhKSIgeGxpbms6aHJlZj0iI2IiLz48dXNlIGZpbGw9IiNGRkYiIHhsaW5rOmhyZWY9IiNiIi8+PHBhdGggZmlsbD0iI0Y2RjZGNiIgZD0iTTIzMCA0NGg1MzN2NDZIMjMweiIvPjxyZWN0IHdpZHRoPSIxNzIiIGhlaWdodD0iMTcyIiB4PSIzMCIgeT0iNDQiIGZpbGw9IiNGNkY2RjYiIHJ4PSI0Ii8+PHBhdGggZmlsbD0iI0Y2RjZGNiIgZD0iTTIzMCAxMThoMzY5djMwSDIzMHpNMjMwIDE4MmgzMjN2MzBIMjMwek04MTIgMTE1aDIzOHYzOUg4MTJ6TTgwOCAxODRoMjQydjMwSDgwOHpNOTE3IDQ4aDEzM3YzN0g5MTd6Ii8+PC9nPjwvc3ZnPg==">
	    </section>
	  </div>
	</template>
	 
	<script>
	  export default {
	    name: 'skeleton'
	  }
	</script>
	 
	<style scoped>
	  .skeleton-header {
	    height: 40px;
	    background: #1976d2;
	    padding:0;
	    margin: 0;
	    width: 100%;
	  }
	  .skeleton-block {
	    display: flex;
	    flex-direction: column;
	    padding-top: 8px;
	  }
	</style>
```
3. 在src目录下创建entry-skeleton.js文件

``` javascript
	import Vue from 'vue'
	import Skeleton from './Skeleton'
	export default new Vue({
	  components: {
	    Skeleton
	  },
	  template: '<Skeleton />'
	})

```
4. 在build 目录下创建 webpack.skeleton.conf.js

``` javascript
	'use strict';
	const path = require('path')
	const merge = require('webpack-merge')
	const baseWebpackConfig = require('./webpack.base.conf')
	const nodeExternals = require('webpack-node-externals')
	 
	function resolve(dir) {
	  return path.join(__dirname, dir)
	}
	 
	 console.log('webpack.skeleton.conf')
	module.exports = merge(baseWebpackConfig, {
	  target: 'node',
	  devtool: false,
	  entry: {
	    app: resolve('../src/entry-skeleton.js')
	  },
	  output: Object.assign({}, baseWebpackConfig.output, {
	    libraryTarget: 'commonjs2'
	  }),
	  externals: nodeExternals({
	    whitelist: /\.css$/
	  }),
	  plugins: []
	})

```
5. 在webpack.dev.conf.js和webpack.prod.conf.js分别加入

``` javascript
	//首屏加载骨架
	const SkeletonWebpackPlugin = require('vue-skeleton-webpack-plugin')
	// inject skeleton content(DOM & CSS) into HTML
	new SkeletonWebpackPlugin({
	  webpackConfig: require('./webpack.skeleton.conf'),
	  quiet: true
	})
```
6. 在index.html文件#app标签里添加一下代码

``` javascript
	<style type="text/css">
    	html,body{
    		margin: 0;
    		padding: 0;
    	}
    	
    	/*第一种方法*/
    	/*.skeleton {
			    padding: 10px;
			}
			 
			.skeleton .skeleton-head,
			.skeleton .skeleton-title,
			.skeleton .skeleton-content {
			    background: rgb(194, 207, 214);
			}
			 
			.skeleton-head {
			    width: 100px;
			    height: 100px;
			    float: left;
			}
			 
			.skeleton-body {
			    margin-left: 110px;
			}
			 
			.skeleton-title {
			    width: 500px;
			    height: 60px;
			}
			 
			.skeleton-content {
			    width: 260px;
			    height: 30px;
			    margin-top: 10px;
			} */
			
			/*第二种情况*/
			/*.skeleton .skeleton-head,
			.skeleton .skeleton-title,
			.skeleton .skeleton-content {
			    background: rgb(194, 207, 214);
			    background-image: linear-gradient(90deg,rgba(255, 255, 255, 0.15) 25%, transparent 25%);
			    background-size: 20rem 20rem;
			    animation: skeleton-stripes 1s linear infinite;
			}
			 
			@keyframes skeleton-stripes {
			    from {
			        background-position: 0 0 ;
			    }
			    to {
			        background-position: 20rem 0;
			    }
			}*/
			
			
			/*第三种情况*/
			.skeleton {
			  padding: 10px;
			}
			 
			.skeleton .skeleton-head,
			.skeleton .skeleton-title,
			.skeleton .skeleton-content {
			  background: rgb(194, 207, 214);
			}
			 
			.skeleton-head {
			  width: 100px;
			  height: 100px;
			  float: left;
			}
			 
			.skeleton-body {
			  margin-left: 110px;
			}
			 
			.skeleton-title {
			  width: 500px;
			  height: 60px;
			  transform-origin: left;
			  animation: skeleton-stretch .5s linear infinite alternate;
			}
			 
			.skeleton-content {
			  width: 260px;
			  height: 30px;
			  margin-top: 10px;
			  transform-origin: left;
			  animation: skeleton-stretch .5s -.3s linear infinite alternate;
			}
			 
			@keyframes skeleton-stretch {
			  from {
			    transform: scalex(1);
			  }
			  to {
			    transform: scalex(.3);
			  }
			}
    </style>
    
	<div id="app">
		<div class="skeleton">
		    <div class="skeleton-head"></div>
		    <div class="skeleton-body">
		        <div class="skeleton-title"></div>
		        <div class="skeleton-content"></div>
		    </div>
		</div>
    </div>
```
# 具体实现可以将本项目下载运行起来

> css添加背景图片，打包后路径出错的问题

## 解决方法：

在build>utils.js文件里面添加配置：publicPath:'../../'

``` javascript
	if (options.extract) {
      return ExtractTextPlugin.extract({
        use: loaders,
        fallback: 'vue-style-loader',
        publicPath:'../../'
      })
    } else {
      return ['vue-style-loader'].concat(loaders)
    }
```