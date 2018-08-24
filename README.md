毕业设计\
很简单的Vue单文件组件初步使用\
全局引入了less、Zepto、iconfont
### 在Vue项目里面全局引入Zepto.js
采用`npm`的方式安装`zepto`
```
npm i zepto -S
```
安装之后，并不是就能全局使用`$符号`了。
```
// main.js入口文件
import $ from 'zepto'
```
这样在入口文件里面引入之后，`npm run dev`会报一个错`createElement is not defined`,导致这个错的原因是`zepto`没有模块化。
解决方法是
```
npm i exports-loader
npm i script-loader
```
安装好这两个依赖之后，在`webpack.base.conf.js`里
```
module: {
    rules: [
        {
            test: require.resolve('zepto'),
            loader:'exports-loader?window.Zepto!script-loader'
        }
    ]
}
```
配置好之后，在`main.js`里面引入即可。
### Vue项目里面使用阿里巴巴矢量图标
- 添加购物车
- 下载代码
- 在`assets`目录文件下创建`font`文件夹
- 将下载的部分有用的文件移入这个文件夹
- 在`main.js`中引入
```
import './assets/font/iconfont.css'
```
- 接下来就可以使用类名显示想要的图标了
### 全局引入Less
`webpack.base.conf.js`里面配置如下
```js
{
test: /\.less$/,
loader: "style-loader!css-loader!less-loader",
}
```
网址：[冰蓝工作室](http://www.binglan.org/)

# Run
`npm run dev`
