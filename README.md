#基于cnn和svm的地貌分类器
![](https://github.com/wukaiqi/image/blob/master/cnn_svm1.png?raw=true)
##数据集
百度图片爬虫获得六类地形，手工筛选，再使用数据增强扩充数据集

Keras框架下的数据增强工具ImageDataGenerator

设置下列参数为：
>rotation_range=20, width_shift_range=0.2, height_shift_range=0.2, shear_range=0.2, zoom_range=0.2, horizontal_flip=True, vertical_flip=True, fill_mode='nearest' 

##cnn
参数如下图
![](https://github.com/wukaiqi/image/blob/master/cnn_svm2.PNG?raw=true)
##svm
LBP（Local Binary Pattern）算法提取纹理特征，再将特征送入svm进行二分类

使用skimage提取LBP特征,使用sklearn.svm 训练分类器

svm参数设置为：
>kernel='rbf', C=1e6, gamma=20

