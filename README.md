# PA-Q&A-2020 NUAA

NUAA PA2020常见问题解答（持续更新，欢迎加星）

------

# 读前必看

1. 提问以前务必翻看翻看本问答文档，对于文档中已经给出的问题，助教均不再回复，敬请谅解！
2. 有偿（`1分钱QQ红包`）征集遇到的问题的解决办法
   想分享你遇到问题的解决办法？没问题你可以把想说的话，想提醒大家的事情，还包括代码框架本身的 bug 等等`直接以 Pull Requests 的形式`提交到本仓库的 `Master` 分支，遇到有人提交我会上去检查一下后合并的。另外这个问答的issue功能关掉了，以免有人使用不文明用语或发答案。
3. 请参与编写 Q&A 的同学严格按照[中文文案排版指北](https://github.com/sparanoid/chinese-copywriting-guidelines)排版，以减少维护工作量，谢谢！
4. 注意这里不是共享答案的地方，每次检查报告的时候是有查重的，请同学们珍惜自己的代码……因此遇到这种提交不予合并，技术性难题大家可以一起讨论。温馨提醒：每次提交的报告都会**查重**，请不要把自己的代码分享给别人，遇到**雷同的按讲义[课程设计提交要求](https://nuaa-pa.github.io/gitbook/others/submit-requirement.html#关于学术诚信)处理，敬请知晓！**
5. 新添加的问题将放在最前面，以免大家看不到以为没更新，想看历史比较久远的问题往后面看


# PA0

1. 【置顶】PA0的所有问题基本百度都能解决，所以遇到问题请大家尝试独立去解决，英文报错大家应该都能看懂，一般按照讲义和视频来自己操作不失误就没什么问题，不要什么问题都来问助教。

2. 安装虚拟机时遇到选择安装后黑屏，很可能是镜像文件本身的问题，请重新到 Debian 官网或者镜像点重新下载安装包镜像重新安装。

3. 如果遇到 virtual box 报错虚拟机无法启动的问题，多半是如下原因，请逐一排查：

   (1)电脑 BIOS CPU 虚拟化未开启（不同机型有不同的开启方法，请上网查阅资料处理）；

   (2)电脑中 Hyper-v 等其他虚拟机占用了虚拟化资源；

   (3)没有用管理员身份运行虚拟机；

   (4)其它问题请根据 log 文件（右击自己创建的虚拟机，点击日志）中的 Error 去搜索引擎搜索，这类问题网上都有解决方案；

   (5)实在解决不了可以换用 VMware 或者装双系统。

4. 用 `su `命令之后不能 `poweroff`，请用 `su -` 命令 (不听课警告，请仔细观看视频！)。

5. 如果遇到自己的主机名是 `bogon` , 对实验应该没什么影响，如果你担心可以去网上搜一下如何改回 `debian`。

6. 命名 `addgroup` 把自己的用户名添加进去了，但是还是不能用 `sudo` 命令的话重启一下虚拟机就好了。

7. ping  百度，显示 name resolution 失败，先尝试ping一下 `114.114.114.114`，如果不可以 ping 通，是网络配置有问题，请检查自己是否联网，interfaces 文件有没有改对，如果可以 ping 通，是 DNS 有问题，请在interfaces文件对应的上网网卡下面添加 `nameserver 114.114.114.114`  和  `nameserver 223.5.5.5` 手动指定一下DNS。

8. putty 连接不上，请检查自己的IP是不是 `127.0.0.1` 端口是不是自己在 virtual box 设置端口转发时的主机端口（在视频中 wsy 设置的是 22223，jh 设置的是 22 ），虚拟机能否 ping 通 (不听课警告，wsy  在做 ssh 链接之前专门讲的)。

9. putty 第一次连接时弹出的窗口请选择“是” (不听课警告，请仔细观看视频)。

10. putty 中打开vim 鼠标右键粘贴不上，可以用 `shift+右键` ，或者参照 [此链接 ](https://www.cnblogs.com/tylf-lk/p/10133477.html)处理（特别鸣谢xhl同学）。

11. 如果遇到 `gcc `等工具不能使用的问题，请用 `sudo apt remove 工具名` 命令删除之后重装该工具（参照PA0.4），因为那段长的安装命令中间执行的过程中一旦有错误，后面的工具就不会安装，有工具没安装成功是正常现象。

12. 获取的代码 make 有问题请检查 PA0.4 安装的那些库文件是否都安装成功，如果已经安装但是不能用就删掉重装。

13. vim 安装之后能用来编辑文件就行了， PA0.5的那些特性不用全部添加，讲义中有的代码你没有是正常的。

