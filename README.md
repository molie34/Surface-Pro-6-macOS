
<h1>Surface Pro 6 黑苹果  CLOVER 配置文件,全球首发</h1></br>


<P>Surface Pro 6 的UEFI BIOS和别的机型BIOS相比较处在一个很特殊的地位，我光是为了解决卡++++++++就花了将近一个月，总过花了一个月17天终于解决了UHD620内屏黑屏的问题！这背后总共试验了1200多次试错，我也收获了对surface pro系列的一些特性了解，整个折腾过程我很享受。</P>

<p>MacBook Pro之后，Surface Pro6 是我非常喜欢的一款机器，它结束了我以前MacBook + iPad的日子，看超高清PDF书籍做笔记和日常系统应用都可以在一个机器上完成，而且重量加上键盘和笔也就770g+310g+20g = 1100g！出差背着一点都不重，超级喜欢，可惜都已经9012年了Apple也没有这样的机器。基于对Surface Pro6的喜欢我做了4个教程来帮助更多Surface Pro6用户无忧折腾。</p><blockquote>
<p>Surface Pro6超详细教程一共有4个系列：</p>
<p><a href="https://www.jianshu.com/p/a5217b200053" target="_blank">Surface Pro 6超详细教程之安装windows10和黑苹果macOS 10.14双系统；</a></p>
<p><a href="https://www.jianshu.com/p/179477882133" target="_blank">Surface Pro 6超详细教程之安装黑苹果macOS 10.14单系统；</a></p>
<p><a href="https://www.jianshu.com/p/6eb827ab5e9a" target="_blank">Surface Pro 6超详细教程之恢复Surface Pro6 windows10系统；</a></p>
<p><a href="https://www.jianshu.com/p/d1b41d913f91" target="_blank">Surface Pro 6超详细教程之下载Surface Pro6 系统恢复镜像并制作系统恢复U盘。</a></p>
<p><b>以上系列教程非授权禁止转载。</b></p>
</blockquote>

<h2>配置信息</h2>
<ul>
  <li>品牌型号：Microsoft Surface Pro 6 无风扇版</li>
  <li>CPU： Core i5-8250U</li>
  <li>显卡：UHD Graphics 620 128MB</li>
  <li>内存：8GB</li>
  <li>声卡：ALC298</li>
  <li>无线网卡：Marvell Marvell AVASTAR Wireless-AC Network Controller</li>
  <li>显示屏：LGD0555 12.3 英寸</li>
  <li>显示屏比例：3:2</li>
  <li>分辨率： 2736 x 1824</li>
  <li>硬盘：	SK HYNIX Skhynix BC501 NVMe 128GB</li>
</ul>
<h2>关于WiFi的解决办法：</h2>
<p>使用COMFAST USB无线网卡即可，具体型号：COMFAST CF-915AC</p>
<p>使用这个驱动很稳定：链接:https://pan.baidu.com/s/1aaUNqg6BJxlPxeq4WoTgSw  密码:y9b0</p>

<h2>关于蓝牙的解决办法：</h2>
<p>使用某联或者CSR芯片的USB蓝牙即可，绿联的蓝牙是免驱动的插上去直接识别，我目前也有这个设备，可以连接键盘、鼠标、耳机，AirPods2(完美)。</p>


<h2>关于使用USB蓝牙/无线鼠标键盘卡顿解决办法：</h2>
<p>目前我使用一个带供电的USB3.0 集线器和一个USB2.0集线器日常使用表现良好，USB3.0 HUB(0.6米)上插1TB SSD U盘；USB2.0 HUB(0.2米)插：USB无线网卡、USB蓝牙接收器、无线鼠标/机械键盘。USB3.0 HUB+ USB3.0 HUB这种模式尝试过，即使带供电一样表现很糟糕。</p>
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/USBly.jpg" />

<p>如果你跟我一样使用的是to go系统并且会在Surface Pro6上使用，USB3.0集线器最好买RTS5411芯片带供电的，可以杜绝突然重启。</p>


