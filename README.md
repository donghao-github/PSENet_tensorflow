# PSENet_tensorflow

PSENet的tensorflow复原代码地址：https://github.com/liuheng92/tensorflow_PSENet

参考CSDN博客：https://blog.csdn.net/liu506039293/article/details/102835275

训练好的模型model 的链接: https://pan.baidu.com/s/1qft1hxVAQBW8ld1D0u4Khw 提取码: bynv



    关于代码复原，CSDN的这篇博客写的很实在，但和github上的一样，有些地方模糊，对小白上手有些障碍，现在记录以下：

1、如果windows系统跑不通，请切换linux系统。我一开始用的windows，在pse文件夹的init文件中始终报错，百度查找无果，果断切换linux，最终可以！



2、本人环境为：ubuntu、python3.7.5、tensorflow 1.13.1、gcc 9.2。 github上源码使用的是python2，如果使用python3请按照上面的CSDN博客更改。共3处,分别在3个文件中：Makefile、utils_tool.py、eval.py。 （若tensorflow1.14.0不行，请用1.13.1试试）



3、从github上下载完源码之后，还要下载model文件及测试集ICDAR2015。对于model文件，github上给出了百度网盘地址，但是这个文件夹中缺少一个文件，需要自己创建，详细内容见CSDN； 测试集网站：https://rrc.cvc.uab.es/   （注意，需要注册才可下载）或者链接: https://pan.baidu.com/s/1nFFd_CtYWsdw-zXWKaoNjg 提取码: dby7



4、将下载model的文件夹放在项目根目录下；同时在根目录下创建data文件夹，在data内创建test_images文件夹，测试图片放在这里面；在根目录下再创建一个results文件夹，用来存放运行结果。



5、在eval.py 文件开头，补充完整你的model地址和测试集地址，如下：



test_data_path:测试图片地址

checkpoint_path:为model文件夹地址，即模型地址

output_dir:为输入结果地址



6、做完上述修改之后，在终端直接运行  python eval.py 命令即可运行。
