# know-BOM（了解BOM）
## BOM:浏览器对象模型的简称
> Browser Object Model
- 打开一个浏览器，里面的所有功能都是BOM对象
> 窗口（打开的网页整体看做一个窗口）、屏幕（网页是显示在一个屏幕上的）、导航栏、历史访问记录、标题、网页主题内容、地址栏、收藏
>> 我们将打开的整个网页看做窗口对象,窗口对象中封装了和窗口相关的属性和方法，比如打开一个窗口，关闭一个窗口。
>>> 最常见的一个：window.open（）;里面有许多的参数
>>>> innerHeight | pixel value | 窗口中文档的像素高度
>>>> innerWidth | pixel value | 窗口中文档的像素宽度
- 可以说万物都是window对象
> 定义一个全局变量num或者函数fn
>> 都可以使用window.num或者window.fn来直接调用
## Window 内置全局属性和方法
1. 全局常量: Infinity, NaN, undefined, null
2. 全局方法: eval(), isFinite(), isNaN(), parseFloat(), parseInt(),decodeURI(),decodeURIComponent(), encodeURI(), encodeURIComponent()
>  对话框
3. alert() 函数：弹出消息对话框（对话框中有一个OK按钮）confirm() 函数：弹出消息对话框（对话框中包含一个OK按钮与Cancel按钮）prompt() 函数：弹出消息对话框（对话框中包含一个OK按钮、Cancel按钮与一个文本输入框）
> 时间等待与间隔函数
4. setTimeout() 函数   clearTimeout() 函数    setInterval() 函数    clearInterval() 函数
> 获取失去焦点
5. focus() 函数：使窗体或空间获得焦点    blur() 函数：使窗体或控件失去焦点
### 相关的知识点
1. 指数表示法
> 如果数字巨大，可以使用指数表示法
>> 比如：
>>> 1e1表示在1后面加1个    0 ：10
2. NAN
> 它表示’不是数字‘的数字,事实上他是一个数字类型：
>> typeof NaN  ：number
>>> 如果我们再数字运算中使用了不恰当的操作数，导致运算失败，该运算就会返回NaN
>>>> 例如:var a = 10 * 'f'  --- NaN
3. parseInt&parseFloat
> 将输入的值转换成数字
> parseInt('123')
>> parseFloat('1.2ab')//1.2
4. inNaN
> 确定某个数值可以参与运算 inNaN(123);
5. eval
> 会把里面的字符串当做js代码来执行
## 地址栏对象（标重点）
> 地址栏window.location
- 面向对象的方法分析地址栏
### 他大概包含了如下属性
1. URL网址：http://www.baidu.com
2. 协议：http ftp
3. 端口号：默认80
4. 查询字符串？name=zzc&&password=123456
- url属性
> 我们在浏览器的地址栏里输入的网站地址叫做URL(Uniform Resource Locator，统一资源定位符)。
>> 就像每家每户都有一个门牌地址一样，每个网页也都有一个Internet地址。
>>> 当你在浏览器的地址框中输入一个URL或是单击一个超级链接时，URL就确定了要浏览的地址
- 协议
> 协议是一种规定，只要你按照这个格式就能实现想要的功能。

> 比如只要你在地址栏中输入一个网址就能打开一个网页，这就是http协议.

> HTTP协议是用来浏览网站的.

> FTP是用来访问和传输文件的,FTP文件传输有点批量上传和维护网站的意思.

> 简单说HTTP是面向网页的，而FTP是面向文件的。
>> 其他协议
>>> 文件传输协议FTP
>>> 电子邮件传输协议SMTP
>>> 域名系统服务DNS
>>> 网络新闻传输协议NNTP
>>>> window.location也可以做成window.open的效果。
## 历史访问记录对象
    document.getElementById('btn').onclick=function() {
        /*改变当前窗口的地址，则会打开新的网页*/
        window.location ='test2.html'
    }

    document.getElementById('btn1').onclick=function() {
        history.back()
    }

    document.getElementById('btn2').onclick=function() {
        history.forward()
    }
## 网页的核心-DOM
> 学习DOM，其实就是学习增删查改




