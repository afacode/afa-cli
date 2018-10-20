# afa-cli
自定义前端脚手架工具 afa-cli

# 安装
```
npm install -g afa-cli
```
or
```
git clone https://github.com/afacode/afa-cli

cd afa-cli && npm install

npm link
```

# 使用
打开命令行 `afa-cli` or `afa-cli -h` , 帮助信息:
```
  Usage: afa-cli <command>


  Commands:

    add|a      Add a new template
    list|l     List all the templates
    init|i     Generate a new project
    delete|d   Delete a template

  Options:

    -h, --help     output usage information
    -V, --version  output the version number
```

# Commands
### add | a
添加自定义的模板信息 `templates.json`.
```
$ afa-cli add
```
```
 /*  模板名称 */
Template name: koa2-mysql

 /* 你的模板地址 */
Git https link:  https://github.com/afacode/koa2-mysql-demo 

 /* 选择模板分支 */
Branch: master 
```
确定以后, 你将看到类似的信息:
```

{ tpl:
   { 'koa2-mysql':
      { url: 'https://github.com/afacode/koa2-mysql-demo',
        branch: 'master' } } }
```
看到类似这样的信息, 添加模板成功

### list | l
显示模板列表.
```
$ afa-cli list

{ tpl:
   { 'koa2-mysql':
      { url: 'https://github.com/afacode/koa2-mysql-demo',
        branch: 'master' } } }
```

### init | i
初始化你的项目(选择模板).
```
$ afa-cli init

Template name: koa2-mysql

Project name: my-new-project
```
确认后:
```
Start generating...

 √ Generation completed!

 cd my-new-project && npm install
```
安装成功

### delete | d
删除你的模板:
```
$ afa-cli delete
```
要删除的模板名称:
```
Template name: koa2-mysql
```
如果模板存在:
```

{ tpl:
   { 'koa2-mysql': undefined } }
```
删除成功.


# License
MIT.