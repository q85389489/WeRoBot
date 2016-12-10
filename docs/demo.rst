微信werobot的简单demo例子：
  操作系统：ubuntu 16.04
  python版本:2.7.12
  werobot版本:1.0.0
  
1:首先需要安装werobot模块
  命令：sudo pip install werobot
  
2:安装完成后，进入python环境
  命令 python
  输入 import werobot 
  如果没有报错，恭喜您，已经成功安装改模块
  
3:创建一个我们存放微信的源码目录
  命令 mkdir wx
 
4:进入该目录
  命令 cd wx
5:新建第一个微信后台的处理程序
  命令 touch index.py
  
6:利用VIM进行代码编辑
  命令 vim index.py
 
7:我们来做一个简单的例子：
  import werobot
  robot=werobot.WeRoBot(token="填写你的TOKEN")
  
  下面这句代码处理新用户关注公众号事件
  @robot.subscribe
  def echo(message):
        return "你好，欢迎关注像素数据公众号,请回复帮助查看中文菜单"
        
  下面这句代码处理用户发来的文本
  @robot.text
  def echo(message):
      return “发什么文本？”
  
  下面这句代码处理用户位置信息
  @robot.location
  def echo(message):
      return "你的位置？我记得了，下次去找你"
  
  下面这句代码处理用户发来http地址
  @robot.view
  def echo(message):
      return "这是什么地址？说中文"
  @robot.voice
  
  下面这句代码处理用户发来的语音
  def echo(message):
      return "我们公司现在还没有做语音识别，请用中文!拜托"
 
 下面这句代码处理用户发送过来的图片
 @robot.image
  def echo(message):
      return "图片收下了，想体验人脸识别？直接回复 [想体验人脸识别] 然后看文字操作
步骤来"

  
  
