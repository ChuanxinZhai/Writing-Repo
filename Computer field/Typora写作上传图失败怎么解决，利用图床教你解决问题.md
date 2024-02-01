# Typora写作上传图失败怎么解决，利用图床教你解决问题
Typora是一款非常好用的富文本Markdown编辑器，笔者在它转为买断制后，依然选择了付费使用。但是写作过程中发现有一个很大的问题，就是当你在写作时插入图片，图片会以本地路径储存，当你将markdown文件上传至CSDN、知乎等网站时，就会出现不可查看图片的问题（如下图），如何解决这个问题呢？本教程利用 Typora，Gitee， PicGo解决此问题。
![在这里插入图片描述](https://img-blog.csdnimg.cn/88db36411d384ce3b22c0f307d17488f.png)

### Step1. 注册Gitee账号
https://gitee.com/ 注册流程因为太简单就省略了
### Step2. 配置图床仓库
注册完成后，点击右上角的“＋”，选择“新建仓库”
![在这里插入图片描述](https://img-blog.csdnimg.cn/50af75c7046a41e5beaf8d1fdbc838ef.png)
输入仓库名称，这个你随便起，路径会根据你仓库名自动生成，不用改。
![在这里插入图片描述](https://img-blog.csdnimg.cn/adf5dd55faa340668aca203559f12e7c.png)
关于“开源”“私有”，我们要选择开源（别人才能看到），但这里只能选择“私有”，等我们完成创建仓库后，教程在下边会教你修改。

创建仓库完成后，点击仓库，找到“管理”。
![在这里插入图片描述](https://img-blog.csdnimg.cn/42d25cf6a13f4c52a7912df9df6d7432.png)

在这里选择开源，并保存。![在这里插入图片描述](https://img-blog.csdnimg.cn/3d2eeeb19d654f1cabb04fd74e11697e.png)
### Step3. 生成私人令牌
依旧是在gitee页，点击右上角你的账户头像，选择“设置”。
![在这里插入图片描述](https://img-blog.csdnimg.cn/065f65ec8c33407c89971e21c83b5efb.png)
在左边找到“私人令牌”。
![在这里插入图片描述](https://img-blog.csdnimg.cn/e22099fa5d6248d896ec115079f58421.png)

点击“生成新令牌”,勾选如下信息，点击“提交”。
![在这里插入图片描述](https://img-blog.csdnimg.cn/8017c8e332c4443c9532f76d57257a08.png)
你的私人令牌就生成完毕了，因为之后就看不到了，**要存一下**（譬如发给微信小号什么的）。
![在这里插入图片描述](https://img-blog.csdnimg.cn/ef477be5abdd411d9f313ee0d577e5e8.png)
### Step4. 安装Node.js
官方下载链接：[Node.js下载](http://nodejs.cn/download/)

![image-20221023223513445](https://gitee.com/Zashilaozhai/writing-materials-repo/raw/master/image-20221023223513445.png)

在安装过程中，Node.js会自动

### Step5. 安装PicGo与下载所需插件
这里放一下链接，找自己电脑系统的下载安装即可。
链接: [PicGo](https://github.com/Molunerfinn/picgo/releases)
![在这里插入图片描述](https://img-blog.csdnimg.cn/0da89dddf0364f108c65b9366cf91601.png)
傻瓜安装，一步就好，默认大家都不会出现问题。
![在这里插入图片描述](https://img-blog.csdnimg.cn/b8153ff4d8b641ed9cf5b42d21e09416.png)
打开软件，在左边找到”插件设置“，搜索gitee-uploader。
![在这里插入图片描述](https://img-blog.csdnimg.cn/d9a7c3e00220441ab691cb807476bbd3.png)

安装完成后，在图床设置里找到gitee：
repo：填写https://gitee.com/后的内容，也就是你的用户名/仓库名，举例：zhangsan/repo。别填错了，如下下图所示；
branch：默认都是master，不用改；
token：之前让你存的私人令牌；
点击确认，设为默认图床。
退出软件，重新打开。

![在这里插入图片描述](https://img-blog.csdnimg.cn/19357afcfd3940cd9b16b9b9decce860.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/32bd49d2174249528f7ecfbbc9b366b0.png)
### Step6. 配置Typora
打开Typora，左上角 ”文件“ → ”偏好设置“ → ”图像“。

插入图片时 ”无特殊操作“ 改为 ”上传图片“；
勾选以下三个选项；
上传服务 ”无“ 改为 ”PicGo(app)";
找到你刚才安装PicGo的路径，（也可能系统自己就找到了）

![在这里插入图片描述](https://img-blog.csdnimg.cn/48b9ac2875274bbfb75535322e08a140.png)
点击”验证图片上传选项“，应该就成功了，然后在自己的gitee repo也可以看到测试上传的图标图片。

### 更新不易，都看到这了，点个赞再走吧
