# 塔斯汀小程序模仿项目

- 本项目归塔斯汀所有，只做学习所用，请尊重原厂版权

- 可以去监听访问数据  fiddler 抓包工具抓取图片

- 界面模仿采用markman做标记
 1. 我们没有设计稿，如何1：1还原小程序？
 2. 拍屏得到小程序截图
 3. 使用在线大小[转换工具](https://www.gaitubao.com/)，将图片改成750
    以后在写wxss的时候，直接量像素就可以写进去，因为小程序以750rpx作为设计稿标准大小帮我们自动适配，很好用。
 4. 使用[markman](http://www.getmarkman.com/) 先标注，再学样式
    以后上班了就不用了，设计师会标注好
    现在还是自己来LOL吧

- 项目配置在根目录下的
    - 隐藏并定制navigatorBar
        "navigationStyle": "custom"
    - 开启定位功能

- 使用了BEM 国际CSS命名规范
    tst_banners  广告位  Block
    tst_banners__img  Element

- css 技巧
    1. 能不用定位就不要用定位
        定位会脱离文档流
    2. 在移动端多用弹性布局 