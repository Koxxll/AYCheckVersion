# AYCheckVersion

[![LICENSE](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/AYJk/AYPageControl/blob/master/License)&nbsp;
[![SUPPORT](https://img.shields.io/badge/support-iOS%207%2B%20-blue.svg)](https://en.wikipedia.org/wiki/IOS_7)&nbsp;
![CocoaPods Version](https://img.shields.io/badge/pod-v1.0.0-brightgreen.svg)
[![BLOG](https://img.shields.io/badge/blog-ayjkdev.top-orange.svg)](http://ayjkdev.top/)&nbsp;

我的博客中有详尽的实现过程和相关说明：
[iOS利用iTunesLookup检查更新](http://ayjkdev.top/2016/04/06/update-in-app-with-itunes-lookup/)
[中文介绍](https://github.com/AYJk/AYCheckVersion#中文介绍)

This is a utility class to check version from AppStore. 

![两个按钮情况](http://7xrofo.com1.z0.glb.clouddn.com/Simulator%20Screen%20Shot%202016%E5%B9%B44%E6%9C%887%E6%97%A5%20%E4%B8%8B%E5%8D%8811.24.14.png)        ![三个按钮情况](http://7xrofo.com1.z0.glb.clouddn.com/Simulator%20Screen%20Shot%202016%E5%B9%B44%E6%9C%887%E6%97%A5%20%E4%B8%8B%E5%8D%8811.25.06.png)

# Installtion
The preferred way of installtion is via [CocoaPods](http://cocoapods.org/)

```ruby
pod 'AYCheckVersion'
```

and run `pod install` or `pod update`. It will install the most recent version of AYCheckVersion.

After that import \<AYCheckVersion/AYCheckVersion.h\>.

Use AYCheckVersion

# Usage

```objc
AYCheckManager *checkManger = [AYCheckManager sharedCheckManager];
[checkManger checkVersion];
```
start check version with default param.

```objc
- (void)checkVersion;
```

start check version with AlertTitle,NextTimeTitle,ConfimTitle.

```objc
- (void)checkVersionWithAlertTitle:(NSString *)alertTitle nextTimeTitle:(NSString *)nextTimeTitle confimTitle:(NSString *)confimTitle;
```

start check version with AlertTitle,NextTimeTitle,ConfimTitle,skipVersionTitle.

```objc
- (void)checkVersionWithAlertTitle:(NSString *)alertTitle nextTimeTitle:(NSString *)nextTimeTitle confimTitle:(NSString *)confimTitle skipVersionTitle:(NSString *)skipVersionTitle;
```

If you want open AppStore inside your App, set `openAPPStoreInsideAPP`

```objc
checkManger.openAPPStoreInsideAPP = YES;
```
If you can't get the update info of your App. Set countryAbbreviation of the sale area. like `countryAbbreviation = @"cn"`,`countryAbbreviation = @"us"`.General, you don't need to set this property

```objc
checkManger.countryAbbreviation = @"cn";
```

set `debugEnable` to print the info in Debug arae

```objc
checkManger.debugEnable = YES;
```

# Changelog

v 1.0.1 add debug function, print the info in Debug arae

v 1.0.0 first version

# Licence
AYCheckVersion is provided under the MIT license. See LICENSE file for details.	

=================
# 中文介绍

这是一个从AppStore检测最新版本的工具类。

# 安装

推荐使用[CocoaPods](http://cocoapods.org/)进行安装。

```ruby
pod 'AYCheckVersion'
```

然后输入 `pod install` or `pod update`。将会安装最新版本的AYCheckVersion。

最后导入头文件\<AYCheckVersion/AYCheckVersion.h\>

# 用法

```objc
AYCheckManager *checkManger = [AYCheckManager sharedCheckManager];
[checkManger checkVersion];
```

使用默认属性进行版本的检测。

```objc
- (void)checkVersion;
```

自定义警示框的标题，下次提示的标题，立即更新的标题。

```objc
- (void)checkVersionWithAlertTitle:(NSString *)alertTitle nextTimeTitle:(NSString *)nextTimeTitle confimTitle:(NSString *)confimTitle;
```

自定义警示框的标题，下次提示的标题，立即更新的标题，跳过该版本的标题。

```objc
- (void)checkVersionWithAlertTitle:(NSString *)alertTitle nextTimeTitle:(NSString *)nextTimeTitle confimTitle:(NSString *)confimTitle skipVersionTitle:(NSString *)skipVersionTitle;
```

如果你想在当前应用中以模态视图的形式打开AppStore，请设置`openAPPStoreInsideAPP`，默认从应用跳转出去到AppStore。

```objc
checkManger.openAPPStoreInsideAPP = YES;
```

如果你无法检测到你的App的最新版。请设置你应用的销售地区，如：`countryAbbreviation = @"cn"`,`countryAbbreviation = @"us"`。通常情况下，你不需要设置这个属性。

```objc
checkManger.countryAbbreviation = @"cn";
```

设置`debugEnable`来输出更新信息

```objc
checkManger.debugEnable = YES;
```

# 版本更新

v 1.0.1 添加Debug功能，输出当前更新信息

v 1.0.0 首次提交

# 许可证

AYCheckVersion 使用 MIT 许可证，详情见 LICENSE 文件。	