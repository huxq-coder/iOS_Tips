# 开发中遇到到的问题记录
## 1、
报错：Failed to set () user defined inspected property on (UIButton)
![截图](https://raw.githubusercontent.com/huxq-coder/resource/master/image/view/view_tips1.png)
查询xib中UIbutton的右侧工具栏中的属性中是否有不合适的属性设置。链接： [https://stackoverflow.com/questions/43032924/failed-to-set-user-defined-inspected-property-on-uibutton/44101008](Stack Overflow链接)
## 2、UITextView 计算高度
根据textview的内容使用boundingRectWithSize或者sizeThatFits方法计算高度时不准确，因为textview的内容显示有内边距，textView.textContainerInset = (top = 8, left = 0, bottom = 8, right = 0)，所以计算出来的高度需要再 +16；