<h2>Surface Pro6 专用黑苹果镜像</h2>
<P>Surface Pro6 安装镜像：<A HREF="https://www.jianshu.com/p/560659017a7f" target="_blank">Surface Pro6 黑苹果镜像 macOS Mojave 10.14.4 正式版 with Clover 4919</A></p>
<P>Surface Pro6 安装镜像：<A HREF="https://www.jianshu.com/p/65b9207276fd" target="_blank">Surface Pro6 黑苹果镜像 macOS Mojave 10.14.2 正式版 with Clover 4877</A></p>
<h2>更新信息：</h2>
<p>请在macOS用Clover Configurator 打开黑苹果配置所在的EFI分区，然后删除 EFI/目录下BOOT、CLOVER 这个两个目录，再把下载好的EFI文件内BOOT、CLOVER 目录拖到系统 EFI/目录下完成更新。</p>

<ul>
  <li>2019-04-22：
  <ul>
    <li>v1.9.2</li>
    <li>修复10.14.2无限重启的问题</li> 
    <li>使用原生变频</li> 
    <li>移除 CPUFriend.kext</li>
    <li>移除 CPUFriendDataProvider.kext</li>
    <li>关于10.14.4安装完后用config-Instll进入系统无限重启的，请在CLOVER界面光标移到macOS图标上按空格进入引导设置界面，选择“Block injected kexts”进入禁止加载驱动界面，选择10.14之后禁用“SMCBatteryManager.kext” 电池驱动即可进入系统进行重建缓存。</li>
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
    <li>添加 ACPIBatteryManager.kext 1.90.1,完善触控板设置，由CabbSir测试发现，经过测试截止目前Surface Pro6 的触控板已经完美</li>
    <li>虽然添加了电池驱动，但是没有做任何电池和电源适配器修复，如果发现无法进入系统，请在COVER 界面设置禁止加载ACPIBatteryManager.kext 即可重新进入系统</li>
    <li>如果你有任何分享请在Issues提交问题，个人的精力实在有限</li>
    

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
    <li>重新生成新变频，档位在13-16档左右，最低档位1300 MHz、i5处最高档位3400 MHz，i7最高档位4200 MHz</li>

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
    <li>kexts目录加入了两个文件：VoodooI2C.kext、VoodooI2CHID.kext，这两个文件为论坛Pro5 兄弟编译的，只要放入 /System/Library/Extensions/ 目录下然后重建缓存就能使用两指和三指触控板手势，四指触控手势</li>

  </ul>
  </li>
  <li>2019-03-26:
   <ul>
     <li>v1.5</li>
     <li> 更新CLOVER 4903</li>
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
      <li> 加入R神的SSDT，仿冒一个无用的en0网卡，使用USB无线网卡可以通过Apple ID验证</li>
    </ul>
  </li>  
  <li>2019-02-23:
   <ul><li>v1.1</li></ul></li>
  <li>2019-02-21:
      
   <ul><li>v1.0</li></ul></li>
   </li>
</ul>
<h2>macOS 版本：</h2>

<ul><li>macOS 10.14 - macOS 10.14.4，我目前使用macOS 10.14.4正式版</li></ul>
<h2>CLOVER版本：</h2>
<img src="https://github.com/molie34/Surface-Pro-6-macOS/blob/master/images/0.jpg" />
<ul><li>CLOVER 4915</li>
   
</ul>

<h2>目前完成：</h2>
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

<h2>未进行项目：</h2>
<ul>
<li>音量+-按键；</li>
<li>电量显示；</li>
<li>摄像头；</li>
<li>全球暂时无解：触摸屏、内置蓝牙、内置WiFi；</li>
<li>期待你的完善分享！</li>
</ul>
<h2>EFI文件：</h2>
<h5>config文件、kexts、SSDT文件都在EFI/CLOVER/OEM/Surface Pro 6/UEFI/内。</H5>

<H5>config文件有三个：</h5>
<ul>
  <li>config.Plist</li>
  <li>config-Install.Plist</li>
  <li>config-out-Display.Plist</li>
