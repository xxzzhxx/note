# PyTorch

在官网选择所建立的模式可以给你指令进行下载

pip 指令将pip3改为pip就可以在conda中安装了

## 经卷积后的矩阵尺寸大小计算公式

N=((W-F+2P)/S)+1

- 输入图片大小W*W
- Filter大小F*F
- 步长S
- padding的像素数P（一般为0）

如input（3，32，32）output（16，28，28）

## Pytorch Tensor的通道排序

[batch,channel,height,width]

# code

loss.py中CrossEntropyloss中包含logSoftmax

## 为什么每计算一个batch，就需要调用一次optimizer.zero_grad()

如果不清楚历史梯度，就会对计算的历史梯度进行累加（通过这个特性你能够变相实现一个很大batch数值的训练）

参考链接：https://www.zhihu.com/question/303070254

## 理解python中的with语句

这看起来充满魔法，但不仅仅是魔法，Python对with的处理还很聪明。基本思想是with所求值的对象必须有一个__enter__()方法，一个__exit__()方法。

紧跟with后面的语句被求值后，返回对象的__enter__()方法被调用，这个方法的返回值将被赋值给as后面的变量。当with后面的代码块全部被执行完之后，将调用前面返回对象的__exit__()方法。

参考链接：http://linbo.github.io/2013/01/08/python-with

## with torch.no_grad()

torch.no_grad()会在函数包含的所有阶段都不计算它的误差梯度了，这样可以防止内存爆掉

## train.py中的59

```
predict_y = torch.max(outputs,dim=1)[1]
```

这里torch.max是指概率最大的那个值，dim=1是指所分的类别，[1]是指只要那个值的index就行，不需要知道数值是多大



conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/