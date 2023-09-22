# JarsAuthBreaker

JarsAuth殴打工具

![81b5966c1e195356f8afdbf920838388](https://github.com/METSUBOUJINRAIxNET/JarsAuthBreaker/assets/110760759/9b5ec8e2-1d25-4fd5-84cd-82f4872df23e)

## 使用方法

1. 从 [Releases](https://github.com/METSUBOUJINRAIxNET/JarsAuthBreaker/releases) 下载文件，并放到 **.minecraft** 或 **版本隔离** 的目录下 [**不要放在mods文件夹**] ，或自行选择一个目录放置JAB，然后给当前版本添加**JVM**参数 **-javassist:<JAB文件名/完整路径> -Djab.version=<JarsAuth版本(默认20230817)**
2. 未添加自定义模组的情况下启动游戏，等待出现提示“Hash变动”的弹窗后关闭游戏，生成的HASH已自动复制到剪贴板
3. 给当前版本添加**JVM**参数 **-Djab.notify=false -Djab.hash=<生成的HASH>**，禁用Hash变动提示并设定伪装的Hash
4. 再次启动游戏，如果设置正确，此时JarsAuth应该已经被解除并允许添加自定义模组进服
5. 服务器的整合包更新后，在未作任何更改（包括新增模组和更改JVM参数）的整合包中重新进行一次此操作

## 支持版本

- 20230817
- 20230820 (JAB 230922+)

## JVM启动参数注释

- **-javaagent:<JAB>** 设置JavaAgent
- **-Djab.hash** 设置JAB FakeHash
- **-Djab.version** 设置JAB注入使用的JarsAuth版本 (230922+)
- **-Djab.notify** 启用/关闭JAB Hash更新弹窗
- **-Djab.debug** 启用/关闭调试，启用后将在注入和验证包发送时弹窗 （230922+）

**PCL2**
![image](https://github.com/SpinningDev/JarsAuthBreaker/assets/110760759/2d30ac6a-0f11-48a9-a365-5ff9f0d9988a)
![image](https://github.com/SpinningDev/JarsAuthBreaker/assets/110760759/44129093-e8fc-4784-b1ea-6a60bac0469d)

**HMCL (1)**
![image](https://github.com/SpinningDev/JarsAuthBreaker/assets/110760759/77783cae-49a1-433f-8471-53207e524516)
![image](https://github.com/SpinningDev/JarsAuthBreaker/assets/110760759/d1e2b0d4-cc6f-466a-8d11-6f66efbf0df0)
![image](https://github.com/SpinningDev/JarsAuthBreaker/assets/110760759/4ab8aca9-2b68-4620-a99d-55a75bbef43e)

**HMCL(2)**
![image](https://github.com/SpinningDev/JarsAuthBreaker/assets/110760759/ccdc2601-6a28-49b8-9dc1-1e2d4520b6a7)
![image](https://github.com/SpinningDev/JarsAuthBreaker/assets/110760759/74716c2b-e694-47db-bfe0-08f1a3ed8765)
![image](https://github.com/SpinningDev/JarsAuthBreaker/assets/110760759/7e3afb4c-3725-4cff-a117-b2e88853272c)


## 其他破解方法

**此方法适用于JarsAuth 20230817及以前，已确认20230820已经移除本地配置**

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
