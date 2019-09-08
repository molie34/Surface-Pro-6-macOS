
<h2>Surface Pro 6 黑苹果  CLOVER 配置文件,全球首发</h2>
<p>MacBook Pro之后，Surface Pro6 是我非常喜欢的一款机器，主机770g+键盘310g+笔20g = 1100g！非常轻便。基于对Surface Pro6的喜欢我做了4个教程来帮助更多Surface Pro6用户无忧折腾。</p><blockquote>
<p>Surface Pro6超详细教程一共有4个系列：</p>
<p><a href="#" target="_blank">Surface Pro 6超详细教程之安装windows10和黑苹果macOS 10.14双系统；</a></p>


<p><b>以上系列教程非授权禁止转载。</b></p>
</blockquote>

<h3>配置信息</h3>
<ul>
  <li>品牌型号：Microsoft Surface Pro 6 无风扇版</li>
  <li>CPU： Core i5-8250U</li>
  <li>显卡：UHD Graphics 620 128MB</li>
  <li>内存：8GB</li>
  <li>声卡：ALC298</li>
  <li>显示屏：LGD0555 12.3 英寸</li>
  <li>显示屏比例：3:2</li>
  <li>分辨率： 2736 x 1824</li>
  <li>硬盘：	SK HYNIX Skhynix BC501 NVMe 128GB</li>
</ul>
<h4>关于卡在田字牌解决办法：</h4>
<p>关于重启卡在田字logo界面的两种终极解决方法：

1.在win下用DG进入ESP分区，把三个.开头的目录全部删除，然后关机等20-60秒再开机就可以进入clover引导。如果还不能进入clover界面，继续强制关机之后等1分钟再开机就可以进入。

2.如果你的EFI是安装在移动设备上，强制关机后扒掉移动存储设备再插入开机即可识别。

另外在安装好黑苹果后，所有的EFI文件更新都要在macOS下进行操作就基本不会遇到这种情况，不管你的EFI安装在那个设备上。</p>

<h4>关于WiFi的解决办法：</h4>
<p>使用COMFAST USB无线网卡，型号：COMFAST CF-915AC、 COMFAST CF-811AC、COMFAST CF-WU810N</p>
<p>使用这个驱动很稳定：链接:https://pan.baidu.com/s/1aaUNqg6BJxlPxeq4WoTgSw  密码:y9b0</p>

<h4>关于蓝牙的解决办法：</h4>
<p>使用绿联的USB蓝牙（白色不带挂绳孔款 CSR8510 A10芯片），macOS系统直接免驱动，插上即可识别，可以同时多个连接键盘、鼠标、耳机，AirPods2(完美)。</p>

<h4>关于无线网卡蓝牙二合一USB设备：</h4>
	<p>悦智人心5G无线网卡蓝牙二合一usb设备经Pro6用户chase69测试反馈蓝牙无法使用</p>


<h4>关于使用USB蓝牙/无线鼠标键盘卡顿解决办法：</h4>
<p>使用一个带供电的USB3.0 集线器和一个USB2.0集线器日常使用表现良好，USB3.0 HUB(0.6米)上插1TB SSD U盘；USB2.0 HUB(0.2米)插：USB无线网卡、USB蓝牙接收器、无线鼠标/机械键盘。</p>
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/USBly.jpg" />

<p>如果你跟我一样使用的是to go系统并且会在Surface Pro6上使用，USB3.0集线器最好买RTS5411芯片带供电的，可以杜绝突然重启。</p>

<h4>触摸板启用方法：</h4>
<p>把EFI/CLOVER/OEM/Surface Pro 6/UEFI/kexts/内的VoodooI2C.kext、VoodooI2CHID.kext两个文件，放入 /System/Library/Extensions/ 目录下然后重建缓存就能完美使用触控板。</p>
<p> /System/Library/Extensions/ 在你的系统中文路径为：macOS/系统/资源库/Extensions/</p>

<h4>外接显示器模糊解决方法：</h4>
<p>请前往：<a href="https://www.jianshu.com/p/9c9dd3488597" target="_blank">Surface Pro6黑苹果外接显示器开启原生HiDPi显示效果</a> 按照教程即可一键开启HIDPI，完美解决外接显示模糊的问题。</p>
<h3>Surface Pro6 专用黑苹果镜像</h3>
<P>Surface Pro6 安装镜像：<A HREF="#" target="_blank">Surface Pro6 黑苹果镜像 macOS Mojave 10.14.6 正式版 with Clover 4968</A></p>


