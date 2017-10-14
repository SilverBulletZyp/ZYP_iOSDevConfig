# ZYP_iOSDevConfig

iOS开发常用配置内容


## Podfile


* 替换工程名`Project`


* 安装或更新


```vim
pod install
pod update
```


## Pch


* 替换`Project`内容并导入需要的`pod`


* 添加本地目录


```vim
$(SRCROOT)/Project/Project.pch
```


## .gitignore


* 按需注释或解注常用文件


```
## Obj-C/Swift specific
# *.hmap
# *.ipa
# *.dSYM.zip
# *.dSYM

## Various settings
# xcuserdata/
# _Store
# *.xcscheme
# *.xcuserdatad
# .idea/

## CocoaPods
# Pods/

## Carthage
# Carthage/Build
```



## common pod use


* [Myself HomeView instruction](https://github.com/SilverBulletZyp/ZYP_HomeViewController)


* [Masonry]()


```
//#define MAS_SHORTHAND
//#define MAS_SHORTHAND_GLOBALS
#import "Masonry.h"
```

* [iConsole](https://github.com/nicklockwood/iConsole)


```objective-c
// AppDelegate.h - 同时添加 iConsoleDelegate
@property (strong, nonatomic) iConsoleWindow *window;
// didFinishLaunchingWithOptions
_window = [[iConsoleWindow alloc] initWithFrame:[[UIScreen mainScreen] bounds]];
[iConsole sharedConsole].delegate = self;
[iConsole sharedConsole].logSubmissionEmail = @"xxx@126.com";
// 协议方法
- (void)handleConsoleCommand:(NSString *)command
{
  if ([command isEqualToString:@"version"])
   {
         [iConsole info:@"%@ version %@",
         [[NSBundle mainBundle] objectForInfoDictionaryKey:@"CFBundleName"],
         [[NSBundle mainBundle] objectForInfoDictionaryKey:@"CFBundleVersion"]];
    }
    else
    {
         [iConsole error:@"unrecognised command, try 'version' instead"];
    }
}
// import
#import "iConsole.h"
// 主动调用
[iConsole show];
// 三跟手指由下往上滑动. 模拟器两根手指, 默认启动
[iConsole sharedConsole].simulatorTouchesToShow = YES;  
[iConsole sharedConsole].deviceTouchesToShow = YES;
// 摇动手机启动 默认禁用
[iConsole sharedConsole].deviceShakeToShow = YES;
// [iConsole info:@"记录"];
```

