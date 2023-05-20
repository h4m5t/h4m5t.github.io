# My Blog

> 记录一些博客配置方面的问题。

```
skip_render: README.md # 不把README.md解析为html
```

```
post_asset_folder: true
当资源文件管理功能打开后，Hexo将会在你每一次通过 hexo new [layout] <title> 命令创建新文章时自动创建一个文件夹。这个资源文件夹将会有与这个文章文件一样的名字。将所有与你的文章有关的资源放在这个关联文件夹中之后，你可以通过相对路径来引用它们，这样你就得到了一个更简单而且方便得多的工作流。
```

发现每次hexo g之后，Custom domain会消失，导致404。在Source下创建CNAME文件可解决此问题。