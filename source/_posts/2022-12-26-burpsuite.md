---
title: Mac下 安装BurpsuiteProfession
date: 2022-12-26 21:22:14
tags:
---

# Mac下安装BP Profession

### 背景

之前用的注册机现在不能使用了，需要换新的。

原来：https://github.com/TrojanAZhen/BurpSuitePro-2.1

现用：https://github.com/h3110w0r1d-y/BurpLoaderKeygen



### 安装

先到官网下载安装。

https://portswigger.net/burp/releases

按往常一样，将jar包放到Burpsuite app同级目录下，

![](..//img/test2.png)

运行：

```
cd /Applications/Burp\ Suite\ Professional.app/Contents/Resources/app && "/Applications/Burp Suite Professional.app/Contents/Resources/jre.bundle/Contents/Home/bin/java" "--add-opens=java.desktop/javax.swing=ALL-UNNAMED" "--add-opens=java.base/java.lang=ALL-UNNAMED" "--add-opens=java.base/jdk.internal.org.objectweb.asm=ALL-UNNAMED" "--add-opens=java.base/jdk.internal.org.objectweb.asm.tree=ALL-UNNAMED" "--add-opens=java.base/jdk.internal.org.objectweb.asm.Opcodes=ALL-UNNAMED" "-javaagent:BurpLoaderKeygen.jar"  "-jar" "/Applications/Burp Suite Professional.app/Contents/Resources/app/burpsuite_pro.jar"
```



开另一个终端：

```
/Applications/Burp\ Suite\ Professional.app/Contents/Resources/jre.bundle/Contents/Home/bin/java -jar /Applications/Burp\ Suite\ Professional.app/Contents/Resources/app/BurpLoaderKeygen.jar
```

按往常的注册流程即可。

为方便运行，

修改vmoptions.txt

```
-XX:MaxRAMPercentage=50
-include-options user.vmoptions--add-opens=java.desktop/javax.swing=ALL-UNNAMED
--add-opens=java.base/java.lang=ALL-UNNAMED
--add-opens=java.base/jdk.internal.org.objectweb.asm=ALL-UNNAMED
--add-opens=java.base/jdk.internal.org.objectweb.asm.tree=ALL-UNNAMED
--add-opens=java.base/jdk.internal.org.objectweb.asm.Opcodes=ALL-UNNAMED
-javaagent:BurpLoaderKeygen.jar
-Xmx2048m
```

![](..//img/test1.png)

之后就可以正常使用了。

### 参考

https://www.sqlsec.com/2019/11/macbp.html#BP-2022-1
