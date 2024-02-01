# 手把手教你配Anaconda

此教程全程Typora手打，绝对不洗稿！本篇写于2022年9.18日

因为学校的课程，需要安装Anaconda，我自己在安装过程中也出了一些配置环境变量上的问题，所以决定写这篇博客记录一下整个安装过程，包含下载、安装、配置、检验。看完这个教程，你应该配好没什么问题~

### Step1.上官网下载安装包

这里放一下Anaconda的官网，可以直接跳转下载

[Anaconda | The World's Most Popular Data Science Platform](https://www.anaconda.com/)

![在这里插入图片描述](https://img-blog.csdnimg.cn/0979a77baaa64a69b841f26923d27ddd.png)


下面以windows系统为例，一步步安装

### Step2. 安装过程

2.1点击Next

![在这里插入图片描述](https://img-blog.csdnimg.cn/a88e485b577548eab212dacbdff6524b.png)


2.2直接点同意（Agree）

![在这里插入图片描述](https://img-blog.csdnimg.cn/fdccd961750d4274af481f2cddeea13a.png)

2.3这个地方，如果是自己电脑，选择All users也可以的，影响不大，继续点击Next

![在这里插入图片描述](https://img-blog.csdnimg.cn/55612222609e47ddbb9d2a17e875c81b.png)


2.4这里就是看你放在哪个盘，C盘有位置就可以放，想放D盘或者其它盘也可以。稍微记一下你的安装路径，如果你改了默认安装路径的话，step3里的配置环境变量需要用到。

（注意，路径最好不要有中文，不然可能会出现问题，包括你安装其它东西也是这样子）
![在这里插入图片描述](https://img-blog.csdnimg.cn/fd38845cc30348dcbb9a17cc2c40d8c7.png)


2.5这里高级选项中，

​    第一个Add PATH不建议勾选，配置环境变量等安装完我们会在Step3里教你怎么改。

​    第二个建议勾选。

​    然后选择安装（Install）
![在这里插入图片描述](https://img-blog.csdnimg.cn/64c93fff028b4be19673811335d2591e.png)


2.6 等安装完后一直点Next，等到出现以下界面

![在这里插入图片描述](https://img-blog.csdnimg.cn/49b8d232d03342b2af6bbdb74a39208f.png)


这里，两个都是教程或者广告一类的，不用勾选，点击”Finish“完成安装。

接下来我们就可以开始配环境变量了。

### Step3. 配置环境变量

这一步很重要，关乎到你有没有真正的弄成功

3.1 打开电脑桌面上的“此电脑”，鼠标右键“属性”，在系统这个页面选择“高级系统设置”

![在这里插入图片描述](https://img-blog.csdnimg.cn/cd8680e7c7654acc91e981d0fbe6b12f.png)


点击，“环境变量”

![在这里插入图片描述](https://img-blog.csdnimg.cn/f7021268e06e41c8b72baffd0ca52114.png)


嫌麻烦的话，可以直接电脑左下角搜索“查看系统高级设置”或“编辑系统环境变量”，可以直接出来此页面。

![在这里插入图片描述](https://img-blog.csdnimg.cn/51071f153c65426a8b4cfc4719d3a700.png)


3.2 来到“环境变量”页面

![在这里插入图片描述](https://img-blog.csdnimg.cn/b7a25839126c44fd966a7eaf0fb802e4.png)


点击“系统变量”，找到“Path”，点击“编辑”，划到最下方空白处，点击“新建”

![在这里插入图片描述](https://img-blog.csdnimg.cn/102c2f464b3d4d109a56133fdb438e76.png)


依次输入：

​    Anaconda安装路径（step2安装步骤里提到过的）

​    Anaconda安装路径\Scripts

​    Anaconda安装路径\Library\bin

​    Anaconda安装路径\Library\mingw-w64\bin

如果你没有改默认路径，那就跟我的一样（如截图所示），我直接把路径放到这里，你直接ctrl C V大法即可。

C:\ProgramData\Anaconda3

C:\ProgramData\Anaconda3\Scripts

C:\ProgramData\Anaconda3\Library\bin

C:\ProgramData\Anaconda3\Library\mingw-w64\bin

完事后，点击“确定”，我们的配置环境变量就结束了

接下来我们检验一下是否配置好了

### Step4.检验

win键+R，输入cmd。
![在这里插入图片描述](https://img-blog.csdnimg.cn/0e45beeefaec49c194f62e72663fcb4d.png)


打开命令行，输入"conda --version" 或者“conda -V”

![在这里插入图片描述](https://img-blog.csdnimg.cn/ee6ce06f45c64f47b1b0f6e095d460b5.png)


如果能看到conda的版本，例如我这里是4.14.0，那就是安装成功了。

还可以输入“python --version”或“python -V"查看python的版本。

（如果看到提示说“不是内部或外部命令，也不是可运行的程序”，那说明你还没配好，找找之前的配置环境变量是不是出问题了。）


### 希望每个看到这个教程的人都可以配好环境

都看到这里了，点个赞再走吧，大学生更新不易，感谢您！
