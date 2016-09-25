```
netsh wlan show drivers
netsh wlan set hostednetwork mode=allow ssid=qwerty26256 key=qwerty1943
netsh wlan set hostednetwork mode=disallow
netsh wlan start hostednetwork
netsh wlan stop hostednetwork
```
#1.
首先以管理员身份运行`cmd.exe`

输入命令`netsh wlan show drivers`，确认是否支持承载网络

在显示的一大段文字中找到 **“支持的承载网络：”**

如果显示**“是”**，恭喜

如果显示**“否”**，则本方法不适用，请关闭窗口并删除此文件

不要关闭`cmd.exe`窗口
#2.
输入命令`netsh wlan set hostednetwork mode=allow ssid=****** key=******`

mode：是否启用虚拟Wifi网卡，allow为启用，disallow为禁用，虚拟网卡即会消失

ssid：指定你自己喜欢的无线网络的名称，此处以\*\*\*\*\*\*代替；最好为英文

key：指定无线网络的密码，此处以\*\*\*\*\*\*代替；该密码用于对无线网进行安全的WPA2加密，能够很好的防止被蹭网

以上三个参数可以单独使用，例如使用`netsh wlan set hostednetwork mode=disallow`可以直接禁用虚拟Wifi网卡

不要关闭`cmd.exe`窗口
#3.
输入命令`netsh wlan start hostednetwork`

打开：控制面板-网络和共享中心-更改适配器设置

（不管你用什么方法，进入控制面板-网络和 Internet-网络连接就行）

找到“虚拟Wi-Fi”或者“Virtual Wi-Fi”或者任何有虚拟意思的连接，说明设置成功

找到现有有线上网方式连接，比如宽带拨号方式为“宽带连接 WAN微型端口PPPOE”、VPN为“VPN连接”、局域网为“以太网”或“局域网”

右键单击现有上网方式-属性

打开属性-选择共享选项卡，勾选“允许其他网络用户通过此计算机的Internet连接”

在下方下拉框选择虚拟意思的连接名称，单击确定

不论出现什么提示信息，都确定

不要关闭`cmd.exe`窗口
#4.
输入命令`netsh wlan stop hostednetwork`

输入命令`netsh wlan start hostednetwork`

关闭一切窗口

ok一切大功告成，赶快邀请你的朋友搜索自己亲手建立起来的Wlan吧

#提示：
每次使用前要在cmd中输入命令`netsh wlan start hostednetwork`。可以新建一个空文本文件，输入`netsh wlan start hostednetwork`并保存，将文件名和后缀名命名为“Wlan Start.bat”，每次使用前右键单击以管理员身份运行即可；同理可得“Wlan Stop.bat”。

可能出现的问题：

在cmd中输入命令`netsh wlan start hostednetwork`或运行bat文件时，会出现以下提示：“无法启动承载网络。组或资源的状态不是执行请求操作的正确状态”

解决：

右键单击“计算机”或“我的电脑”-属性

进入左上角“设备管理器”

（不管你用什么方法，进入设备管理器就行）

找到网络适配器下的无线网硬件，右键-禁用，再右键-启用

之后再按上述步骤设置一遍即可。