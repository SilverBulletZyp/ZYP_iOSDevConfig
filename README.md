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



## Myself common

* [HomeView instruction](https://github.com/SilverBulletZyp/ZYP_HomeViewController)


