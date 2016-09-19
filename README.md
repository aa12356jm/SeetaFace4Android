#SeetaFace4Android

[SeetaFaceEngine](https://github.com/seetaface/SeetaFaceEngine)是山世光老师新创立的中科视拓(Seeta)旗下最新开源的人脸识别全流程解决方案，但是其检测和对齐模块并没有相应的工程，本项目是其对应的windows下VS2013工程。

先来看下效果还是很不错的：

![results](results/4.jpg)

本工程构造了SeetaFace在windows下VS2013的解决方案，此外，相对原工程为了方便在anroid端移植做了如下改进：

1.使用单例模式封装检测和对齐代码，使得代码调用逻辑更清晰；

2.使用MATH_UTIL_BY_SIMD宏区分SSE指令，以增强跨平台的能力，目前改写了util下的math_func.h文件，但还有部分函数函数尚未完成转换，因此anroid版本尚未放出，敬请期待；

3.从文件夹下读取测试图片，输出检测和对齐的结果。

完整工程请参见[SeetaFaceEngine-windows.rar](SeetaFaceEngine-windows.rar)