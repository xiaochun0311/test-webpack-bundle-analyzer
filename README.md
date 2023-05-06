[webpack-bundle-analyzer]是一个用于分析Webpack打包文件大小和组成的工具。它生成一个视觉化表示打包文件内容的报告，包括单独模块和其依赖关系的信息，以帮助识别潜在的优化机会。在大型项目中，可以使用此工具来查找和删除不必要的依赖项，将代码拆分成更小的chunks等。
### 引入方式
```bash
# NPM
npm install --save-dev webpack-bundle-analyzer
# Yarn
yarn add -D webpack-bundle-analyzer
```
### 使用方式
使用此工具很简单。首先，在Webpack配置文件中安装和引入webpack-bundle-analyzer插件。然后，运行Webpack构建命令时添加--profile参数以生成构建性能数据，最后再运行webpack-bundle-analyzer命令来启动报告生成器。该工具将在浏览器中打开一个页面，显示出打包文件的可视化图表和各个模块的详细信息。用户可以通过缩放、过滤等方式进行交互操作，以更好地理解打包文件的组成和优化机会。
```js
const BundleAnalyzerPlugin = require('webpack-bundle-analyzer').BundleAnalyzerPlugin;

module.exports = {
  plugins: [
    new BundleAnalyzerPlugin()
  ]
}
```
