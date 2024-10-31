# Moonlight Android

[Moonlight for Android](https://moonlight-stream.ORG) 是一个开源客户端，用于连接NVIDIA GameStream或[Sunshine](https://github.com/LizardByte/Sunshine)。

Moonlight for Android可以让您将Windows PC上的完整游戏集合流式传输到Android设备上，无论是在家中还是通过互联网。

Moonlight还有[PC客户端](https://github.com/moonlight-stream/moonlight-qt)和[iOS/tvOS客户端](https://github.com/moonlight-stream/moonlight-ios)。

## 关于Attect的修改版

您看到此处说明则表示您处于Attect修改的Moonlight分支，如果您需要原版信息及支持，请前往[官方仓库](https://github.com/moonlight-stream/moonlight-android)。

修改动机来自使用原版时发现一些操作无法进行或及其繁琐。

以下为修改说明：

### 改动的部分效果演示

[点击此处查看演示视频](https://www.bilibili.com/video/BV1Ys421T784/)

### 代码侵入

增加的功能实现将主要在library-attect实现，原代码仅有极少处的修改，不修改布局结构，对合并友好。

### 新增部分的语言支持

仅支持：`英语`、`简体中文`

### 悬浮按钮及屏幕覆盖菜单

开始串流后，您将在屏幕左上角看到一个Moonlight图标样式的悬浮按钮，此按钮可以拖动以避免遮挡关键画面。点击按钮后会显示菜单，分别有：

1. ESC：模拟按一次键盘的ESC键，用于在一些游戏呼出菜单。
2. 开始菜单：便捷的启动其它程序，或者暂时的弹出游戏。
3. 系统菜单：便捷的打开系统管理相关的程序。
4. 鼠标中键：用于终端操作，或者部分游戏使用中键交互。
5. 屏幕手柄：实时切换屏幕手柄的显示
6. 触摸屏模式：将触摸操作直接传递给PC，不再模拟触摸板或者鼠标位置。
7. 触摸板模式：模拟触摸板或者鼠标位置。
8. 软键盘：唤出本机的软键盘。
9. 关闭程序：即Alt+F4。
10. 截图：短按进入选取截图（Win11）或将所有显示器画面截图到剪贴板，长按则立即保存当前所有显示器的屏幕截图到文件。
11. 任务管理器：便捷的打开任务管理器，不怕游戏卡住了。
12. 资源管理器：随时随地打开学习资料。
13. 复制、剪切、粘贴、全选：为输入和文件管理提供便捷操作。
14. 显示桌面：完全弹出游戏。
15. 任务视图：在多个程序中键快速切换。
16. 新建桌面：Win7及其它系统不支持，Win10/11新建一个虚拟桌面。
17. 删除桌面：Win7及其它系统不支持，Win10/11删除当前虚拟桌面，窗口将被左移一个卓main。
18. 上个桌面：Win7及其它系统不支持，Win10/11则向左切换到上一个虚拟桌面。
19. 下个桌面：Win7及其它系统不支持，Win10/11则向右切换到下一个虚拟桌面。
20. N卡菜单：唤出Nvidia GeForce Experience/Nvidia App的游戏内覆盖菜单
21. 屏幕快照：基于ShadowPlay的屏幕截图
22. 照片模式：N卡的拍照模式
23. 游戏滤镜：N卡的游戏画面滤镜
24. 即时重放：ShadowPlay保存即时重放（注意需要先从菜单中打开即时重放功能）
25. 录制：基于ShadowPlay的屏幕录制，再按一次保存录像

### UI修改

1. 修改了游戏列表界面的图片缩放规则，游戏封面将被裁切居中填充，不会再拉伸变形了。

### BUG修改

1. 修正了翻译`KeyEvent.KEYCODE_SYSRQ`错误的问题。

## 构建
* 安装Android Studio和Android NDK
* 在moonlight-android/目录下运行`git submodule update --init --recursive`
* 在moonlight-android/创建名为`local.properties`的文件。在`local.properties`文件中添加一个`ndk.dir=`属性，并将其设置为您的NDK目录。
* 使用Android Studio或gradle构建APK

## 作者
* [Cameron Gutman](https://github.com/cgutman)
* [Diego Waxemberg](https://github.com/dwaxemberg)
* [Aaron Neyer](https://github.com/Aaronneyer)
* [Andrew Hennessy](https://github.com/yetanothername)
* [Attect](https://github.com/Attect)

Moonlight是[凯斯西储大学](http://case.edu)的学生的作品，最初作为[MHacks](http://mhacks.org)项目开始。