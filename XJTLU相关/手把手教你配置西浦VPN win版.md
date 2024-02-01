# 手把手教你配置西浦VPN win版

Intro：现在很多校园内的资源想要查看的话，都需要连接学校内部的Wifi，那如果我们在宿舍或者是外地也想要查看，怎么办呢？此教程以windows10为例，教你轻松解决。

事情的起因源于我半夜想在宿舍查看图书馆的馆藏信息来借阅点图书，发现打不开收藏的opac网页（原来在校外也是可以打开的），于是去翻找了lib官网的信息，查到了以下通知。

![image-20221001212144168](https://gitee.com/Zashilaozhai/writing-materials-repo/raw/master/image-20221001212144168.png)

### 1.下载并安装西浦VPN软件

链接放在这里了：

https://box.xjtlu.edu.cn/library/40d017f7-ccba-4d31-90bd-345322465e94/MITS%20Student%20Share/Software/VPN%20Client%20for%20off%20campus%20-%20PacketiX

把这个叫vpnclient.rar的压缩包文件下载后，解压出exe文件，然后点击 弹出安装页面。

直接点击“下一页”

![image-20221002031515695](https://gitee.com/Zashilaozhai/writing-materials-repo/raw/master/image-20221002031515695.png)

点击VPN Client（默认的），下一页。

![image-20221002031616219](https://gitee.com/Zashilaozhai/writing-materials-repo/raw/master/image-20221002031616219.png)

同意用户许可协议后，接着“下一页”。

安装目录就随便吧，默认路径或者你有其它盘也可以指定目录。

![image-20221002031730849](https://gitee.com/Zashilaozhai/writing-materials-repo/raw/master/image-20221002031730849.png)

然后一直点“下一页”，等待安装完成。

### 2.配置VPN（最重要）

双击“添加新的VPN连接”

![image-20221002032031655](https://gitee.com/Zashilaozhai/writing-materials-repo/raw/master/image-20221002032031655.png)

在弹出的管理器中，填写如下信息：

​	主机名：vpn.xjtlu.edu.cn

​	端口号：选择5555（SE-VPN端口）

​	虚拟HUB名：aaa

​	认证类型：选择RADIUS或NT域验证

​    用户名和密码就不用我多说了吧（你的西浦学生账号），最后点击确定。

![image-20221002032712238](https://gitee.com/Zashilaozhai/writing-materials-repo/raw/master/image-20221002032712238.png)

双击咱们刚才设置好的新VPN；

![image-20221002032944443](https://gitee.com/Zashilaozhai/writing-materials-repo/raw/master/image-20221002032944443.png)

然后就可以登录成功啦！

![image-20221002033450309](https://gitee.com/Zashilaozhai/writing-materials-repo/raw/master/image-20221002033450309.png)

### 3.测试

这里放两个需要连接学校内网才能查看的网站资源，可以点击看一下是否能正常打开使用，作为测试我们的VPN是否配置好了。

往年试卷：https://etd.xjtlu.edu.cn/index.html?code=b2212d768e4833679e342c9f6e123d7bc5d12cd79d79d6b99e1fe426d3b8a56e#/SearchDetail/EXAMXJTLU

图书馆借阅个人主页：https://opac.xjtlu.edu.cn/reader/redr_info.php

### 4.小提示

最后的小tips：

	1. 西浦的这个VPN仅供查看校内资源，油管等网站是不可以看的。
	2. 带宽有限，不用的时候可以及时退出。
	3. 这个软件会开机自启，我好像没在软件内找到禁用，但是可以在任务管理器中的启动页面，找到这个软件并点击禁止开机自启。
