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
    3. 选择器优先级
        标签 1 < 类名 10 < id 100 < 计算表达式 
        p.md2  11
        p.md2 + div.md3  11 + 11
        行内样式，优先级更高  少用
        !important 最高  慎用
    4. 弹性布局
        移动端 flex 可以解决大部分问题
        div  块级
        布局的一种  跟外部不一样的布局
        flex 内部  块级哪里丢失，默认不会换行    BFC Block formating context
        


- git 提交
    1. 第一次git 命令行提交
        全局配置  git config --global user.name "1975686741"
        git config --global user.email "1975686741@qq.com" 

- 滴滴swiper 多页滑动菜单功能
        用户体验  less is more！ 摆在第一位
        菜单太多，用户的密集恐惧症，把重要的放在首页
        其他的可以多放一些
        技术难度 
    1. swiper > 2 swiper-item
    2. swiper 高度 变化的 等高的
        2行
        4行的高度
        swiper height  响应式的数据
    3. class = "didi_menus {{'higher_menu'}}" 
        {{}} 占位符 返回值是替换的值
    4. swiper bindChange 事件
        event 对象中
        event.datail.current  当前是第几个swiper-item?
        menu_type
        this.setData()

- 数据响应式编程
    它是一个思想，有别于DOM编程API
    设置一些页面效果，操作的不是DOM，
    操作的是数据，因为数据一旦发生改变，页面会自动刷新
1. 滴滴可变高度的首页菜单
