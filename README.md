bodule-middleware
=================

Bodule的Express中间件，在Express项目中，随心所欲地在浏览器端使用CommonJS模块！

## 安装

    npm install bodule-middleware

## 使用方式

使用`npm`安装在浏览器端使用的模块，例如：

    node_modules/
    ├── backbone
    │   ├── CNAME
    │   ├── CONTRIBUTING.md
    │   ├── LICENSE
    │   ├── README.md
    │   ├── backbone-min.js
    │   ├── backbone-min.map
    │   ├── backbone.js
    │   ├── index.js
    │   └── package.json
    └── underscore
        ├── CNAME
        ├── CONTRIBUTING.md
        ├── LICENSE
        ├── README.md
        ├── favicon.ico
        ├── index.js
        ├── package.json
        ├── underscore-min.map
        └── underscore.js

在expres项目中，添加上bodule-middleware：

    app.use(require('bodule-middleware'));

在web app中：

    doctype 5
    html
      head
        title= title
        link(rel='stylesheet', href='/stylesheets/style.css')
        script(type='text/javascript', src='/bodule-middleware/bodule.js')
        script(type='text/javascript').
          bodule.use(['backbone, underscore'], function(require, exports, module) {
            var Backbone  = reuqire('backbone'),
                _         = require('undercore')
          })
      body
        block content
