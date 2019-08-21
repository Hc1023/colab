# colab
这里我将存放一些在colab运行过的代码，免费GPU，感觉还不错

网页查看需打开小飞机，科学上网

## colab初次使用 [hello_world.ipynb](<https://github.com/Hc1023/colab/blob/master/hello_world.ipynb>)

## 经典数据集的分类器 [MNIST_in_Pytorch.ipynb](<https://github.com/Hc1023/colab/blob/master/MNIST_in_Pytorch.ipynb>)

修改自[classifier_sample]('https://github.com/Hc1023/colab/blob/master/classifier_sample.ipynb')，数据集从CIFAR变为MNIST，不同之处：1.CIFAR是三通道的而MNIST是单通道的； 2.网络的参数需要变动。

同时，这是classifier_sample的进化版，全面实现了一个分类器应该做的事情，而前者只进行了训练。

且可与[MNIST_in_Keras](https://github.com/Hc1023/colab/blob/master/MNIST_in_Keras.ipynb)对比

## “肺结节识别”暑期大作业运行结果 [runLIDC.ipynb](<https://github.com/Hc1023/colab/blob/master/runLIDC.ipynb>)

运行“2019数学软件”暑期大作业“肺结节识别”程序，这份notebook展示了本次作业的准确率和模型参数

整个程序参考了[mixupfamily](<https://github.com/FengHZ/mixupfamily>)，并在此基础上修改而成

  - 主要架构

dataloader.py 对数据集建立dataset类，参考了[DATA LOADING AND PROCESSING TUTORIAL](<https://pytorch.org/tutorials/beginner/data_loading_tutorial.html>)，以及划分训练集和验证集，1197份数据进行训练，200份进行验证

wideresnet.py 选用wideresnet作为训练网络，3D卷积

main.py 读入数据集，训练，验证，保存模型

 - 现存问题

由于网络复杂而数据集较小，使得网络过拟合，验证集损失不降。
期间调整过学习率的大小并没有改善。

训练集损失在迭代次数增加时稍有上升，后期可考虑降低学习率。

 - 结果

模型参数见文件中的checkpoint

准确率及损失见[日志](https://github.com/Hc1023/colab/blob/master/0820.png)



