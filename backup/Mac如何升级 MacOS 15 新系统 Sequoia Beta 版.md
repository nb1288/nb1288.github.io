## Mac升级教程
有必要提醒一下大家，开发者测试版系统一般是给开发者测试用的，可能存在功能不完善、部分软件不兼容的情况，所以不建议普通用户升级，如果实在忍不住，升级之前记得做好备份。
### 升级方法很简单：
1. 打开苹果开发者计划官网：

-  **_https://developer.apple.com/cn/programs/_**
 
2. 点击右上角的「注册」；
![1](https://github.com/nb1288/nb1288.github.io/assets/15091534/9999453f-c70f-45b7-9742-e5bd365cd67b)

3. 点击「开始注册」，然后用你的 Apple ID 和密码直接登录就行；
![2](https://github.com/nb1288/nb1288.github.io/assets/15091534/a25aa85e-138e-41d0-a1fb-4f2fc9e7c8fd)

4. 登录成功后，打开 Mac 的「系统设置」-「通用」-「软件更新」；
5. 点击 Beta 版更新后面的 ⓘ；
6. 选择「macOS Sequoia Developer Beta」（如果没有出现，试试重启电脑），点击「完成」；
![3](https://github.com/nb1288/nb1288.github.io/assets/15091534/7c68ab97-c336-4e1e-ac63-dc9e289f1da1)

7. 点击「立即升级」；就会开始下载系统；
8. 系统下载完成后，点击「重新启动」，等待重启并开始走进度条；
9. 走完进度条之后来到新系统的登录界面，就升级完成了。
测试版系统在我的 14 寸 MacBook Pro 上使用还是很流畅的，暂时没有遇到卡顿的情况，更详细的使用体验，等我用一段时间再跟大家分享。如果你已经升级，欢迎在评论区分享使用感受。
## 黑苹果升级教程
### 安装前需要做哪些必备工作？

1.准备macOS 15 Sequoia测试版镜像，已经在网站内更新，自行前往下载即可，更新方式可以是直接增量升级也可以是老方法重来那种升级。

2.更新OpenCore引导版本至0.9.9~1.0.1，目前最高就是1.0.1开发版。其实我试过0.9.9版本更新，也可以，但是要EFI引导文件比较稳定才行。

3.使用 OCAT 这款软件屏蔽掉下图中序列号为32~35``的4款intel WIFI蓝牙驱动，原则是有则屏蔽，无则就算；
![4](https://github.com/nb1288/nb1288.github.io/assets/15091534/bf6b8af8-723b-4533-8472-496706345b12)


4.在 Misc/Security处将SecureBootModel改为Disabled （这个有争议，反正试试）；

![5](https://github.com/nb1288/nb1288.github.io/assets/15091534/21451950-1e53-4b2f-9fab-91408cb57a16)

5.在NVRAM/Add/7C436110-AB2A-4BBB-A880-FE41995C9F82/boot-args处增加参数-lilubetaall。


最后，使用OCAT更改好config.plist后，千万不要忘记保存文件哦~