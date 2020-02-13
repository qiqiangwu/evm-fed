# 规范说明
规范遵循[Angular风格指南](https://angular.cn/guide/styleguide)，部分强调单独说明

# 通用规范

## 命名

参考[Angular风格指南](https://angular.cn/guide/styleguide#naming)

# Ionic项目规范

## 项目列表

1. com-evmtv-fed-ruralvitalization

## 应用程序结构与NgModule

````
ionic-project
├── config
|   ├── xingcun
│   └── ...
├── documentation
├── src
|   ├── app
│   |   ├── projects
│   |   |   ├── xingcun
│   |   |   └── ...
│   |   ├── standard
│   |   |   ├── components
│   |   |   ├── models
│   |   |   ├── pages
│   |   |   ├── pipe
│   |   |   ├── services
│   |   |   ├── types
│   |   |   └── standard.module.ts
|   ├── assets
|   ├── config
|   ├── environments
|   ├── theme
|   ├── global.scss
|   ├── index.html
|   └── theme.less
├── www
├── packages.json
````

注：以上目录仅列出部分
* config 用于不同地方项目配置文件
* documentation 项目文档，npm run compodoc:app生成
* src/app/projects/** 目录下为不同地方项目的个性化代码，目录结构参考src/app/standard介绍
* src/app/standard 标准模块目录，包含项目通用页面，其他项目复用的组件、服务、管道等
* src/app/standard/components/** 标准模块下通用组件，每个组件为领域模块，地方项目可以导入使用
* src/app/standard/models/** 标准模块使用的类或者接口定义
* src/app/standard/pages/** 标准模块下通用页面
* src/app/standard/pipe/** 标准模块下通用管道，每个管道为领域模块，地方项目可以导入使用
* src/app/standard/services/** 应用的服务，注册到根模块，可以直接注入
* src/app/standard/types/** 标准模块定义的type
* src/app/standard/standard.module.ts 标准模块的NgModule，主要用于定义路由


