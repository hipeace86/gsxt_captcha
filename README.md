# 破解极验点击验证码

国家企业信用信息公示系统](http://www.gsxt.gov.cn/index.html)中的验证码是按语序点击汉字，如下图所示：

![验证码](./doc_images/gsxt.png)

即，如果依次点击：‘无’，‘意’，‘中’，‘发’，‘现’，就会通过验证。

本项目的**破解思路**主要分为以下步骤：

1. 使用目标探测网络YOLOV2进行**汉字定位**
2. 设计算法进行**汉字切割**
3. 使用darknet的分类器进行**汉字识别**
4. 设计算法进行**汉字纠错与语序识别**

说明：该项目对于破解5个字及5个字以下的验证码效果不错，本人测试了400张图片正确率达到了0.85。

这里提供一个提升破解速度和准确率的思路：在以后破解gsxt网站的时候，可以将识别正确的词语加入到字典库中，这样随着时间的推移，正确率和速度都会越来越高。

# 免责声明

**该项目仅用于学术交流，不得任何商业使用！**

**如果该项目对您有帮助，记得点一个star哦！**，详细文档请见[个人博客](https://runninggump.github.io/2018/11/19/破解含语序问题的点击验证码)


