## Vue中使用TailWIndCSS：
### Vue-cli 3.x+中先引入Postcss在引用TailWindCSS
- 1. 导入postcss：
`npm install -D postcss-loader precss sugarss autoprefixer`
    - 其中第一个插件是postcss-loader，就是一个css-loader
    - 第二个插件precss是一个很牛逼的css插件，能够让你像在Sass，less中那样使用变量，条件，迭代器，自定义属性，媒体查询等新兴的Css功能
    - 第三个插件sugarss，是一个css语法解析器，能够让我们像stylus一样使用缩进来写CSS，使用sugarss解析器之后我们就不必要再添加{}，每条css规则之后也不需要;了。
    - 第四个插件autoprefixer，用于对浏览器兼容的，自动添加prefix。
- 2. 安装完这几个基础模块后（如果不喜欢这种缩进式风格的话，sugarss也可以不安装），我们可以直接在package.json中加入以下内容：
```json
"postcss": {
    "parser": "sugarss", // 配置解析器
    "plugins": {
        "precss": {}, // 引入插件，{}内可以填写插件配置
        "autoprefixer": {}
    }
}
```
> 这个时候我们就能够在项目中来使用到postcss这些插件的功能了

- 3. 导入tailwindcss：
    - `npm install tailwindcss`
    - > 安装完毕之后，新建一个xxx.css的文件，在里面进行tailwindcss模块的导入：
    
    ```css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    ```
    -  *Tips*：这里需要注意一点的是，如果我们在postcss中使用了`postcss-import`插件进行css的模块管理，那么上面的`xxx.css`需要写成原始的css导入形式：
    ```css
    @import 'tailwindcss/base';
    @import 'tailwindcss/components';
    @import 'tailwindcss/utilities';
    ```
    
- 4. 在postcss中使用tailwindcss插件：
```json
"postcss": {
    ...
    "plugins": {
        ...
        "tailwindcss": {}
        ...
    }
}
```
> 之后就可以在项目中直接使用tailwindcss了。

- 5. 如果还需要对tailwindcss进行其他配置的话，可以使用`npx tailwind init`命令创建`tailwind.config.js`配置文件


#### 参考资料
- [B站TailWindCSS学习视频](https://www.bilibili.com/video/BV18J411y7xj?from=search&seid=11864768838841588462)