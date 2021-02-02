# tensorflow

通道顺序：[batch,height,width,channel]



## 查看数据集的一些语句

```python
import numpy as np
import matplotlib.pyplot as plt


imgs = x_test[:3]
labs = y_test[:3]
print(labs)
plot_imgs = np.hstack(imgs)
plt.imshow(plot_imgs, cmap='gray')
plt.show()
```



## @tf.function装饰器（构造高效的python代码）

将python代码转换为tensorflow的图模型结构，训练速度会大大提升





![image-20200721232805078](C:\Users\zzh\AppData\Roaming\Typora\typora-user-images\image-20200721232805078.png)