</ul>
<p>理论上默认的config.Plist配置文件应该能治疗目前所有八代UHD620高分内屏黑屏！</span></p>

<H2>安装过程:</H2>
使用config-Install.Plist 文件进行全程安装，安装完成后先用这个配置文件进系统使用kexts Uiltiy 进行重建缓存，然后重启使用默认配置文件即可驱动内屏！</br>
<h4>特别提示：</h4>
如果重建缓存之后重启跑玩-v代码后重启的，那么选择congfig-out-Dispaly.Plist 这个配置文件，然后连接上显示器就可以正常进入驱动后的系统，然后再一次重建缓存，重启之后使用默认配置文件就可以驱动内屏了！</br>
<h2>系统截图</h2>
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

<h2><a class="anchor" id="user-content-感谢" aria-hidden="true" href="#感谢"><svg xmlns="http://www.w3.org/2000/svg" class="octicon octicon-link" aria-hidden="true" viewBox="0 0 16 16" width="16" height="16" version="1.1"><path fill-rule="evenodd" d="M 4 9 h 1 v 1 H 4 c -1.5 0 -3 -1.69 -3 -3.5 S 2.55 3 4 3 h 4 c 1.45 0 3 1.69 3 3.5 c 0 1.41 -0.91 2.72 -2 3.25 V 8.59 c 0.58 -0.45 1 -1.27 1 -2.09 C 10 5.22 8.98 4 8 4 H 4 c -0.98 0 -2 1.22 -2 2.5 S 3 9 4 9 Z m 9 -3 h -1 v 1 h 1 c 1 0 2 1.22 2 2.5 S 13.98 12 13 12 H 9 c -0.98 0 -2 -1.22 -2 -2.5 c 0 -0.83 0.42 -1.64 1 -2.09 V 6.25 c -1.09 0.53 -2 1.84 -2 3.25 C 6 11.31 7.55 13 9 13 h 4 c 1.45 0 3 -1.69 3 -3.5 S 14.5 6 13 6 Z" /></svg></a>感谢</h2>
<ul>
<li><a href="https://github.com/RehabMan">RehabMan</a> 提供 <a href="https://github.com/RehabMan/HP-ProBook-4x30s-DSDT-Patch/tree/master/kexts/AppleBacklightInjector.kext">AppleBacklightInjector</a> 和 <a href="https://github.com/RehabMan/EAPD-Codec-Commander">EAPD-Codec-Commander</a> 和 <a href="https://github.com/RehabMan/OS-X-ACPI-Battery-Driver">OS-X-ACPI-Battery-Driver</a> 和 <a href="https://github.com/RehabMan/OS-X-Clover-Laptop-Config">OS-X-Clover-Laptop-Config</a> 和 <a href="https://github.com/RehabMan/OS-X-FakeSMC-kozlek">OS-X-FakeSMC-kozlek</a> 和 <a href="https://github.com/RehabMan/OS-X-USB-Inject-All">OS-X-USB-Inject-All</a> 和 <a href="https://github.com/RehabMan/OS-X-Voodoo-PS2-Controller">OS-X-Voodoo-PS2-Controller</a> 和 <a href="https://github.com/RehabMan/OS-X-BrcmPatchRAM">OS-X-BrcmPatchRAM)</a> 的维护</li>
<li><a href="https://github.com/vit9696">vit9696</a> 提供 <a href="https://github.com/acidanthera/Lilu">Lilu</a> 和 <a href="https://github.com/acidanthera/AppleALC">AppleALC</a> 和 <a href="https://github.com/acidanthera/WhateverGreen">WhateverGreen</a> 和 <a href="https://github.com/acidanthera/VirtualSMC">VirtualSMC</a>  和 <a href="https://github.com/acidanthera/VirtualSMC">VirtualSMC</a> 的维护</li>
<li><a href="https://github.com/alexandred">alexandred</a> 和 <a href="https://github.com/hieplpvip">hieplpvip</a> 提供 <a href="https://github.com/acidanthera/AirportBrcmFixup">AirportBrcmFixup</a> 的维护</li>
</ul>
