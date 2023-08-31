# ColorMC用户指南

![](../image/pic.png)

## 目录

- [获取二进制文件](#获取二进制文件)
- [启动启动器](#启动启动器)
- [启动器运行路径](#启动器运行路径)
- [游戏实例与账户](#游戏实例与账户)
- [添加游戏实例](#添加游戏实例)
- [添加与选择账户](#添加与选择账户)
- [启动游戏实例](#启动游戏实例)
- [添加在线整合包](#添加在线整合包)
- [启动器设置](#启动器设置)

## 获取二进制文件

获取启动器二进制文件有3种方式

1. 从Github publish中获取
打开[ColorMC仓库](https://github.com/Coloryr/ColorMC)  
然后点击[Releases](https://github.com/Coloryr/ColorMC/releases)  
根据你的电脑系统选择下载
- windows系统下载win64
- linux系统.deb .pkg.tar.zst .AppImage
- macOs系统下载osx64

2. 从QQ群下载
加入群[571239090](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=iFEiL7JvAbPmM2E351SJlFk4UAHLx2yD&authKey=wyHTk7JbF8B47XYhvAQKmOcGTy3FQ%2FYA62hygi3J1x0KmZsfrlV%2B%2BK0iSyuxn3k1&noverify=0&group_code=571239090)或者[806493738](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=BK6-22zZvH5ERw8JMKqGCv2nVphhFUsf&authKey=eO1qaYSITVwLcarH8AqgZVYqqul7745D8a3aeBRsgss18unQgBKIMi8BpVEgPc0l&noverify=0&group_code=806493738)  
从群文件下载

3. 从源码里面构建
首先安装[dotnet sdk](https://dotnet.microsoft.com/en-us/download/dotnet)  
下载并安装.NET 7  
克隆代码
```
git clone https://github.com/Coloryr/ColorMC.git
cd ColorMC/src/ColorMC.Launcher
```
编译
```
dotnet build
```
完成后在文件夹`src\ColorMC.Launcher\bin\Debug\net7.0`可以获取到二进制

## 启动启动器

- windows和macOs系统，解压即可双击启动
- Linux系统安装包后可以在桌面或菜单中直接启动
- AppImage可以在Linux上直接启动

启动器启动后若有更新会提示下载并更新

## 启动器目录说明

- Windows系统下，游戏会放在启动器根目录下  
账户储存会放在`C:\Users\{User}\AppData\Roaming\ColorMC`
- Linux系统下，游戏和账户储存会放在`~/ColorMC`  
- macOs系统下，游戏放在`/Users/shared/ColorMC`  
账户储存会会放在`/Users/{User}/ColorMC`

启动器启动后会创建如下的文件夹结构
- download    下载缓存
- image       图片缓存
- java        下载的Java
- minecraft   游戏文件
  - assets         游戏资源文件
  - instances      游戏实例
  - libraries      游戏运行库
  - versions       游戏版本储存
- tool        工具文件夹
- config.json   核心配置文件
- gui.json      GUI配置文件
- count.dat     游戏统计储存
- lock          启动器锁定
- logs.log      启动器日志
- maven.json    本地运行库信息

在账户文件夹只有一个`auth.json`文件，里面是账户数据

## 游戏实例

ColorMC是`多实例`游戏启动器，启动器是以`游戏实例`为单位启动游戏  
`游戏实例`相当于一个独立的游戏配置  
将Mod、配置、世界等储存在一个游戏文件夹  
使用多实例管理游戏可以将多个整合包放在一起，但又互不影响，但共享游戏资源文件和运行库，同时运行后可以不受其他游戏实例的干扰  

## 账户

ColorMC的启动游戏实例需要一个`账户`，账户可以是以下几种类型
- 离线账户
- 微软账户
- 统一通行证账户
- LittleSkin皮肤站账户
- 自建皮肤站账户

注意：使用离线账户来启动游戏时，至少登录一个正版账户

账户至少会有以下数据
- 用户名
- 用户UUID
- 账户类型
- 客户端UUID

## 启动器默认主页面

![](pic13.png)  

启动器主页面中间会显示所有目前存在的游戏实例  
右侧是菜单，点击按钮可以打开对应的窗口  
点击箭头可以让右侧菜单最小化

![](pic26.png)  

每一个图标代表一个游戏实例，图标下面是游戏实例的名字  
点击游戏实例可以选择游戏实例，点击右键可以呼出实例菜单  
![](pic14.png)  

## 账户窗口

添加游戏账户需要在主界面`点击头像`打开账户窗口  
![](pic5.png)  
![](pic6.png)

窗口打开后，点击右上角的`添加账户`可以开始新建账户  
![](pic7.png)

双击账户列表中的账户可以切换账户  
![](pic8.png)  

右键账户可以呼出菜单  
![](pic9.png)  

## 添加游戏实例

点击启动器主页面右侧的`添加实例`，可以打开新建实例窗口  
![](pic1.png)  

添加游戏实例有3种方式

- 从头新建实例  
![](pic2.png)  
从头新建实例很简单，只需要填写实例名字，选择版本等信息，最后点击右下角的`添加`按键即可添加  
也可以从在线的整合包来添加实例  
点击`在线搜索整合包`可以打开此窗口

- 从压缩包里导入实例  
![](pic3.png)  
从压缩包导入实例需要先选择压缩包，然后填写实例名字与选择压缩包类型，最后点击右下角的`导入压缩包`即可

- 从现有的文件夹导入实例
![](pic4.png)  
从现有的文件夹导入实例需要先选择路径，然后填写实例名字，选择需要导入的文件内容，最后点击`添加`即可  
由于添加后缺失版本信息，因此需要手动选择游戏版本

## 添加在线整合包

在添加实例的窗口内，点击添加整合包可以打开窗口
![](pic10.png)  
可以在上方的选择中筛选整合包等  
双击一个整合包可以打开版本选择  
![](pic11.png)  
再次双击可以开始下载整合包

在下载前若保持`添加实例窗口`开启  
整合包下载完成后会自动填入`实例名字`与`游戏分组`信息

## 启动游戏实例

在启动器主界面选择好需要启动的游戏实例  
![](pic12.png)  
选中时会有蓝色框进行包裹  
可以点击右边的`启动实例`按钮启动  
又或者双击需要启动的`游戏实例`

## 修改游戏实例

选择实例后，在启动器主页面点击`修改实例`按钮  
或右键游戏实例，选择`修改实例`可以打开窗口  

游戏实例设置主要有
- 版本设置  
设置游戏的版本，Mod加载器，整合包信息等
![](pic16.png)  
可以检测整合包更新  
![](pic46.png)  
![](pic47.png)  
- 启动参数  
设置游戏启动时使用的参数
![](pic27.png)  
- Mod列表  
查看游戏实例的Mod  
自动检测modid冲突
![](pic48.png)  
可以查看Mod的基础信息  
![](pic28.png)  
可以检测Mod依赖\更新等  
![](pic30.png)  
检测标记的Mod更新  
![](pic32.png)  
![](pic29.png)  
选择项目右键可以打开菜单  
![](pic31.png)  
- 地图列表  
查看游戏实例的地图  
![](pic33.png)  
选择世界后右键可以打开菜单  
![](pic49.png)  
- 资源包  
查看游戏实例的资源包  
![](pic34.png)
- 游戏截图  
查看游戏实例内的截图  
![](pic35.png)
- 服务器列表  
查看游戏实例的服务器信息  
![](pic36.png)
- 光影包  
查看游戏实例的光影包信息  
![](pic37.png)
- 结构文件  
查看游戏实例的结构文件，包括投影Mod的结构文件  
![](pic38.png)

## 游戏实例配置文件修改

打开游戏实例设置窗口后，在版本设置的最下面点击`修改配置文件`按钮  
![](pic50.png)  
或在地图列表内右键世界点击`修改配置`按钮可以打开窗口  
打开窗口后可以查看\修改配置文件  
在左上角的选择框可以选择配置文件  
过滤器会选出名字包含的文件  
![](pic17.png)  
内置有NBT修改器，若打开的是NBT格式文件，或地图文件，可以进行NBT修改  
![](pic18.png)  
![](pic51.png)  
NBT编辑器下，可以通过右键来打开菜单进行编辑  
![](pic52.png)  
地图编辑模式下，可以进行方块或者实体的查找  
![](pic53.png)  
修改完配置文件后需要点击保存修改或按下快捷键`Com + S`才会保存

## 游戏实例日志文件查看

打开游戏实例设置窗口后，在版本设置的最下面点击`查看运行日志`按钮  
![](pic54.png)  
或在主界面右键实例点击`运行日志`按钮可以打开窗口  
![](pic19.png)  
该页面会加载所有logs/下的日志文件，在上方选择后可以打开文件  
![](pic40.png)  
文本无法编辑，但是可以复制  

测试启动用于检测游戏启动时的日志信息

## 游戏实例导出

打开游戏实例设置窗口后，在版本设置的最下面点击`导出游戏实例`按钮  
![](pic55.png)  
打开后可以进行导出类型的选择
![](pic39.png)  
若为主流整合包，可以设置Mod在线下载  
![](pic56.png)  
文件选择可以将所需文件放进压缩包内  
![](pic57.png)  
文件在线下载可以选择文件设置下载路径  
![](pic58.png)  
选择完毕，并填写所需信息后即可开始导出  
![](pic59.png)  

## 启动器设置

在启动器主页面点击`启动器设置`按钮可以打开窗口  
![](pic60.png)  
启动器设置主要有
- 界面设置  
调节启动器界面显示等  
![](pic41.png)  
例如启动器的主题色，背景颜色  
启动器的字体，窗口透明方式等
- 网络设置  
调节启动器联网功能  
![](pic15.png)  
在文件下载过程中，不可修改代理设置
- 启动设置  
调节游戏启动参数等  
![](pic42.png)  
例如启动前，启动后运行  
游戏窗口大小等
- Java路径  
调节目前设置的Java  
![](pic43.png)
- 客户端定制  
给服主使用的定制功能  
![](pic44.png)  
可以自定义UI界面或开启自定义音乐
- 配置文件  
启动器配置文件  
![](pic45.png)  
- 关于  
启动器说明

## Live2D人物显示

在`启动器设置`的`界面设置`内，往下拖动有`Live2D人物设置`选项  
![](pic61.png)  
在使用Live2D人物模型显示之前，需要先安装[Core](https://www.live2d.com/download/cubism-sdk/download-native/)  
将下载好的压缩包解压后，复制`dll`或`so`文件到启动器二进制根目录下
![](pic62.png)  
注意：不同系统需要放的二进制文件不一样  
然后重启启动器  
再次打开设置页面找到`Live2D人物设置`，若能正确识别Core版本则安装成功  
然后就可以选择模型并加载  
模型只支持model3和moc3，不支持其他版本

在主界面显示人物后，可以点击人物进行互动，操作等  
![](pic24.png)  
右键可以呼出菜单  
![](pic25.png)  

## 客户端定制 

在`启动器设置`内选择`客户端定制`  
可以进行定制设置  
- 锁定启动实例 玩家只能启动某个游戏实例  
- 锁定登陆模型 玩家只能以某种方式进行登录
- 自定义UI 导入自定义UI界面
- 服务器同步 启动前同步游戏文件
- 自定义音乐 在启动器启动时循环播放音乐，支持网易云的音乐链接

自定义UI使用axaml格式，默认的模板为
```xml
<view:CustomPanelControl
    xmlns="https://github.com/avaloniaui"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:view="clr-namespace:ColorMC.Gui.UI.Controls.Custom"
    xmlns:views="clr-namespace:ColorMC.Gui.UI.Controls"
    xmlns:views1="clr-namespace:ColorMC.Gui.UI.Controls.Main"
    Title="自定义标题"
    mc:Ignorable="d">
    <Panel>
        <StackPanel
            Margin="0,0,5,0"
            HorizontalAlignment="Right"
            VerticalAlignment="Bottom">
            <Button
                Width="100"
                Height="25"
                Margin="5,0,0,5"
                Command="{Binding Launch}"
                Content="启动游戏" />
            <Button
                Width="100"
                Height="25"
                Margin="5,0,0,5"
                Command="{Binding Setting}"
                Content="启动器设置" />
            <Button
                Width="100"
                Height="25"
                Margin="5,0,0,5"
                Command="{Binding OpUrl}"
                CommandParameter="Https://www.baidu.com"
                Content="打开网页" />
            <Button
                Width="100"
                Height="25"
                Margin="5,0,0,5"
                Command="{Binding User}"
                Content="编辑账户" />
            <Button
                Width="100"
                Height="25"
                Margin="5,0,0,5"
                Command="{Binding Skin}"
                Content="查看皮肤" />
        </StackPanel>
        <Label
            Margin="10"
            HorizontalAlignment="Left"
            VerticalAlignment="Bottom"
            Background="#FFEEEEEE"
            Content="xxx服务器专用客户端"
            FontSize="20"
            Foreground="#FF000000" />
        <views:ServerMotdControl Margin="5" IPPort="{Binding Server}" />
        <views1:GameControl
            HorizontalAlignment="Center"
            VerticalAlignment="Center"
            DataContext="{Binding Game}" />
        <StackPanel
            Margin="10,80,10,10"
            HorizontalAlignment="Right"
            VerticalAlignment="Top"
            Orientation="Vertical">
            <Image
                Width="80"
                Height="80"
                Margin="10,0,10,0"
                HorizontalAlignment="Center"
                Source="{Binding Head}" />
            <Label
                Margin="0,5,0,5"
                HorizontalContentAlignment="Center"
                Content="{Binding UserName}" />
            <Label
                Margin="0,5,0,5"
                HorizontalContentAlignment="Center"
                Content="{Binding UserType}" />
        </StackPanel>
    </Panel>
</view:CustomPanelControl>
```
UI使用Avalonia的标准页面编写即可  
[AXAML](https://docs.avaloniaui.net/docs/next/basics/user-interface/introduction-to-xaml)  [UI控件](https://docs.avaloniaui.net/docs/next/basics/user-interface/controls/builtin-controls)

## 游戏实例添加资源

打开游戏实例设置窗口后，在Mod列表，地图列表等点击左侧的`添加`按钮  
![](pic64.png)  
或在主界面右键实例点击`添加资源`按钮可以打开窗口  
![](pic63.png)  
添加资源主要用于下载游戏资源，例如Mod，地图，材质包等  
![](pic20.png)  
在上方可以选择来筛选内容  
![](pic65.png)  
双击后打开版本列表，双击版本可以开始下载资源  
![](pic66.png)  

## 游戏实例Mod列表

打开游戏实例设置窗口后，在Mod列表可以进行游戏实例的Mod操作
![](pic28.png)  
双击Mod项目可以`启用/禁用`Mod  
![](pic21.png)  
上方的按钮功能为
- 导入Mod 从现有文件添加到游戏实例中
- 添加Mod 从网上下载资源
- 刷新 刷新列表
- 检测Mod更新 检测有标记的Mod是否有新版本
- 标记Mod 用于标记Mod所在的下载源项目ID与版本等
- 依赖检测 检测Mod的前置是否齐全

可以拖拽`jar文件`到列表中来添加Mod  
按住`Shift键`可以多选Mod  
右键可以打开菜单，进行操作  
![](pic22.png)  

## 游戏实例服务器包与同步

待补充