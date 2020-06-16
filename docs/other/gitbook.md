# GitBook 安装及使用

本博客使用的是 GitBook 搭建的。

## 安装

```shell
sudo npm install gitbook-cli -g
```

安装完成后，新建一个项目文件夹 MyGitBook, 使用命令初始化 GitBook。

```shell
gitbook init
```

初始化后会生成两个必要的文件 `README.md` 和 `SUMMARY.md`

- README.md: 书的介绍、简介。在章节中，也可以作为章节的简介。
- SUMMARY.md: 书的章节结构和顺序。

添加文件夹作为文章的章节

## 本地预览

```shell
gitbook serve
```

浏览器打开 `http://localhost:4000` 浏览

## 安装插件

[博文](https://www.jianshu.com/p/427b8bb066e6)
