# 第一天

项目准备

全局安装vue-cli
npm install --global vue-cli

创建项目
vue init webpack mall


安装依赖包
cd mall
npm install
npm run dev


目录结构：
assets      静态文件目录
components  公共组件
base        基础组件
pages       页面组件
api         数据组件




# 第二天

配置路径

文件位置：build/webpack.base.conf.js     里面的resolve位置


安装插件1：
npm install --save-dev node-sass sass-loader

node-sass 把 sass编译成css
sass-loader 是webpack的一个loader（装配器）  



安装插件2：
cnpm install --save babel-polyfill fastclick

babel-polyfill 转换代码
fastclick  清除300毫秒延时

禁用缩放
<meta name = "viewport" content="user-scalable=no" > 











