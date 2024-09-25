# Matebook-D14/D15-2020-OpenCore 黑苹果 hackintosh  
  

readme in other language:  
[中文🇨🇳](README.md) | [English🇬🇧](readme-en.md)   


  
```diff 
此repo内含EFI可用于2020版华为MateBook D14以及D15的intel版本
```

姐妹项目:  
[Matebook-x-pro-2019-OpenCore 黑苹果 hackintosh  ](https://github.com/ske1996/Matebook-x-pro-2019-Hackintosh-newest)  
[MateBook 13/14 OpenCore 黑苹果](https://github.com/ske1996/matebook-13-2019-oc-efi)  
[matebook-x-2020-Hackintosh-OpenCore-黑苹果   ](https://github.com/ske1996/matebook-x-2020-Hackintosh-OpenCore)  


如果你遇到了什么问题（与安装无关的），有可能在这里找到答案：[issues](https://github.com/ske1996/Matebook-D14-2020-hackintosh/issues)  

请在这个网页的最右上角帮我点颗小星星⭐️哟  




<details>  
<summary>⭐️点击查看如何在黑苹果下玩所有3A大作（matebook D14的黑苹果🉑️）</summary>  
    
  
  
  
 ⚠️在注册的时候填写邀请码：DBZNT3EC  
！！可以白嫖3小时！！
  
       
      
我自己用的一个云电脑服务  
挺好用的能玩游戏（包括3A） 
也就是说在matebook的黑苹果上也可以无硬件限制的玩任何游戏了  
直接4K全画质的开  
没啥延迟，就跟在本地玩一样  
我自己用的，推荐使用这个，这样在mac玩游戏也解决了  
  
⚠️在注册的时候填写邀请码：DBZNT3EC  
！！可以白嫖3小时！！
  
  
  
[点击进入它的官网](https://www.haixingcloud.com/#/Home)  
  

</details>   



## 更新日志（⚠️一定先看这个）  
<details>  
<summary>点击以查看详细信息</summary>  
  

- 20210506:  
合并了Catalina跟BigSur的EFI,尝试修复了drm以及sidecar问题，尝试优化了缓冲帧参数  

- 20210223:  
添加了一个Matebook D15 2020 pm981 专用的efi，一切正常  


- 20201205:  
关了sip  
以及设置安全模式为默认  

- 20201117:  
更新至oc 0.6.4，删除了一些不必要的东西，更新了所有我认为有必要更新的驱动  
  
  
- 20201012:    
修复了唤醒后色彩失真的问题，本次缓冲帧部分来自于[@Shaopeng](https://github.com/gongshaopeng0828)  

- 20201011:  
尝试修复了hdmi问题，目前hdmi可用，但是可能唤醒后会导致色彩失真的问题，可以尝试去偏好设置，显示器，色彩的位置做调整  
另外感谢[@Shaopeng](https://github.com/gongshaopeng0828)帮忙测试  

- 20200917:  
使用了Z大的最新AirportItlwm的wifi驱动，跟heliport说拜拜啦，今后可以原生切换wifi了，另将oc升级至0.6.1  
bigsur跟catalina需要对号入座，不可串着用  

- 20200904:  
上传了根据OC官方版制成的efi  
  
  
</details>   

<details>  
<summary>About booting MacOS 12 Monterey</summary>  

【Yes,we can boot it.】  

Whatever you want to upgrade your hackintosh from BigSur,or new-installing.

need to do:  
upgrade your lilu and replace your airportitlwm and intelbluetoothfirmware to lastest ones,
disable intelbuletoothinjector and add bluetoolfix to oc/kexts/ and config.plist.
then,OTA or new-installing your OS with apple's guide.

Every thing works like in BigSur,but need to replace some kext.

My experience: [click this](https://github.com/ske1996/matebook-13-2019-oc-efi/issues/155)  


   
</details> 


**Supported BigSur and Monterey already**  

## 正常可用的部件：
**以下的【蓝牙】【WIFI】【HDMI】的文字可点击后查看详情**   

<details>  
<summary>1.蓝牙</summary>   
  
驱动作者[@zxystd](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)  
1. 华为的蓝牙鼠标不可用！！！  
2. 苹果的妙控2可用   
3. 亲眼所见，微软设计师鼠标可用[淘宝链接](https://detail.tmall.com/item.htm?id=575557854943&spm=a1z09.2.0.0.119c2e8dUqx3iI&_u=bkg3nm2911&sku_properties=5919063:6536025)  
4. 亲眼所见，型号为thinkpad 0a36193（SMB）的蓝牙鼠标可用，购买选“蓝牙无线激光”，[京东链接-移动端](https://item.m.jd.com/product/748175.html?utm_campaign=t_1001328990)  
5. Airpods可以用，但是你得配对一次，我们又不是白苹果，不能开盖就用  
6. 以下几个蓝牙鼠标根据群友测试说可用，但是我没亲眼所见，要是买了发现不能用别怪我  
----雷柏m200g/刺鳞树蝰/罗技m336/微软sculpt/英菲克/飞利浦spk7355  

</details>   

  
<details>  
<summary>2.WIFI</summary>  
  
1. 使用了Z大的最新AirportItlwm的wifi驱动，跟heliport说拜拜啦  


2. 驱动作者[@zxystd](https://github.com/OpenIntelWireless/itlwm)  

3. Airdrop和无线的随航不可用，随航需要插线用，handoff可用但有时不太稳定，可以用apple watch解锁mac，但是有时不稳定  
4. Wi-Fi觉得不好使的去上面我写出来的作者的repo里更新驱动
5. Wi-Fi连接要尽可能的去连5ghz的
6. 从Windows切换过来MacOS发现wifi没法用就关机，10s后再开机

</details>   

3.睡眠正常  

4.触摸板可用  

<details>  
<summary>5.HDMI可用 </summary>  

感谢[@Shaopeng](https://github.com/gongshaopeng0828)帮忙测试  

</details> 

6.解锁cfg lock后可完美原生电源管理

7.已注入缓冲帧 核显正常

8.cpu变频正常（补充：此efi内涵cpufriend，设置为：1800mhz，最高性能）

9.键盘快捷键正常  

10.耳机接口正常（需要使用下面的【安装ComboJack实现耳机耳麦切换，改进电流声】）
  
  
## 无法正常工作的部件：  


1.摄像头  

2.独显  




  
## 个人使用版本信息等   
<details>  
<summary>点击以查看详细信息</summary>  
oc版本0.6.0

自用macos版本：10.15.5 Catalina    

matebook D14 2020 i5-10210U  

</details>  

## 有关安装： 
  

⚠️事前准备：f2进bios，调成中文，然后关闭一切带有“安全”的东西，保存，退出  

<details>  
<summary>⚠️事前准备2：安装前先定制三码（点击查看详情）</summary>  
因为很多人都不替换自己的三码就用，所以导致苹果账号服务受限的情况比比皆是，因此，我把config设置为“如果不改三码就用，那直接无法启动”  
具体修改三码的教程自己百度，自己编辑config。（p.s.其实应该四码，包含：SSN，MLB，ROM，UUID） 
  
windows下编辑config的工具：[ProperTree-windows.zip](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ProperTree-windows.zip)  
  
  
</details>  

镜像下载链接：https://blog.daliansky.net/  

OC官方教程:https://dortania.github.io/OpenCore-Install-Guide/  
  







  
  



## 安装后：  

<details>  
<summary>⚠️注意事项</summary>  
⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️  
  
1.不要用oc引导windows，因为你弄不好你的正版软件许可证就全没了  
直接oc的选择系统界面里通过ctrl+回车选择mac的引导磁盘  
设置mac为默认引导磁盘，关闭config里，showpicker  
引导windows用f12选windows  


2.一定要先改三码再用，具体的教程自己百度  

3.icloud中的查找我的mac不要打开  

4.安全与隐私中的文件保险箱不要打开  

5.再任何系统，任何OS下都要杜绝热启动，意思是重启的话一律先选关机再用开机键开机  
无论是单个系统下的重启需求或者是想要重启切换系统，都不要选重启选项，一律先选关机再用开机键开机  
不然有可能会导致蓝牙，触控板，Wi-Fi失灵问题。  


</details>  

<details>  
<summary>安装ComboJack实现耳机耳麦切换，改进电流声。（修复耳机接口）</summary>   
  
参考： 

![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5q01OKCJFpwjG8DeWk34ZAk2FSNjwQUoIN0*GZw*WPuJGXoFx6QKbikJBN0lMTsBAB*.2jRAK8HeEs9KtxTHRjs!/b&bo=SAdMAgAAAAADByM!&rf=viewer_4)



在这里下载由Heporis制作的ComboJack.

https://github.com/randomprofilename/ComboJack


终端运行下面路径的脚本
```bash
ComboJack_Installer/install.sh
```
  
</details>

  
  
<details>  
<summary>解锁CFG</summary>  

⚠️关于解锁cfg后能做到什么？  
完美的电源管理  
CPU完美变频  
完美睡眠（我个人经验：睡眠6H只掉了1%的电）  
⚠️以下教程的cfg lock偏移地址提取自matebook d14 2020款  
其他的需要自行提取bios并自行分析，核对偏移地址  
如因以下教程修改导致的一切后果，本人不予承担责任，下载本repo中任何一个文件视为同意以上条款  


以下教程来自：  
https://zhuanlan.zhihu.com/p/121655468

先去华为官网升级bios至1.19

然后找偏移地址就不用做了，我告诉你，就是0x3E  

【⚠️千万不要用oc去引导ru！！】懂得人自然懂，收起那个想法，老老实实按我下面写的来  
⚠️以下教程的cfg lock偏移地址提取自matebook d14 2020款  
其他的需要自行提取bios并自行分析，核对偏移地址  
如因以下教程修改导致的一切后果，本人不予承担责任，下载本repo中任何一个文件视为同意以上条款  


- U盘准备阶段：  
（大小无所谓）  

1.先准备一个u盘，格式化为fat32  
2.u盘里创建文件夹：EFI  
3.打开EFI文件夹，在里面创建文件夹BOOT  
4.复制[cfgunlock.zip(点击下载)](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/cfgunlock.zip)里面的bootx64.efi进U盘的EFI/BOOT下  
5.关机后开机按F12使用这个U盘去引导，然后进入修改bios底层阶段  

- 以下为修改bios底层阶段：  
1. 进入后 ‘alt’ + ’=‘ 切换进 ACPI Variable  
2. 用pageup/pagedown/上下方向键找到 CPUSetup  
3. 回车进入然后用上下左右方向键找到对应的地址（也就是0x3e，那么就是纵坐标03，横坐标0e的位置）  
![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5q01OKCJFpwjG8DeWk34ZAl40wvQBwENCvcC8AXw3U9pLndZFaQGhnrwveoEM7FzByVHyIsV*u1nI.1JoXvOXOA!/b&bo=0AIQAgAAAAABB.A!&rf=viewer_4)  
4. 一看，确实是0x01，那么回车，输入0 就可以看到它变成了0  
5. 使用'crtl' + 'w' 来保存 保存的时候屏幕上会直接显示update written 的，这说明已经写入了  
6. 使用'alt' + 'q' 来退出，然后即可回到引导进入系统了，CFG已经解锁  


修改完成后可以再用那个u盘引导启动一次，查看是否修改成功  
然后我建议使用[propertree](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/ProperTree.zip)修改EFI分区中的EFI/OC/config.plist的kernel/add/quirks为下图所示  
![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5mhOVTuQ0sSbBPmet1ZSU1zDz7zUBccaFytwrKxAqPz4ygQph98Mo9E5.JjYf6DFuuWhDZs8DFFN1ujnFI9OIz4!/b&bo=wASKAwAAAAADB28!&rf=viewer_4)  



</details> 

  
<details>  
<summary>修改dvmt至64mb</summary>  
    
  ⚠️关于修改dvmt后能做到什么？  
  可以hdmi/dp输出4k60p的信号了  
  
  
⚠️以下教程的cfg lock偏移地址提取自matebook d14 2020款  
其他的需要自行提取bios并自行分析，核对偏移地址  
如因以下教程修改导致的一切后果，本人不予承担责任，下载本repo中任何一个文件视为同意以上条款  

- U盘准备阶段：  
（大小无所谓）  

1.先准备一个u盘，格式化为fat32  
2.u盘里创建文件夹：EFI  
3.打开EFI文件夹，在里面创建文件夹BOOT  
4.复制[cfgunlock.zip(点击下载)](https://github.com/ske1996/matebook-13-2019-oc-efi/raw/master/cfgunlock.zip)里面的bootx64.efi进U盘的EFI/BOOT下  
5.关机后开机按F12使用这个U盘去引导，然后进入修改bios底层阶段  

- 以下为修改bios底层阶段：  
1. 进入后 ‘alt’ + ’=‘ 切换进 ACPI Variable  
2. 用pageup/pagedown/上下方向键找到 SaSetup  
3. 进入SaSetup后，然后用crtl加pagedown翻到下一页找到左侧横坐标0100，如下图所示，注意左侧横坐标第一项就是0100  
![image](http://m.qpic.cn/psc?/V51Uqo3Z3KmDDj0bhEZH0ySaLy25K537/ruAMsa53pVQWN7FLK88i5rx2t9cSeXQiYLuqJ05.4FSNLMnbEuWry.WaVUK8DLZK1Ex*4Q8psZMPKE3FXEd3kK9GM.4uvgaVsGsHP0v8onU!/b&bo=gALbAQAAAAABB3g!&rf=viewer_4)  
4. 横坐标0100纵坐标07改成02，横坐标0100纵坐标08改成03（就是我圈出来的位置修改的跟上图一样就行了）  
5. Crtl加w保存就行了  

  
最后记得用propertree去修改一下config，移除里面缓冲帧的“framebuffer-fbmem”，“framebuffer-stolenmem”，“framebuffer-unifiedmem”这三个条目。  

  
[本教程灵感来源@laozhiang](https://github.com/laozhiang)  
  


</details>   
  
<details>  
<summary>解决window与macos时间不同步/显示不正确</summary>  
  
  
  
在windows下面WIN+x 选择管理员模式进入CMD  
  
  执行以下命令：  
  
```bash
Reg add HKLM\SYSTEM\CurrentControlSet\Control\TimeZoneInformation /v RealTimeIsUniversal /t REG_DWORD /d 1
```  
</details>   

<details>  
<summary>关于如何在黑苹果下玩游戏（打破平台/硬件限制，黑苹果也能玩所有PC游戏）</summary>  
    
  
  
  
 ⚠️在注册的时候填写邀请码：DBZNT3EC  
！！可以白嫖3小时！！
  
       
      
我自己用的一个云电脑服务  
挺好用的能玩游戏（包括3A） 
也就是说在matebook13/14的黑苹果上也可以无硬件限制的玩任何游戏了  
直接4K全画质的开  
没啥延迟，就跟在本地玩一样  
我自己用的，推荐使用这个，这样在mac玩游戏也解决了  
  
⚠️在注册的时候填写邀请码：DBZNT3EC  
！！可以白嫖3小时！！
  
  
  
[点击进入它的官网](https://www.haixingcloud.com/#/Home)  
  


</details>   




## 如果想打赏小的，请选择一个你喜欢的方式打赏五块钱，谢谢！
  
  ⭐️打赏附言请留下自己的github的ID，用于公示感谢  
    
    
  
  
如果可用请在issues中提交你的机器信息（年份，cpu，matebook13还是14）  
用于构建更好的efi

## 感谢：

- @intel 感谢10年一管牙膏

- @apple 感谢创造出macos

- [@zxystd](https://github.com/OpenIntelWireless/itlwm) 感谢创造出wifi以及蓝牙的驱动

- [@MoZyo](https://github.com/MoZyo/RedmiBook-13-10th-Gen-Intel-Hackintosh) 教会了我很多东西

- [@Edoardo001](https://github.com/Edoardo001/Matebook-13-Hackintosh) 我做黑苹果的入门引路人 感谢他在matebook13的clover版efi上的杰出贡献
