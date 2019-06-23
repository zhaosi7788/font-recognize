# Chinese-font-recognition
Chinese font recognition

## Training

- Run `python train.py` to train VGG16


## Training on your own dataset
-Add font files to dataset/fonts folder. Take Mac for example, those files are in /System/Library/Fonts. 将字体文件放置在dataset/fonts的文件夹下

-cd dataset 进入dataset文件夹

-Run python generator.py to generate datasets 运行generato.py文件，生成训练集

-Run python train.py to train VGG16 运行train.py将根据训练集生成模型文件并保存到models文件夹下。 -生成自己的模型之后，运行web.py文件将网页版字体识别程序部署到flask服务器上，暴露的端口在run函数内定义。如port=5000将暴露5000端口，地址改为“0.0.0.0”就可以 被所有的主机访问。

-上传页面在template的upload.html -上传的图片保存在static/images文件夹下。 -训练的log写在log文件夹下，可由tensorboard查看。
