# github使用指南
## fork和pull request
首先访问ukui/hacking-test项目，地址[如下](https://github.com/ukui/hacking-test.git) 。来到项目主页后可以看到项目中已经有一个hello-ukui.cc项目，现在我们要做的是fork该项目。点击项目右上角的fork按钮，会弹出如下对话框
![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test1.png) 
点击自己的用户名，github就会将项目克隆到自己的账户下。
![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test2.png) 
等待一会项目fork完成，此时点击右侧绿色的clone按钮，出现相应的地址
![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test3.png) 
复制地址并到终端执行git clone命令
```bash
$ git clone https://github.com/readlnh/hacking-test.git
```
我们可以注意到hacking-test前已经是我们的用户名了。稍等一会，待项目克隆到本地。
我们进入hacking-test目录，并创建一个新的c++代码文件，文件名为`hello`+`用户名`的形式。这里以用户readlnh为例，命令如下:
```bash
cd hacking-test
vim hello-readlnh.cc
```
![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test4.png) 
按i进入vim编辑模式，进行编码，编码完成后先按下esc，然后按下:,输入wq保存并退出
![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test5.png) 
在终端编译代码，并执行，命令如下
```bash
$g++ hello-readlnh.cc 
$./a.out
```
如果无误，会输出相应结果。我们先删除生成的a.out文件，然后将我们的代码添加到git里，并提交到github。命令如下：
```bash
$git add hello-readlnh.cc
$git commit -m "I'm readlnh"
$git push
```
![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test6.png) 

`git commit -m`命令后跟的是提交信息，你可以输入任何你想要的提交信息。
`git push`命令后会需要你输入账号密码，注意，如果之前没有在配置git账户，可能会出错，不过要解决也很简单，配置自己的用户名和邮箱即可，命令如下:
```bash
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```
`Your Name`是你的用户名，`email@example.com`改为你的邮箱。

做完这一切后我们可以看到我们fork的项目地址那里已经多了一个c++代码文件了
![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test7.png) 

我们点击pull request按钮进入如下页面

![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test8.png) 

点击Create pull request按钮，在跳转的页面中可以输出一些信息来表示你pull request，比如`请求合并`
![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test9.png) 
再次点击Create pull request按钮，pr发送完毕，等管理员通过pr你的提交就会被合并到ukui下的hacking-test项目中了！
![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test10.png) 

## 提交issue
点击issue标签，进入如下页面

![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test11.png) 

点击New issue按钮，按如下格式提交bug

![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test12.png) 

点击Submit new issue按钮提交issue，issue创建完毕

![](https://raw.githubusercontent.com/readlnh/picture/master/hacking-test13.png) 