<p>关于10.14.4安装完后用config-Instll进入系统无限重启的，请在CLOVER界面光标移到macOS图标上按空格进入引导设置界面，选择“Block injected kexts”进入禁止加载驱动界面，选择10.14驱动目录，然后勾选“SMCBatteryManager.kext” 即可禁用电池驱动，按ESC回到主界面选择config-Intall进系统进行重建缓存。</li>

<h3>更新信息：</h3>
<p>请在macOS用Clover Configurator 打开黑苹果配置所在的EFI分区，然后删除 EFI/目录下BOOT、CLOVER 这个两个目录，再把下载好的EFI文件内BOOT、CLOVER 目录拖到系统 EFI/目录下完成更新。</p>

<p>2019/05/10：由于前段时间手里的CHIPFANCIER NANO 1TB SSD报废导致这几年存储的所有照片、设计素材等等数据都没有了。这段时间也没有心思去折腾，这两天才刚刚配好新装备做好可用的系统，特地来更新一小波。由于原CLOVER主题太大（28MB）会影响启动速度，特地设计了一个新的4K主题，整个文件大小4MB左右，默认背景可以自由更换。</p>
<ul>
  <li>2019-09-08：
  <ul>
    <li>v2.3</li>
    <li>更新 CLOVER 4968</li> 
    <li>更新macOS 10.14 - 10.14.6 全系列支持</li> 
    <li>更新macOS 10.14 - 10.14.6 全系列SD卡支持</li> 
    <li>更新AppleALC</li> 
    <li>更新Lilu</li> 
    <li>更新WhateverGreen</li> 
  </ul>
  </li>
  <li>2019-05-26：
  <ul>
    <li>v2.2</li>
    <li>更新 CLOVER 4934</li> 
    <li>支持 macOS 10.14.5</li> 
 
  </ul>
  </li>
  <li>2019-05-10：
  <ul>
    <li>v2.1</li>
    <li>更新 CLOVER 4928</li> 
    <li>更新 VirualSMC 1.0.3</li> 
    <li>加入新的默认主题 XBlue</li> 
  </ul>
  </li>

  <li>2019-04-24：
  <ul>
    <li>v2.0</li>
    <li>更新 CLOVER 4922</li> 
    <li>修复开机第二阶段驱动显卡时横向小花屏问题</li> 
    <li>增加一个Config-D-Display.plist文件，外接显示器用，可以通过调节亮度或者合上键盘盖关闭内屏</li> 
    <li>截止目前最稳定的EFI版本</li> 
  </ul>
  </li>

  <li>2019-04-22：
  <ul>
    <li>v1.9.2</li>
    <li>修复10.14.2无限重启的问题</li> 
    <li>使用原生变频</li> 
    <li>移除 CPUFriend.kext</li>
    <li>移除 CPUFriendDataProvider.kext</li>
  </ul>
  </li>

  <li>2019-04-16：
  <ul>
    <li>v1.9.1</li>
    <li>更新 VoodooI2c 2.1.5 </li>
    <li>更新 AppleALC 1.3.7</li>
    <li>更新 WhateverGreen 1.2.8</li>
    <li>加入 SMCBatteryManager.kext</li>
    <li>移除 ACPIBatteryManager.kext</li>
  </ul>
  </li>

  <li>2019-04-08：
  <ul>
    <li>v1.9</li>
    <li>更新 CLOVER 4919</li>
    <li>修复进入系统第一阶段苹果图标大小显示</li>
    <li>去除载入CLOVER前的版本提示</li>
    <li>去除默认配置文件EDID注入信息</li>
  </ul>
  </li>

  <li>2019-04-02：
  <ul>
    <li>v1.8</li>
    <li>更新 CLOVER 4915</li>
    <li>更新 drivers64UEFI 驱动
        <ul>
          <li>添加 AudioDxe-64.efi</li>
        </ul>
    </li>

  </ul>
  </li>
  <li>2019-03-31：
  <ul>
    <li>v1.7</li>
    <li>更新 CLOVER 4912</li>
    <li>更新 liu 1.3.5</li>
    <li>更新 AppleALC 1.3.6</li>
    <li>更新 USBInjectAll 0.7.1</li>
    <li>取消最低800MHz档位变频</li>
    <li>重新生成新变频文件</li>

  </ul>
  </li>
  <li>2019-03-29：
  <ul>
    <li>v1.6</li>
    <li>更新 CLOVER 4910</li>
    <li>修复亮度保存</li>
    <li>精简并更新 drivers64UEFI
        <ul>
          <li>去除 AudioDxe-64.efi</li>
          <li>去除 Fat-64.efi</li>
          <li>去除 UsbKbDxe-64.efi</li>
          <li>去除 UsbMouseDxe-64.efi</li>
          <li>去除 VBoxHfs-64.efi</li>  
          <li>更新 EmuVariableUefi-64.efi</li> 
          <li>更新 HFSPlus.efi</li> 
        </ul>
      </li>
    <li>去除 CodecCommander.kext</li>
    <li>去除 VoodooPS2Controller.kext</li>
    <li>增加 VoodooI2C.kext</li>
    <li>增加 VoodooI2CHID.kext</li>
    <li>VoodooI2C.kext、VoodooI2CHID.kext两个文件，放入 /System/Library/Extensions/ 目录下然后重建缓存就能使用触控板</li>
  </ul>
  </li>
  <li>2019-03-26:
   <ul>
     <li>v1.5</li>
     <li>更新CLOVER 4903</li>
     <li>支持10.14.4正式版</li>
     <li>安装10.14.4更新过程中重启多次的时候必须选择config-Install配置文件，等更新完成进入系统后一定要重建缓存，重建缓存完成后就可以重启使用默认配置文件进入系统</li>
   </li>
   </ul>
  </li>
  <li>2019-03-22:
   <ul>
     <li>v1.4</li>
     <li>更新CLOVER 4901</li>
     <li>默认启动系统为macOS，请确保你按照教程把macOS分区名称格式为macOS，否则你需要自行修改</li>
  
  </ul></li>

  <li>2019-03-15:
  <ul>
    <li> v1.3</li>
    <li> 更新CLOVER 4896</li>
  </ul>
  </li>
  <li>2019-02-24:
    <ul>
      <li>v1.2</li>
      <li>仿冒一个无用的en0网卡，使USB无线网卡可以通过Apple ID验证</li>
    </ul>
  </li>  
  <li>2019-02-23:
   <ul><li>v1.1</li></ul></li>
  <li>2019-02-21:
      
   <ul><li>v1.0</li></ul></li>
   </li>
