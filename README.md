# -vue-cli-3.x-
webpack的配置和文件地方

![](C:\Users\YKB\Desktop\github\vue-cli-3.x-\webpack.jpg)



## vue.config.js

vue-cli3里可以调整 webpack 配置最简单的方式就是在 `vue.config.js` 中 .

`vue.config.js` 是一个可选的配置文件，如果项目的 (和 `package.json` 同级的) 根目录中存在这个文件，那么它会被 `@vue/cli-service` 自动加载。你也可以使用 `package.json` 中的 `vue` 字段，但是注意这种写法需要你严格遵照 JSON 的格式来写。

这个文件应该导出一个包含了选项的对象：

```
// vue.config.js
module.exports = {
  // 选项...
}
```

```
// vue.config.js
module.exports = {
    // 选项...
    baseUrl:"./",
    outputDir:"dist",
    assetsDir:"assets",
    indexPath:"index.html",
    filenameHashing:true,
    pages:undefined,
    lintOnSave:true,
    runtimeCompiler:false,
    transpileDependencies:[],
    productionSourceMap:false,
    crossorigin:undefined,
    integrity:false,
    devServer:{//代理
        port:8086,
        proxy:'http://192.168.255.201:8082'
    }
}
```