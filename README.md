# <center>CGAN_jittor</center>

Generative Adversarial Nets（GAN）[1]提出了生成和对抗网络来训练生成模型。然而，GAN对于要生成的图片缺少控制。Conditional GAN（CGAN）[2]通过添加显式的条件或标签，可以更好地解决控制生成图像的问题。

本项目利用jittor框架，搭建了一个完整的、用于手写数字图片生成的CGAN模型，可以借助开源数字图片数据集MNIST完成训练和生成手写数字过程。



## 运行方式

```
git clone --recursive https://github.com/liu-tq20/CGAN_jittor.git
cd CGAN_jittor
```



## 训练参数

```
--n_epochs      number of epochs
--batch_size    size of each batch
--lr            learning rate
--b1            decay of first order momentum of gradient
--b2            decay of first order momentum of gradient
--n_cpu         number of cpu threads to use during batch generation
--latent_dim    dimensionality of the latent space
--n_classes     number of classes for dataset
--img_size      size of each image dimension
--channels      number of image channels
--sample_interval interval between image sampling
```



## 训练结果

下面展示了本项目在MNIST数据集的训练结果。以下分别是训练第0 epoch和93 epoches的结果。  ![93000](https://github.com/liu-tq20/CGAN_jittor/blob/main/resultImg/0.png)![93000](https://github.com/liu-tq20/CGAN_jittor/blob/main/resultImg/93000.png)

## 参考文献

[1] Goodfellow, Ian, et al. “Generative adversarial nets.” Advances in neural information processing systems. 2014.

[2] Mirza, Mehdi, and Simon Osindero. “Conditional generative adversarial nets.” arXiv preprint arXiv:1411.1784 (2014).