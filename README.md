# onscripter-plus_fork
[WIP] My Onscripter Plus PC port, running in Xubuntu 20.04 without Android

## References  
* https://github.com/matthewn4444/onscripter-engine-android/tree/master/src/main/cpp/onscripter  

## TODO
* Remove debug printf output
* Remove gcc -funsigned-char, make ScriptDecoder.cpp more portable, see ChineseDecoder::isChinese  
* How to change font size like Onscripter Plus Android version   

## Weibo record  
```
我把onscripter-plus的源代码单独抽出来魔改，
编译成命令行模式运行gbk中文用例成功，
有时间放到gh上。onscripter-plus的亮点是
可以自动检测字符集（例如gbk和sjis都可以正确显示字体），
并且可以动态修改字体大小（在下一次显示字符时变大），
暂时不管字体大小问题，我只是把自动检测字符
这个功能用xubuntu 20跑通了。
不过检测代码有个小bug，onscripter-plus的
源代码没有明确使用unsigned char，
所以会导致编译成功但运行会出问题（如果是用arm gcc编译
则没有这个问题），所以我加上一个编译开关-funsigned-char
来暂时规避这个bug。总体来说onscripter-plus还是很好用的
```

