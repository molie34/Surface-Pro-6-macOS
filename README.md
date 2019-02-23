<h1>Surface Pro 6 黑苹果  CLOVER 配置文件,全球首发</h1></br>
<P>Surface Pro 6 的UEFI BIOS和别的机型BIOS相比较处在一个很特殊的地位，我光是为了解决卡++++++++就花了将近一个月，总过花了一个月17天终于解决了UHD620内屏黑屏的问题！这背后总共试验了1200多次试错，我也收获了对surface pro系列的一些特性了解，整个折腾过程我很享受。</P>


<P>很感谢<A HREF="https://github.com/gdllzkusi/hackintosh--lenovo-Yoga-3-Pro-1370" target="_blank">hackintosh--lenovo-Yoga-3-Pro-1370</A>！,在他提供的经验帮助之上，我修改了适合Pro6 的配置文件最终实现了Surface Pro6 内屏的完美，在没有修复内屏之前我都是使用外接显示器来使用macOS，现在也可以成功使用内屏。这里也要感谢制作DVMT补丁的作者、感谢为黑苹果做出过努力的大神，感谢你们的教程。</P>

远景论坛查看帖子：<A HREF="http://bbs.pcbeta.com/viewthread-1806047-1-1.html" target="_blank">Surface Pro6 黑苹果</A>

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
<h2>更新信息：</h2>
<ul>
  <li>暂无。</li>
</ul>
<h2>macOS 版本：</h2>

<ul><li>macOS 10.13.6 - macOS 10.14.x，我目前使用macOS 10.14.2正式版</li></ul>
<h2>CLOVER版本：</h2>
<img src="https://github.com/molie34/Surface-Pro-6/blob/master/images/0.jpg" />
<ul><li>CLOVER 4877</li>
   
</ul>
<h2>SMC版本：</h2>
<ul><li>使用VirtualSMC 1.2.7</li></ul>
<h2>目前完成：</h2>
<ul>
  <li>内屏显示内建正常；</li>
  <li>亮度调节正常；</li>
  <li>外接HDMI正常，可以同时使用内屏；</li>
  <li>ALC298内建正常；</li>
  <li>休眠睡眠唤醒正常；</li>
  <li>使用原装网线转接卡正常使用en0，同时可以使用外置USB网卡en1；</li>
  <li>iCloud登陆正常；</li>
  <li>App Store登陆正常，下载正常；</li>
  <li>iMessage登陆正常</li>
  </ul>
TPS：我没有使用代码仿冒一个无用的en0，我是先装好系统后，首先使用Apple 有线转接网卡进行联网，此时系统自动内建en0，然后再安装外置USB网卡驱动即为en1。
<h2>未进行项目：</h2>
<ul>
<li>音量+-按键；</li>
<li>触控板；</li>
<li>摄像头；</li>
<li>内置SD卡槽；</li>
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
<img src="https://github.com/molie34/Surface-Pro-6/blob/master/images/1.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6/blob/master/images/2.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6/blob/master/images/3.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6/blob/master/images/4.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6/blob/master/images/5.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6/blob/master/images/6.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6/blob/master/images/7.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6/blob/master/images/8.jpg" />
<img src="https://github.com/molie34/Surface-Pro-6/blob/master/images/9.jpg" />


<h2><a class="anchor" id="user-content-感谢" aria-hidden="true" href="#感谢"><svg xmlns="http://www.w3.org/2000/svg" class="octicon octicon-link" aria-hidden="true" viewBox="0 0 16 16" width="16" height="16" version="1.1"><path fill-rule="evenodd" d="M 4 9 h 1 v 1 H 4 c -1.5 0 -3 -1.69 -3 -3.5 S 2.55 3 4 3 h 4 c 1.45 0 3 1.69 3 3.5 c 0 1.41 -0.91 2.72 -2 3.25 V 8.59 c 0.58 -0.45 1 -1.27 1 -2.09 C 10 5.22 8.98 4 8 4 H 4 c -0.98 0 -2 1.22 -2 2.5 S 3 9 4 9 Z m 9 -3 h -1 v 1 h 1 c 1 0 2 1.22 2 2.5 S 13.98 12 13 12 H 9 c -0.98 0 -2 -1.22 -2 -2.5 c 0 -0.83 0.42 -1.64 1 -2.09 V 6.25 c -1.09 0.53 -2 1.84 -2 3.25 C 6 11.31 7.55 13 9 13 h 4 c 1.45 0 3 -1.69 3 -3.5 S 14.5 6 13 6 Z" /></svg></a>感谢</h2>
<ul>
<li><a href="https://github.com/RehabMan">RehabMan</a> 提供 <a href="https://github.com/RehabMan/HP-ProBook-4x30s-DSDT-Patch/tree/master/kexts/AppleBacklightInjector.kext">AppleBacklightInjector</a> 和 <a href="https://github.com/RehabMan/EAPD-Codec-Commander">EAPD-Codec-Commander</a> 和 <a href="https://github.com/RehabMan/OS-X-ACPI-Battery-Driver">OS-X-ACPI-Battery-Driver</a> 和 <a href="https://github.com/RehabMan/OS-X-Clover-Laptop-Config">OS-X-Clover-Laptop-Config</a> 和 <a href="https://github.com/RehabMan/OS-X-FakeSMC-kozlek">OS-X-FakeSMC-kozlek</a> 和 <a href="https://github.com/RehabMan/OS-X-USB-Inject-All">OS-X-USB-Inject-All</a> 和 <a href="https://github.com/RehabMan/OS-X-Voodoo-PS2-Controller">OS-X-Voodoo-PS2-Controller</a> 和 <a href="https://github.com/RehabMan/OS-X-BrcmPatchRAM">OS-X-BrcmPatchRAM)</a> 的维护</li>
<li><a href="https://github.com/vit9696">vit9696</a> 提供 <a href="https://github.com/acidanthera/Lilu">Lilu</a> 和 <a href="https://github.com/acidanthera/AppleALC">AppleALC</a> 和 <a href="https://github.com/acidanthera/WhateverGreen">WhateverGreen</a> 和 <a href="https://github.com/acidanthera/VirtualSMC">VirtualSMC</a>  和 <a href="https://github.com/acidanthera/VirtualSMC">VirtualSMC</a> 的维护</li>
<li><a href="https://github.com/alexandred">alexandred</a> 和 <a href="https://github.com/hieplpvip">hieplpvip</a> 提供 <a href="https://github.com/acidanthera/AirportBrcmFixup">AirportBrcmFixup</a> 的维护</li>
</ul>
