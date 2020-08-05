# 安卓车辆检测APP

## 依赖项：

- Android Studio
- Tensorflow object detection API

## 配置模型：

1. 将基于Tensorflow API训练好的my_vehicle.pb文件放在Android文件夹中的 assets文件夹下。
2. 设置对应的Label文件：my_vehicle.txt。
3. 查找 “DetectorActivity.java”文件，找到 **TF_OD_API_MODEL_FILE** 与 **TF_OD_API_LABELS_FILE** 这两个变量，前一个改成自己模型的路径，如 ".../assets/my_vehicle.pb"，后一个改成标签 .txt文件的路径，如 “.../assets**/**my_vehicle.txt”.
4. "DetectorActivity.java” 文件中 **MINIMUM_CONFIDENCE_TF_OD_API** 变量，决定最低多少置信度画识别的框，如果发现移植到手机上的模型效果不理想，可以把这个值调低，就会更容易识别出物体（但是也更容易误识别），根据自己的实际运行效果测试修改。

## 运行TF Detect:

运行结果如下，这是我美丽的南京皇家邮电大学~

![](https://github.com/mgykk/Android-Vehicle_Detection/blob/master/image/1.jpg)

![](https://github.com/mgykk/Android-Vehicle_Detection/blob/master/image/2.jpg)

![](https://github.com/mgykk/Android-Vehicle_Detection/blob/master/image/3.jpg)

![](https://github.com/mgykk/Android-Vehicle_Detection/blob/master/image/4.jpg)
