# My Blog

> 记录一些博客配置和使用方面的问题。

提交的文件没有README.md
```
skip_render: README.md # 不把README.md解析为html
```

图片引用问题
```
最简单的是引用/img下的图片文件，但是如果图片太多，不方便管理。
为方便管理和引用，开启资源文件管理功能：当资源文件管理功能打开后，Hexo将会在你每一次通过 hexo new [layout] <title> 命令创建新文章时自动创建一个文件夹。这个资源文件夹将会有与这个文章文件一样的名字。将所有与你的文章有关的资源放在这个关联文件夹中之后，你可以通过相对路径来引用它们，这样你就得到了一个更简单而且方便得多的工作流。

方法一（没用）：
网上都说安装这个插件，但是没用，最后卸载了。
npm install -g cnpm --registry=https://registry.npm.taobao.org
安装插件：cnpm install hexo-asset-image --save
参考：https://guguge.top/blog/butterfly/#%E6%9C%AC%E5%9C%B0%E5%9B%BE%E7%89%87%E5%BC%95%E7%94%A8%E9%97%AE%E9%A2%98


方法二（能用）：
安装另外一个插件：npm install hexo-renderer-marked --save


启用后，资源图片将会被自动解析为其对应文章的路径。
例如： image.jpg 位置为 /2020/01/02/foo/image.jpg ，这表示它是 /2020/01/02/foo/ 文章的一张资源图片， ![](image.jpg) 将会被解析为 <img src="/2020/01/02/foo/image.jpg"> 。

参考：https://zhuanlan.zhihu.com/p/265077468
官方说法：https://hexo.io/docs/asset-folders.html


即最终结论：
安装hexo-renderer-marked
开启相关功能(_config.yml)：
post_asset_folder: true #文章资源文件夹
marked:
  prependRoot: true
  postAsset: true

在md文章中，用以下两种方法引用图片：
{% asset_img  1.jpg %}
![pic](1.jpg)
```

域名访问问题

```
发现每次hexo g && hexo d之后，Custom domain会消失，导致404。
解决方法：在Source下创建CNAME文件可解决此问题。
```

多终端同步问题。