</ul>

<h3>目前完成：</h3>
<ul>
  <li>内屏显示内建正常；</li>
  <li>亮度调节正常；</li>
  <li>外接HDMI正常，可以同时使用内屏；</li>
  <li>ALC298内建正常；</li>
  <li>内置SD卡槽正常；</li>
  <li>休眠睡眠唤醒正常；</li>
  <li>内建假冒en0网卡；</li>
  <li>Siri使用正常；</li> 
  <li>iCloud登陆正常；</li>
  <li>App Store登陆正常，下载正常；</li>
  <li>iMessage登陆正常</li>
  <li>电源按键正常，按三秒显示关键菜单，按一秒开关屏幕</li>  
  <li>触控板正常</li> 
  </ul>

<h3>未进行项目：</h3>
<ul>
<li>音量+-按键；</li>
<li>电量显示；</li>
<li>全球暂时无解：触摸屏、内置蓝牙、内置WiFi、摄像头；</li>
<li>期待你的完善分享！</li>
</ul>

<h3>系统截图</h3>
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/1.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/2.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/3.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/4.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/5.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/6.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/7.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/8.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/9.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/10.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/11.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/12.jpg" />

<h3>感谢</h3>
<p>感谢以下人员提供的经验、测试、反馈帮助：</p>
<p>xjzkp、13956737563、CabbSir、9805xinwen、radonjaw、chase69、Fnckerpoi </p>
<p>感谢各位开发黑苹果驱动的大神。</p>
<p>最后感谢翔哥。</p>
