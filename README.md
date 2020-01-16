# [RxTool](https://tamsiree.com/RxTool/)

[![tamsiree.com](https://img.shields.io/badge/%E6%8A%80%E6%9C%AF%E5%8D%9A%E5%AE%A2-Tamsiree-brightgreen.svg)](https://tamsiree.com/)  [![Stars](https://badgen.net/github/stars/tamsiree/RxTool)](https://ghbtns.com/github-btn.html?user=tamsiree&repo=rxtool&type=star)  [![RxTool](https://jitpack.io/v/tamsiree/RxTool.svg)](https://jitpack.io/#tamsiree/RxTool)  

[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)  [![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)  [![](https://img.shields.io/badge/platform-android-brightgreen.svg)](https://developer.android.com/index.html)  [![API](https://img.shields.io/badge/API-17%2B-blue.svg?style=flat)](https://android-arsenal.com/api?level=17)  [![Gradle-5.4.1](https://img.shields.io/badge/Gradle-5.4.1-brightgreen.svg)](https://img.shields.io/badge/Gradle-5.4.1-brightgreen.svg)  
  
![image](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/DeskTop/miku.png)

	所谓：工欲善其事必先利其器！
	`RxTool` 是 `Android` 开发过程经常需要用到各式各样的工具类集合，虽然大部分只需谷歌/百度一下就能找到。
	但是有时候急需使用却苦苦搜寻不到，于是整理了自己平常用到的工具类，以便以后的使用。


---

# 我的运行环境
> Android Studio 3.5.2  
> Build #AI-191.8026.42.35.5977832, built on October 31, 2019  
> JRE: 1.8.0_202-release-1483-b49-5587405 amd64  
> JVM: OpenJDK 64-Bit Server VM by JetBrains s.r.o  
> Linux 5.3.11-1-MANJARO  
>
> targetSdkVersion 28  
> [gradle-wrapper.properties文件内] distributionUrl 5.4.1  
> [build.gradle文件内] gradle 3.5.2

---

# 如何使用它


## Step 1.先在 build.gradle(Project:XXXX) 的 repositories 添加:

```gradle
allprojects {
    repositories {
        maven { url "https://jitpack.io" }
    }
}
```

## Step 2.然后在 build.gradle(Module:app) 的 dependencies 添加:
```gradle
dependencies {
  //基础工具库
  implementation "com.github.tamsiree.RxTool:RxKit:v2.4.1"
  //UI库
  implementation "com.github.tamsiree.RxTool:RxUI:v2.4.1"
  //(依赖RxUI库时，需要额外依赖 cardview 库)
      implementation 'com.android.support:cardview-v7:27.1.1'
  //相机库
  implementation "com.github.tamsiree.RxTool:RxCamera:v2.4.1"
  //功能库（Zxing扫描与生成二维码条形码 支付宝 微信）
  implementation "com.github.tamsiree.RxTool:RxFeature:v2.4.1"
  //ArcGis For Android工具库（API：100.1以上版本）
  implementation "com.github.tamsiree.RxTool:RxArcGisKit:v2.4.1"
}
```

## Step 3.在Application中初始化 
(注：v2.0.0以后版本是分多模块的版本)
```java
RxTool.init(this);
```


# API使用文档

## 可以参考文档来调用相对应的API，欢迎指教
- [**[点我看文档]**](https://tamsiree.com/TechnicalResearch/Android/RxTool/Wiki/RxTool-Wiki)
- [**[点我看文档]**](https://tamsiree.github.io/TechnicalResearch/Android/RxTool/Wiki/RxTool-Wiki)
- 备选 [点我看文档](https://github.com/tamsiree/RxTool/wiki/RxTool-Wiki)



# 更新日志
> 因为自己用的关系，更新的频率可能有点快

|  VERSION  |  Description  |
| :-------: | ------------- |
|   2.4.1   | 完善 RxArcGisKit 模块  |
|   **2.4.0**   | **`全面升级到 Android X`**:<br>修复 RxToast 在 Android 9 上,连点只弹出一次的问题<br>修复 二维码扫描框的焦点偏离 问题<br>添加 生成二维码LOGO 功能<br>添加 RxQRCode 的空白边界设置方法<br>更新若干工具类  |
|   2.3.9   | 完善 RxFeature 模块  |
|   2.3.8   | 优化 RxFeature 模块  |
|   2.3.7   | 更新 RxFeature 模块  |
|   2.3.6   | 更新 RxFeature 模块，优化 RxUI 模块  |
|   2.3.5   | 优化 RxDataTool 模块  |
|   2.3.4   | 完善 RxKit 模块  |
|   2.3.3   | 更新 RxDataTool 模块  |
|   2.3.2   | 优化 RxKit 模块 |
|   2.3.1   | 更新 RxUI 模块的 WaveSideBarView |
|   2.3.0   | 优化 RxCamera 模块 |
|   2.2.9   | 更新 RxUI 模块 |
|   2.2.8   | 修复配置文件 |
|   2.2.7   | 新增适配 dimens 文件<br>适配平板等各种屏幕大小的设备 |
|   2.2.6   | 更新 RxMapScaleView 及资源文件 |
|   2.2.5   | 更新 RxCameraView <br>修复部分设备不支持16:9分辨率崩溃问题 |
|   2.2.4   | 更新数据处理工具 |
|   2.2.3   | 调整相机分辨率大小 |
|   2.2.2   | 整理配置文件 |
|   2.2.1   | 增加若干 Shape 资源 |
|   2.2.0   | 增加 ArcGis 坐标系换算方法(投影坐标系、GPS坐标系、设备屏幕坐标系) |
|   2.1.9   | 更新 RxAutoImageView 的屏幕适配大小 |
|   2.1.8   | 更新 RxCameraView 的参数与算法 |
|   2.1.7   | 新增 ArcGis 关于地图精准定位与行程轨迹的实现方法 |
|   2.1.6   | 更新 zip4j 压缩算法 |
|   2.1.5   | RxLocationTool 新增 GPS坐标转百度坐标 方法 |
|   2.1.4   | 新增 ArcGis 若干工具 |
|   2.1.3   | 更新 Gps 移动定位算法 |
|   2.1.2   | 优化 ArcGis 工具类 |
|   2.1.1   | 更新 GPS 定位工具类<br>更新配置文件 |
|   2.1.0   | 更新绘制文字与图片工具 |
|   2.0.9   | 调整安卓各版本下的相机适配 |
|   2.0.8   | 优化相机控件模块 |
|   2.0.7   | 新增相机控件模块 |
|   2.0.6   | 更新 ArcGis 工具<br>更新颜色资源 |
|   2.0.5   | 新增 ArcGis 地图比例尺控件<br>相机工具的优化 |
|   2.0.4   | 降低模块之间的耦合性<br>ArcGisMap 工具的优化 |
|   2.0.3   | 更新扫描二维码 Demo<br>更新日期选择 Dialog |
|   2.0.2   | 更新支付宝 SDK，新增支付宝支付 DEMO <br>更新相机工具 |
|   2.0.1   | 新增(高德/百度)地图导航工具<br>新增 ArcGis 工具类 |
| __2.0.0__ | 重构成多模块 |

# Demo介绍

## RxPhotoTool 操作 UCrop 裁剪图片

| 展示头像 | 选择头像 | 裁剪头像 |
| :----------: | :-------------: | :-------------: |
| ![展示头像](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_1.jpg) | ![选择头像](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_8.jpg) | ![裁剪头像](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_9.jpg) |

## 二维码与条形码的扫描与生成

| 扫描二维码 | 生成二维码 | 扫描条形码 |
| ---------- | ------------- | ------------- |
| ![扫描二维码](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_2.jpg) | ![生成二维码](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_3.jpg) | ![扫描条形码](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_10.jpg) |


## 常用的Dialog展示

| 确认弹窗 | 确认取消弹窗 | 输入框弹窗 |
| :----------: | :-------------: | :-------------: |
| ![确认弹窗](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_5.png) | ![确认取消弹窗](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_6.png) | ![输入框弹窗](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_7.png) |
| 选择日期弹窗 | 形状加载弹窗 | Acfun加载弹窗 |
| ![选择日期弹窗](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_11.png) | ![形状加载弹窗](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_12.png) | ![Acfun加载弹窗](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_13.png) |

## 其他功能展示

| WebView的封装（可播放视频） | RxTextTool操作Demo | RxToast的展示使用 |
| :----------: | :-------------: | :-------------:|
| ![WebView的封装（可播放视频）](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_14.png) | ![RxTextTool操作Demo](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_15.png) | ![RxToast的展示使用](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_18.png)|
| 进度条的艺术 | 网速控件 | 联系人侧边栏快速导航 |
| ![进度条的艺术](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_16.png) | ![网速控件](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_17.png) | ![联系人侧边栏快速导航](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_22.png)|
| 图片的缩放艺术 | 蛛网控件 | 仿斗鱼验证码控件 |
| ![图片的缩放艺术](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_19.png) | ![蛛网控件](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_20.png) | ![仿斗鱼验证码控件](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Picture/RxTool/screenshot_21.png)|

## DEMO 与 打赏

| Demo | 微信赞助 | 支付宝赞助 |
| :----------: | :----------: | :----------: |
| 快下载Demo运行试试吧<br>只展示了部分UI功能<br>功能性功能去源码里探索吧|  如果你帮助到了你<br>可以点右上角"Star"支持一下<br> 谢谢！^_^<br>你也还可以扫描下面的二维码打赏鼓励一下~ <br>请作者喝一杯咖啡。| 如果在捐赠留言中备注名称<br>将会被记录到列表中~ <br>如果你也是github开源作者<br>捐赠时可以留下github项目地址或者个人主页地址<br>链接将会被添加到列表中起到互相推广的作用 |
| ![RxTool](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Function/qrcode_apk.png) |  ![微信](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Function/pay_qr_code.jpg) |   ![支付宝](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Function/qrcode_alipay.jpg) |
|扫描二维码 <br> 或者 <br> [点击下载](https://cdn.jsdelivr.net/gh/Tamsiree/Assets@master/Apk/RxTool.apk) |[捐赠名单](https://tamsiree.com/TechnicalResearch/Android/RxTool/Contributor)<br>备选[捐赠名单](https://tamsiree.com/RxTool/Contributors) | 闲聊群 <br><br>  ![技术的深度探索与论证](https://img.shields.io/badge/QQ%E7%BE%A4-435644020-brightgreen.svg) <br>[点击入群](https://shang.qq.com/wpa/qunwpa?idkey=a14a650c50413f43d5bb0399f5b6617a2cd09866ae09c5a1d7f3e0ba33962bae)<br>
