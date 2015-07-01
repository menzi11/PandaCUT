# PandaCUT 熊猫切图

一个photoshop CC的javascript脚本,可以帮助任何被PS切图折磨的人
进行自动的,批量的,跨越图层的切图.

![image](https://github.com/menzi11/PandaCUT/blob/master/thePandaWhoCUT.png)

## 为什么需要一个新的切图工具?

世界上有不少切图工具,但大部分是基于图层的切图,但事实上,我们经常会遇到
跨越多个图层的切图需求,例如从后向前ABC三个图层,PandaCUT可以实现先隐藏B图层,
打开A和C图层导出,再隐藏A图层,打开C和B图层导出.如此批量导出图片,几乎是全自动化!
你还可以设置无论怎么导出都不隐藏的图层,例如背景图层,曲线/亮度对比度调整图层.

## 那么,如何使用呢?

首先，我们先需要创建一个组，把这个组的名字改成“@PandaCUT_MASKS”，然后我们可以把需要截图的区域用一个矩形来覆盖，即创建一个蒙版，并给这个蒙版起一个已@开头的名字（如@test），这个名字将作为标志用来检索其他图层的名字里是否包含这个标志，来确定在截这个区域的时候哪个图层需要显示，蒙版的大小和位置则用来确定截图的位置，蒙版的其他属性则不重要。

然后给需要被某一个蒙版截图的图层或组的名字加上蒙版标志，每一个图层或组可以加多个标志，并且这些标志可以加到名字里的任何位置。

所有没加过蒙版标志或特殊标志的图层或组，在截图时则一定会被隐藏。

特殊标志“@PandaCUT_NEVERHIDE”
可以给图层或组的名字里加上这个标志，这样无论在截哪一个蒙版区域的时候，这个图层或组都会显示出来。

在photoshop里顺序点击 文件->脚本->浏览，然后选择你本机PandaCUT.jsx的路径，运行后会弹出文件夹选择框，选择一个你用来保存导出图片的文件夹，然后等程序提示运行完成就可以了。

导出图片的名字将和蒙版名字一样，但是会自动去掉@字符，格式则为png。

Example
打开TestForPandaCUT.psd，可以看到有4个蒙版分别是:@green,@black,@yellow,@red; 运行脚本最终会得到4个png,这4个png分别和4个蒙版大小宽高相同，名字相同（除去@）。
可以看到每个截图都只有自己名字的颜色和紫色，因为紫色的图层都是@PandaCUT_NEVERHIDE的所以每个截图都会有紫色。

##English Doc ?

I will do it futrue.

------------

如果有任何意见或建议或使用不明之处,可以提issues,或者可发我的邮箱:
jiangnanxing@threebodytech.com

另外我们在北京招聘热爱金属材质和拟真风格的设计师,如果你有兴趣,也可向这个邮箱发邮件.
或者您有朋友,同学,学生,徒弟亲戚是热爱金属材质和拟真风格的设计师,想找工作,也可以联系
我们.
