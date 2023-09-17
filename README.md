# JarsAuthBreaker

JarsAuth殴打工具

![81b5966c1e195356f8afdbf920838388](https://github.com/METSUBOUJINRAIxNET/JarsAuthBreaker/assets/110760759/9b5ec8e2-1d25-4fd5-84cd-82f4872df23e)

## 使用方法

1. 从 [Releases](https://github.com/METSUBOUJINRAIxNET/JarsAuthBreaker/releases) 下载文件，并放到 **.minecraft** 或 **版本隔离** 的目录下 [**不要放在mods文件夹**] ，或自行选择一个目录放置JAB，然后给当前版本添加**JVM**参数 **-javassist:<JAB文件名/完整路径>**
2. 未添加自定义模组的情况下启动游戏，等待出现提示“Hash变动”的弹窗后关闭游戏，生成的HASH已自动复制到剪贴板
3. 给当前版本添加**JVM**参数 **-Djab.notify=false -Djab.hash=<生成的HASH>**
4. 再次启动游戏，如果设置正确，此时JarsAuth应该已经被解除并允许添加自定义模组进服
5. 服务器的整合包更新后，再进行一次此流程


## 其他破解方法

由于JarsAuth的若只代码，可以在不使用此工具的情况下殴打

1. 将要安装的模组放入mods文件夹
2. 更改 **<游戏运行目录>\config\jarsauth.client.toml** 中的 **exclusions** 项，添加自己安装的模组 (**mods/<文件名>**)，例如
```toml
exclusions = ["mods/mymod.jar"]
```
3. 启动游戏，进入服务器，此时自行添加的mod文件已在Hash计算中被排除

**此方法在每次添加/更改模组时都需要进行，并且不允许修改已有的模组**


## 注意事项
- 此工具仅用于规避JarsAuth验证并添加自定义**功能/优化**模组，使用此工具作弊原作者不负任何责任
