# 开发中遇到的问题记录
## 1、
报错：Failed to set () user defined inspected property on (UIButton)
![截图](https://raw.githubusercontent.com/huxq-coder/resource/master/image/view/view_tips1.png) 
查询xib中UIbutton的右侧工具栏中的属性中是否有不合适的属性设置。链接： [Stack Overflow链接](https://stackoverflow.com/questions/43032924/failed-to-set-user-defined-inspected-property-on-uibutton/44101008)
## 2、UITextView 计算高度
根据textview的内容使用boundingRectWithSize或者sizeThatFits方法计算高度时不准确，因为textview的内容显示有内边距，textView.textContainerInset = (top = 8, left = 0, bottom = 8, right = 0)，所以计算出来的高度需要再 +16；
##  3、支付宝SDK告警信息
warning: (x86_64) /Users/shanjia.gxd/work_space/tmp/ios-msdk-git/AlipaySDK4Standard/AlipaySDK/Library/UTDID.framework/UTDID(UTDIDAES.o) unable to open object file: No such file or directory
warning: (x86_64) /Users/shanjia.gxd/work_space/tmp/ios-msdk-git/AlipaySDK4Standard/AlipaySDK/Library/UTDID.framework/UTDID(UTDIDBaseUtils.o) unable to open object file: No such file or directory
####解决方法
1) Go to Build Settings -> Build Options -> Debug Information Format
2) Change the Debug setting from “DWARF with dSYM File” to “DWARF”
3) Leave the Release setting at “DWARF with dSYM File”
