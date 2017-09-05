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



* 添加本地目录


```vim
$(SRCROOT)/Project/Project.pch
```


* 替换`Project`内容并导入需要的`pod`

