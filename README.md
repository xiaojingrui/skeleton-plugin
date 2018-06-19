## Basic Use

### vue-cli更改之处

#### Step 1

package.json scripts --build改为：

"build": "rm -rf dist &&  cross-env NODE_ENV=production && node build/build.js"

#### Step 2

Add comment `<!-- shell -->` in the root element of you application.
index.html 

```html
  <div id="app"><!-- shell --></div>
```

#### Step 3

webpack.base.conf.js

添加plugins

#### Step 4

webpack.prod.conf.js

new HtmlWebpackPlugin 删掉 removeComments: true,

##### In the development page, use CtrlOrCmd + enter to call out the plugin interactive interface, or enter the toggleBar callout interface in the browser's JavaScript console.

##### page-skeleton-webpack-plugin配置和升级参考 https://github.com/ElemeFE/page-skeleton-webpack-plugin