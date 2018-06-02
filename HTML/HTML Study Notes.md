# HTML Study Notes

> By Kevin Song

<!-- MarkdownTOC autolink='true' -->

- [01-01 HTML概述](#01-01-html%E6%A6%82%E8%BF%B0)
	- [基础概念](#%E5%9F%BA%E7%A1%80%E6%A6%82%E5%BF%B5)
	- [基础标签](#%E5%9F%BA%E7%A1%80%E6%A0%87%E7%AD%BE)
		- [字体font](#%E5%AD%97%E4%BD%93font)
		- [标题h1h6](#%E6%A0%87%E9%A2%98h1h6)
		- [转义字符&;](#%E8%BD%AC%E4%B9%89%E5%AD%97%E7%AC%A6)
		- [注释](#%E6%B3%A8%E9%87%8A)
	- [列表dl](#%E5%88%97%E8%A1%A8dl)
		- [有序列表ol](#%E6%9C%89%E5%BA%8F%E5%88%97%E8%A1%A8ol)
		- [无序列表ul](#%E6%97%A0%E5%BA%8F%E5%88%97%E8%A1%A8ul)
	- [图像标签img](#%E5%9B%BE%E5%83%8F%E6%A0%87%E7%AD%BEimg)
	- [表格标签table](#%E8%A1%A8%E6%A0%BC%E6%A0%87%E7%AD%BEtable)
		- [表格基础标签](#%E8%A1%A8%E6%A0%BC%E5%9F%BA%E7%A1%80%E6%A0%87%E7%AD%BE)
		- [合并单元格](#%E5%90%88%E5%B9%B6%E5%8D%95%E5%85%83%E6%A0%BC)
	- [超链接a](#%E8%B6%85%E9%93%BE%E6%8E%A5a)
	- [框架frameset](#%E6%A1%86%E6%9E%B6frameset)
- [01-02 HTML表单标签form](#01-02-html%E8%A1%A8%E5%8D%95%E6%A0%87%E7%AD%BEform)
	- [input标签](#input%E6%A0%87%E7%AD%BE)
	- [下拉菜单select](#%E4%B8%8B%E6%8B%89%E8%8F%9C%E5%8D%95select)
	- [表单格式化](#%E8%A1%A8%E5%8D%95%E6%A0%BC%E5%BC%8F%E5%8C%96)
- [01-03 服务器通信](#01-03-%E6%9C%8D%E5%8A%A1%E5%99%A8%E9%80%9A%E4%BF%A1)
- [01-04 其他标签](#01-04-%E5%85%B6%E4%BB%96%E6%A0%87%E7%AD%BE)
	- [头标签](#%E5%A4%B4%E6%A0%87%E7%AD%BE)
	- [其他标签](#%E5%85%B6%E4%BB%96%E6%A0%87%E7%AD%BE)
	- [XHTML和XML](#xhtml%E5%92%8Cxml)
	- [标签的分类](#%E6%A0%87%E7%AD%BE%E7%9A%84%E5%88%86%E7%B1%BB)

<!-- /MarkdownTOC -->


## 01-01 HTML概述
### 基础概念
**HTML(Hyper Text Markup Language) 超文本标记语言**
**特点**
- 最基础的网页语言
- 由==标签==和==元素==组成
- 代码==不区分大小写==

```
<html>
    <head>
        <title>Kevin's Homepage</title>
    </head>
    <body>
        Welcome to <font color="red" size=36>Kevin's</font> Homepage!<br>
    </body>
</html>
```
**代码组成**
- \<html>开始
    - \<head>头部分开始
        - 给页面增加辅助信息或者属性，最先加载
    - \</head>头部分结束
    - \<body>体部分开始
        - 存放页面数据的地方
    - \</body>体部分结束
- \</html>结束

**标签格式一**：  

```
<标签名 属性名="属性值"> 数据内容 </标签名>
<br></br>           //换行
<hr></hr>           //横线分隔符
<font>data</font>   //字体
```
**标签格式二**： 
```
<标签名 属性名="属性值" />
<br/>               //换行
<hr/>               //横线分隔符
<font/>             //修改往后所有字体
```
**标签操作思想**：标签相当于一个容器，对数据进行封装，通过操作标签的属性来进行对数据的操作

### 基础标签
#### 字体font
```
<font color="#FF0000" size="+6">HelloWorld</ font>
```

属性 | 值 | 描述
---|---|---
color | #XXXXXX<br>rgb(x,x,x)<br>colorname | 规定文本的颜色<font color='red'>（推荐CSS替代）</font>
face | font_family | 规定文本的字体<font color='red'>（推荐CSS替代）</font>
size | number | 规定文本的大小<font color='red'>（推荐CSS替代）</font>

#### 标题h1h6
```
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
<h4>四级标题</h4>
<h5>五级标题</h5>
<h6>六级标题</h6>
```

属性 | 值 | 描述
---|---|---
align | left<br>center<br>right<br>justify | 规定标题文本排列<font color='red'>（推荐CSS替代）</font>


#### 转义字符&;
```
&lt;        <
&gt;        >
&nbsp;      
&times;     ×
```

#### 注释
```
<!--注释内容-->
```
### 列表dl  
- 列表标签：\<dl>\</dl>
- 上层项目：\<dt>\</dt>
- 下层项目：\<dd>\</dd>

<dl>
    <dt>Games</dt>
        <dd>The Elder Scrolls V: Skyrim</dd>
        <dd>Rise of the Tomb Raider</dd>
        <dd>Tom Clancy's The Division</dd>
    <dt>Departments</dt>
        <dd>Dev Team</dd>
        <dd>Art Team</dd>
        <dd>Marketing</dd>
</dl>

```
<dl>
    <dt>Games</dt>
        <dd>The Elder Scrolls V: Skyrim</dd>
        <dd>Rise of the Tomb Raider</dd>
        <dd>Tom Clancy's The Division</dd>
    <dt>Departments</dt>
        <dd>Dev Team</dd>
        <dd>Art Team</dd>
        <dd>Marketing</dd>
</dl>
```


#### 有序列表ol
```
<ol>
    <li>内容</li>
    <li>内容</li>
    <li>内容</li>
</ol>
```
属性 | 值 | 描述
---|---|---
reversed<font color="red">（HTML5） | reversed | 规定列表顺序为降序
start | number | 规定有序列表起始值
type | 1<br>A<br>a<br>I<br>i | 规定再列表中使用的标记类型

#### 无序列表ul
```
<ul type="circle">
    <li>内容</li>
    <li>内容</li>
    <li>内容</li>
</ul>
```
属性 | 值 | 描述
---|---|---
compact | compact | 规定效果更小巧<font color='red'>（推荐CSS替代）</font>
type | disc<br>square<br>circle | 规定列表的符号类型<font color='red'>（推荐CSS替代）</font>

### 图像标签img
```
<img src="c:\1.jpg" height=920 width=1080 align="middle" border="3" alt="Helloworld" />
```
==必须==属性 | 值 | 描述
---|---|---
alt | text | 规定图像的文本
src | URL | 规定图像的URL

可选属性 | 值 | 描述
---|---|---
align | top<br>bottom<br>middle<br>left<br>right | 规定如何根据周围的文本来排列图像<font color='red'>（推荐CSS替代）</font>
border | pixels | 定义图像周围的边框<font color='red'>（推荐CSS替代）</font>
height | pixels% | 定义图像的高度
width | pixels% | 定义图像的宽度
hspace | pixels | 定义图像左侧和右侧的空白<font color='red'>（推荐CSS替代）</font>


图像地图\<map>

```
<img src="Chinese Map" alt="图片说明文字" usemap="#Map"/>
    <map>
        <area shape="rect" coords="50,59,116,104" href="1.html" />
        <area shape="circle" coords="118,203,40" href="1.html" />
    </map>
```
### 表格标签table
#### 表格基础标签
组成
- \<table> 表格
- \<caption> 标题
- \<th>  表头标签（加粗居中）
- \<tr>  行标签
- \<td>  单元格标签

表格属性
- border：边框
- bordercolor：边框颜色
- cellpadding：单元格内边距
- cellspacing：单元格与单元格距离
- width：宽度
```
<table border=1 bordercolor="#0000FF" cellpadding=10 cellspacing=0 width>
    <tbody>
    <caption>表格标题</caption>
    <tr>
        <th>第一行第一列加粗并居中</th>
        <td>第一行第二列</td>
    </tr>
    <tr>
        <td>第二行第一列</td>
        <td>第二行第二列</td>
    </tr>
    </tbody>
</table>
```
<table border=2 bordercolor="#0000FF">
    <tbody>
    <caption>表格标题</caption>
    <tr>
        <th>第一行第一列加粗并居中</th>
        <td>第一行第二列</td>
    </tr>
    <tr>
        <td>第二行第一列</td>
        <td>第二行第二列</td>
    </tr>
    </tbody>
</table>



#### 合并单元格
**横向合并：colspan属性**
<table border=1 bordercolor="#0000FF" cellpadding=10 cellspacing=0 width>
    <tbody>
    <caption>表格标题</caption>
    <tr>
        <th colspan=2>第一行</th>
    </tr>
    <tr>
        <td>第二行第一列</td>
        <td>第二行第二列</td>
    </tr>
    </tbody>
</table>

```
<table border=1 bordercolor="#0000FF" cellpadding=10 cellspacing=0 width>
    <tbody>
    <caption>表格标题</caption>
    <tr>
        <th colspan=2>第一行</th>
    </tr>
    <tr>
        <td>第二行第一列</td>
        <td>第二行第二列</td>
    </tr>
    </tbody>
</table>
```
**纵向合并：rowspan属性**
<table border=1 bordercolor="#0000FF" cellpadding=10 cellspacing=0 width>
    <tbody>
    <caption>表格标题</caption>
    <tr>
        <th rowspan =2>第一行第一列加粗并居中</th>
        <td>第一行第二列</td>
    </tr>
    <tr>
        <td>第二行</td>
    </tr>
    </tbody>
</table>

```
<table border=1 bordercolor="#0000FF" cellpadding=10 cellspacing=0 width>
    <tbody>
    <caption>表格标题</caption>
    <tr>
        <th rowspan =2>第一行第一列加粗并居中</th>
        <td>第一行第二列</td>
    </tr>
    <tr>
        <td>第二行</td>
    </tr>
    </tbody>
</table>
```
### 超链接a
作用：链接资源

**超链接一**  
```
<a href="http://www.baidu.com" target="窗体名">百度</a>
```
**href**属性需要指定协议，如果没有指定协议，则默认使用file协议

超链接类型
- http 网页
- imgs 图片
- mailto 邮箱
- thunder等自定义协议
- 自定义超链接功能

```
<a href="http://www.baidu.com">百度</a>
```
```
<a href="imgs/1.jpg">图片</a>
```
```
<a href="mailto:Kevin.Song@gmail.com">邮件</a>
```
```
<!--下载文件-->
<a href="http://www.xunlei.com/movies/avengers.avi">复仇者联盟</a><br/>
<!--迅雷下载-->
<a href="thunder://www.xunlei.com/movies/avengers.avi">复仇者联盟</a>
```
```
<a href="javascript:void(0)" onclick="alert('你好')">自定义功能超链接</a>
```
**超链接二**

定位标记：锚

```
<a name="mark">Mark</a>
```
超链接

```
<a href="#mark">Back to Mark</a>
```
锚和超链接结合使用才有效
```
<html>
    <head>
        <title>Kevin's Homepage</title>
    </head>
    <body>
        <a name=top>顶部</a>
        <hr/>
        正文1
        <hr/>
        <a name=center>中间</a>
        <hr/>
        正文2
        <a href="#top">返回顶部</a>
        <a href="#center">返回中间</a>
    </body>
</html>
```
### 框架frameset
框架定义在head和body之间

```
<html>
    <head>
        <title>Kevin's Homepage</title>
    </head>
    
    <frameset rows="30%,*">
        <frame src="1.html" name="page1"/>
        <frameset cols="30%,*">
            <frame src="2.html" name="page2"/>
            <frame src="3.html" name="page3"/>
        </frameset>
    </frameset>
    
    <body>
    </body>
</html>
```
画中画标签

```
<html>
    <head>
        <title>Kevin's Homepage</title>
    </head>
    <body>
        <iframe src="1.html" height=300 width=300>这是画中画标签，如果您看到这段文字，很遗憾，你的浏览器不支持该标签</iframe>
    </body>
</html>
```
## 01-02 HTML表单标签form
<form>      
</form>     
表单是最常用的标签，用于与服务器端的交互

常用属性
- action
- method

### input标签

<input type="属性值" />：输入标签，接受用户输入信息  
type属性的10个值
- text：文本框
- password：密码框
- radio：单选框
    - name：组名，同一组的只能选一个
    - checked：默认选定
- checkbox：复选框
- reset：重置
    - value：自定义按钮名称
- submit：提交
    - value：自定义按钮名称
- file：选择文件
- image：图片超链接
- hidden：隐藏组件，数据不需要客户端知道，但是可以将其提交到服务器端
- button：按钮
    - onclick：点击触发

如果要给服务器提交数据：表单中的组件必须有name和value属性
```
<html>
    <head>
        <title>Kevin's Homepage</title>
    </head>
    <body>
        <form>
            1. 输入姓名：<input type="text" name="user" value="" /><br/>
            2. 输入密码：<input type="password" name="pwd"/><br/>
            3. 选择性别：<input type="radio" name="gender" value="man"/>男<br/>
                     <input type="radio" name="gender" value="woman" checked="checked"/>女<br/>
            4. 选择技术：<input type="checkbox" name="tech" value="Java"/>Java<br/>
                     <input type="checkbox" name="tech" value="C++"/>C++<br/>
                     <input type="checkbox" name="tech" value="Python"/>Python<br/>
            5. 选择文件：<input type="file" name="file" value="" /><br/>
            6. 图片按钮：<input type="image" src="11.jpg"><br/>
            7. 隐藏组件：<input type="hidden" src="11.jpg"><br/>
            8. 一个按钮：<input type="button" value="按钮" onclick="alert('爱你欧')"><br/>
                     <input type="reset" value="重置表单">
                     <input type="submit" value="提交表单">
        </form>
    </body>
</html>
```
### 下拉菜单select
下拉菜单

```
<select>
    <option value="none">--选择国家--</option>
    <option value="USA">美国</option>
    <option value="CN" selected="selected">中国</option>
    <option value="KR">韩国</option>
</select>
```
文本框

```
<textarea name="text"></textarea>
```
### 表单格式化

```
<html>
    <head>
        <title>Kevin's Homepage</title>
    </head>
    <body>
        <form action="http://www.baidu.com" method="get">
            <table border="1" bordercolor="#00ffff">
                <tr>
                    <thcolspan="2">注册表单</th>
                </tr>
                <tr>
                    <td>用户名称</td>
                    <td><input type="text" name="user" value="" /></td>
                </tr>
                <tr>
                    <td>输入密码</td>
                    <td><input type="password" name="pwd"/></td>
                </tr>
                <tr>
                    <td>确认密码</td>
                    <td><input type="password" name="repwd"/></td>
                </tr>
                <tr>
                    <td>选择性别</td>
                    <td>
                    <input type="radio" name="gender" value="man" />男
                    <input type="radio" name="gender" value="woman" />女
                    </td>
                </tr>
                <tr>
                    <td>选择技术</td>
                    <td>
                    <input type="checkbox" name="tech" value="Java"/>Java
                    <input type="checkbox" name="tech" value="C++"/>C++
                    <input type="checkbox" name="tech" value="Python"/>Python
                    </td>
                </tr>
                <tr>
                    <td>选择国家</td>
                    <td>
                        <select name="country">
                            <option value="none">--选择国家--</option>
                            <option value="USA">美国</option>
                            <option value="CN" selected="selected">中国</option>
                            <option value="KR">韩国</option>
                        </select>
                    </td>
                </tr>
                <tr>
                    <th colspan="2">
                    <input type="reset" value="重置表单">
                    <input type="submit" value="提交表单">
                    </th>
                </tr>
            </table>
        </form>
    </body>
</html>
```
## 01-03 服务器通信
前端代码
```
<html>
    <head>
        <title>Kevin's Homepage</title>
    </head>
    <body>
        <form action="http://10.1.31.69:9090" method="get">
            <table border="1" bordercolor="#00ffff">
                <tr>
                    <thcolspan="2">注册表单</th>
                </tr>
                <tr>
                    <td>用户名称</td>
                    <td><input type="text" name="user" value="" /></td>
                </tr>
                <tr>
                    <td>输入密码</td>
                    <td><input type="password" name="pwd"/></td>
                </tr>
                <tr>
                    <td>确认密码</td>
                    <td><input type="password" name="repwd"/></td>
                </tr>
                <tr>
                    <td>选择性别</td>
                    <td>
                    <input type="radio" name="gender" value="man" />男
                    <input type="radio" name="gender" value="woman" />女
                    </td>
                </tr>
                <tr>
                    <td>选择技术</td>
                    <td>
                    <input type="checkbox" name="tech" value="Java"/>Java
                    <input type="checkbox" name="tech" value="C++"/>C++
                    <input type="checkbox" name="tech" value="Python"/>Python
                    </td>
                </tr>
                <tr>
                    <td>选择国家</td>
                    <td>
                        <select name="country">
                            <option value="none">--选择国家--</option>
                            <option value="USA">美国</option>
                            <option value="CN" selected="selected">中国</option>
                            <option value="KR">韩国</option>
                        </select>
                    </td>
                </tr>
                <tr>
                    <th colspan="2">
                    <input type="reset" value="重置表单">
                    <input type="submit" value="提交表单">
                    </th>
                </tr>
            </table>
        </form>
    </body>
</html>
```
服务端代码
```
public class RegServer {
    public static void main(String[] args) {
        ServerSocket ss = new ServerSocket(9090);
        Socket s = ss.accept();
        InputStream in = s.getInputStream();
        byte[] buf = new byte[1024];
        
        int len = in.read(buf);
        
        System.out.println(new String(buf,0,len));
        PrintWriter out = new PrintWriter(s.getOutputStream(),true);
        
        out.println("<font color='green' size=7>注册成功</font>");
        
        s.close();
        ss.close();
    }
}

提交方式：GET
地址栏：http://10.1.31.69:9090/?user=abc&psw=123&repsw=123&sex=nan&tech=java&tech=html&country=cn

GET /?user=abc&psw=123&repsw=123&sex=nan&tech=java&tech=html&country=cn HTTP/1.1
Accept: image/gif, image/x-xbitmap, image/jpeg, image/pjpeg, application/x-shockwave-flash, application/vnd.ms-excel, application/vnd.ms-powerpoint, application/msword, */*
Accept-Language: zh-cn,zu;q=0.5
Accept-Encoding: gzip, deflate
User-Agent: Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; SV1; InfoPath.2)
Host: 10.1.31.69:9090
Connection: Keep-Alive

提交方式：POST
地址栏：http://10.1.31.69:9090/

POST / HTTP/1.1
Accept: image/gif, image/x-xbitmap, image/jpeg, image/pjpeg, application/x-shockwave-flash, application/vnd.ms-excel, application/vnd.ms-powerpoint, application/msword, */*
Accept-Language: zh-cn,zu;q=0.5
Content-Type: application/x-www-form-urlencoded
Accept-Encoding: gzip, deflate
User-Agent: Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; SV1; InfoPath.2)
Host: 10.1.31.69:9090
Content-Length: 68
Connection: Keep-Alive
Cache-Control: no-cache

user=hahah&psw=8989&repsw=8989&sex=nv&tech=html&tech=css&country=usa
```
**GET提交和POST提交的区别**
- 区别一
    - GET提交，提交的信息显示在地址栏中
    - POST提交，提交的信息不显示地址栏中
- 区别二
    - GET提交，敏感数据信息不安全，密码暴露无遗
    - POST提交，敏感数据安全
- 区别三
    - GET提交，对于大数据不行，地址栏存储体积有限
    - POST提交，可以提交大体积数据
- 区别四
    - GET提交，把信息封装到了请求消息的请求行中
    - POST提交，把信息封装到了请求消息的请求体中
- 区别五（在服务端）当中文提交到Tomcat服务器，服务器会默认用ISO8859-1进行解码出现乱码。用IOS8859-1进行编码，再用指定中文码表解码即可。这种方式对GET提交和POST提交都有效
    - 对于POST提交的中文，还有另一种解决方法，直接使用服务端的一个对象。
    - request对象的setCharacterEncoding方法直接设置指定的中文码表就可以将中文数据解析出来
    - 该方法只对请求体中的数据进行解码

**前端和服务端交互的三种方式**
1. 地址栏输入url地址---GET请求
2. 超链接---GET请求
3. 表单---GET和POST请求

**增强型校验**  
增强型校验定义：只要有一个组件内容错误，是无法继续提交的只有全对才可以提交

客户端进行增强型校验后，服务端也需要进行校验  
原因：  
增加安全性，因为与服务端交互方式不止表单提交一种，可以防止直接在地址栏输入url地址暴力注册，确保服务端只会收到正确的信息。

服务端进行增强型校验后，客户端也需要进行校验  
原因：  
增加用户上网体验，每次都在服务端校验增加了等待时间，并且增加了服务端的压力

## 01-04 其他标签
### 头标签
放在<head></head>之间的标签
- <title>
    - 显示标题
- <base> 
    - href 属性 制定网页中所有的超链接的目录
    - target 属性 指定打开超链接的方式。比如_blank表示所有的超链接都用新窗口打开
- <meta>
    - http-equiv 属性模拟http协议的响应消息头
        - 例 三秒后去百度 <meta http-equiv="refresh" content"3;url=http://www.baidu.com" />
- <link>
    - rel 属性 描述目标文档与当前文档的关系
    - type 属性 文档类型
    - media 属性 指定目标文档在哪些设备上有用
    - 例：<link rel="stylesheet" type="text/css" media="screen,print" />

### 其他标签
- <marquee> 让内容动起来
    - direction 属性：left right down up
    - behavior 属性：scroll alternate slide
- \<pre>显示代码的样子
- \<b> 加粗
- \<i> 斜体
- \<u> 下划线
- \<sub> 下标
- \<sup> 上标


```
<html>
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=GBK">
        <title>Untitled Document</title>
    </head>
    <body>
        <pre>
        class Demo {
            public static void main(String[] args) {
                System.out.println("hello");
            }
        </pre>
        <hr/>
        
        <marquee direction="down" behavior="slide">
        AAA
        </marquee>
        <b>AAA</b><i>BBB</i><u>CCC</u>
        X<sub>2</sub> X<sup>2</sup>
    </body>
</html>

```

### XHTML和XML
XHTML 可扩展超文本标记语言（Extensible Hypertext Markup Language）
- 本来替代HTML，没成功，因为HTML已经被广为使用。结构更严谨
- 是基于XML的一种应用

XML 可扩展标记语言（Extensible Markup Language）
- XML是对数据信息的描述。HTML是对数据显示的描述
- XML代码规定更加严格，标签不结束视为错误
- XML规范可以被更多的app所解释，成为一种通用的数据交换语言
- 各个服务器和框架都将XML作为配置文件

### 标签的分类
没有意义的标签，只有封装作用
```
<!--div自动换行-->
<div>这是一个div区域</div>
<div>这是一个div区域</div>
<!--span自动换行-->
<span>这是一个span区域</span>
<span>这是一个span区域</span>
<!--p自动换行且隔行-->
<p>这是一个段落1</p>
<p>这是一个段落2</p>
```
标签的分类
- 块级标签：标签结束后都有换行 <div><p><dl><table><ol><ul>
- 行内标签：标签结束后没有换行 <font><span><img><input><select><a>