# JarsAuthBreaker

JarsAuth殴打工具

![81b5966c1e195356f8afdbf920838388](https://github.com/METSUBOUJINRAIxNET/JarsAuthBreaker/assets/110760759/9b5ec8e2-1d25-4fd5-84cd-82f4872df23e)

## 使用方法

1. 从Releases下载文件，并放到 **.minecraft** 或 **版本隔离** 的目录下 [**不要放在mods文件夹**] ，或自行选择一个目录放置JAB，然后给当前版本添加**JVM**参数 **-javassist:<JAB文件名/完整路径>**
2. 未添加自定义模组的情况下启动游戏，等待出现提示“Hash变动”的弹窗后关闭游戏，生成的HASH已自动复制到剪贴板
3. 给当前版本添加**JVM**参数 **-Djab.notify=false -Djab.hash=<生成的HASH>**
4. 再次启动游戏，如果设置正确，此时JarsAuth应该已经被解除并允许添加自定义模组进服
