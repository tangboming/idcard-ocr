## [idcard-ocr](https://github.com/EliasCai/idcard-ocr )
#### 用途：
主要针对身份证的地址文字OCR，其他有文字的图片也可以，但没有文字检测的功能

#### 代码介绍
1. background：生成文字的背景图片
2. code：代码库
3. corpus：语料库（需要自己准备，这里上传的是一个样例）
4. font：字体库 
5. log：存放模型权重

#### 运行环境
1. keras == 2.2.0
2. tensorflow == 1.6.0

#### 训练：
1. 建立语料库（corpus/address_lite.txt）
2. 训练模型（code/train.py）

#### 改进
代码参考[该库](https://github.com/YCG09/chinese_ocr )，主要改进以下：
1. 扩充了汉字库（增加了200多个，目前有6000个以上汉字）
2. end2end的训练模式，从语料库直接生成文字图片，更加方便
3. 文字和图片的随机增强（文字随机排列、图片的背景和字体的随机生成、文字的角度等）

#### 精度
loss小于0.05，精度大于0.99

#### Todo List
1. ~~模型与训练的代码分开~~
2. 除了地址，增加其他项目的识别（身份证号、有效日期等）
3. 增加文字检测功能（只针对身份证）
4. 文字增强（文字旋转图像不旋转、文字设置透明度）
