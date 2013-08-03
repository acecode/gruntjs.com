Grunt网站 (Grunt Website)
==========================


## 构建 Build

1. 安装依赖包
  `npm install`
1. 取得最新文档，生成网站
  `grunt`


## 配置开发环境 Setup Development

1. 安装依赖包
  `npm install`
1. 取得最新文档，生成网站 - gets the latest docs, generates the site
  `grunt`
1. 你可以使用```grunt watch```来自动构建模板与less文件，(注：文档会被多次生成)
   use ```grunt watch``` if you are editing templates or less files. (Note: doc pages will have to be regenerated)

## 运行服务器 Run Server

1. `grunt server`

## 测试 Run Tests

1. 确认已经开启服务器 Make sure the server is running
1. `grunt test`

## 备注 Notes

1. 默认服务器端口是 5678 ，它是在`Gruntfile`中被定义的
  Default server port is : `5678`. Configured in the `Gruntfile`

## 部署到 Heroku Deploy to Heroku

按需要设置Heroku key
Set Heroku keys (if needed) with
```
ssh-keygen -t rsa -C "YOUR_HEROKU_EMAIL" -f  ~/.ssh/id_rsa_heroku

ssh-add ~/.ssh/id_rsa_heroku

heroku keys:add ~/.ssh/id_rsa_heroku.pub

```

推送上服务器 Push

```
git push git@heroku.com:grunt.git master:master
```

如果需要重新生成网站，请使用空提交
If you need to regenerate the Heroku site, use empty commits:

```
git commit --allow-empty -m "empty commit"
git push git@heroku.com:grunt.git master:master
```

