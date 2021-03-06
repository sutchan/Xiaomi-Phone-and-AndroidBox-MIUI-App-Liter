//用CMD连接上手机，无线连接用IP形式连接，数据线连接可跳过此步。

adb connect 192.168.10.250:5555		// 连接手机

adb devices		//查看可连接设备

adb shell pm list package	//查看已安装app


//=================================
// 可精简app清单 Begin
//=================================

//停用广告模块

adb shell pm uninstall --user 0 com.miui.systemAdSolution

adb shell pm uninstall --user 0 com.xiaomi.ab

adb shell pm uninstall --user 0 com.miui.analytics

//搜狗输入法

adb shell pm uninstall --user 0 com.sohu.inputmethod.sogou.xiaomi

//百度输入法

adb shell pm uninstall --user 0 com.baidu.input_mi

adb shell pm uninstall --user 0 com.baidu.duersdk.opensdk

//安卓系统自带app

adb shell pm uninstall --user 0 com.android.dreams.basic

adb shell pm uninstall --user 0 com.android.dreams.phototable

adb shell pm uninstall --user 0 com.android.musicfx

adb shell pm uninstall --user 0 com.android.htmlviewer

//杜比音效

adb shell pm uninstall --user 0 com.atmos

adb shell pm uninstall --user 0 com.atmos.daxappUI

//自带几种配色主题

adb shell pm uninstall --user 0 com.android.theme.color.purple

adb shell pm uninstall --user 0 com.android.theme.color.orchid

adb shell pm uninstall --user 0 com.android.theme.color.cinnamon

//MTK 自带app

adb shell pm uninstall --user 0 com.mediatek.floatmenu

adb shell pm uninstall --user 0 com.mediatek.mdmlsample

adb shell pm uninstall --user 0 com.mediatek.mtklogger

adb shell pm uninstall --user 0 com.mediatek.providers.drm

//小米自带 app

adb shell pm uninstall --user 0 com.mi.dlabs.vr

adb shell pm uninstall --user 0 com.miui.translation.youdao

adb shell pm uninstall --user 0 com.miui.whetstone

adb shell pm uninstall --user 0 com.miui.wmsvc

//用户手册

adb shell pm uninstall --user 0 com.miui.userguide

//时尚画报
adb shell pm uninstall --user 0 com.mfashiongallery.emag

//多看阅读

adb shell pm uninstall --user 0 com.duokan.reader

//点击助手

adb shell pm uninstall --user 0 com.miui.touchassistant

//用户反馈

adb shell pm uninstall --user 0 com.miui.bugreport

//游戏中心

adb shell pm uninstall --user 0 com.xiaomi.gamecenter

adb shell pm uninstall --user 0 com.xiaomi.gamecenter.sdk.service

//=================================
// 可精简app清单 End
//=================================


//以下为adb常用命令，仅供备用，不用执行。

adb shell pm list packages -[option] 命令查看已经安装的应用，列出包名，后面加不同的后缀输出不同信息。

adb shell pm list packages     ####查看当前连接设备或者虚拟机的所有包

adb shell pm list packages -d    #####只输出禁用的包。

adb shell pm list packages -e    #####只输出启用的包。

adb shell pm list packages -s    #####只输出系统的包。

adb shell pm list packages -i   #####只输出包和安装信息（安装来源）。

adb shell pm list packages -u   #####只输出包和未安装包信息（安装来源）。

adb shell pm list packages -i   #####只输出包和安装信息（安装来源）。

adb shell pm list packages -f   #####输出包和包相关联的文件

adb shell pm list packages -3   #####输出所有第三方包。

adb shell pm list packages -[option] "sina"   #####按照要求搜索包。
