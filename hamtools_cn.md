---
layout: page
title: HAM 常用工具
---
## 网站
- 通联前
  - [Windy](https://www.windy.com/)：天气预报与气象云图。打雷时别操作，大风大雨时别野架。
  - [HF Propagation and Solar-Terrestrial Data](https://www.hamqsl.com/solar.html)：太阳活动与短波、VHF传播信息。其实很多时间短波通不到人不是因为传播不好，而是因为天线设备太菜了。
- 通联中
  - [PSK Reporter](https://www.pskreporter.info/)：数字模式监测站报告，可以用来查看都有哪些台站收到了你的数字信号，适用CW、FT8等模式。这个网站因为使用了Google的相关服务，以及一个被墙的前端库，所以国内网上不去。具体解决办法可以参考[本站的 PSK Reporter 国内换源教程](https://yurihou.github.io/2024/05/08/PSK-Reporter-%E5%9B%BD%E5%86%85%E6%8D%A2%E6%BA%90%E6%95%99%E7%A8%8B.html)。
  - [Reverse Beacon Network](https://www.reversebeacon.net/)：简称RBN，CW信号监测台。
  - [Contest Calendar](https://www.contestcalendar.com/)：竞赛日历，收集了一些竞赛信息。
  - [DX Summit](http://www.dxsummit.fi/)：远征台信息报告，可以上传自己收到的稀有台（其实不稀有也能传）报告，并查看别的台上传的报告。
  - [QRZ.com](https://www.qrz.com/)：在线HAM数据库，给数据库内的HAM提供一个免费的网页供编辑，可以些一些个人的信息，比如邮寄地址、天馈设备之类的信息上去。也可以查找别人的相关信息，当然前提是对方也上传了。有个 [国区特供 QRZ.cn](http://www.qrz.cn/) ，似乎维护一般，反正我是不想用它。
- 通联后
  - [Logbook of the World](https://lotw.arrl.org/)：简称LoTW，美国无线电传播协会的官方日志系统。[LoTW申请流程](https://www.bilibili.com/read/cv21069343/)
  - [QRZ.com](https://www.qrz.com/)：QRZ.com 还有一套日志系统挺好用的。QRZ.com 注册账号不难，但是后面还需要有人把呼号添加进数据库才能正常使用功能。详见 [QRZ.com注册教程](https://yurihou.github.io/2023/12/18/QRZ.com-%E7%BD%91%E7%AB%99%E6%B3%A8%E5%86%8C%E6%8C%87%E5%8D%97.html)
  - [eQSL.cc](https://www.eqsl.cc/)：一款在线日志系统，日志本身挺好用，就是GUI有点难看。
- HAM 使用的各种地图
  - [Maidenhead Grid Locator](https://www.f5len.org/tools/locator/)梅登黑德网格地图。因为使用了[OpenStreetMap](https://www.openstreetmap.org/) ，网站原版国内不太好用。这里有个国内特供版 [梅登黑德网格定位系统](http://sjzham.cn/grid/) 挺好用的。
  - [Great Circle Mapper](https://ns6t.net/azimuth/azimuth.html)：大圆地图，确定定向天线的指向比较好用。冷知识，北京打美国，天线应当指向正北而不是正东。
  - [GridTraker](https://gridtracker.org/)：可以配合[WSJT-X](https://wsjt.sourceforge.io/wsjtx.html), [JTDX](https://sourceforge.net/projects/jtdx/), [JTDX 国区特供版](https://forum.hamcq.cn/d/318) 等软件，显示正在呼叫的，或者以前通联过的FT8台的台站位置。
- HAM DIY
  - [LC Filter Design Tool](https://markimicrowave.com/technical-resources/tools/lc-filter-design-tool/)：LC滤波器计算器。因为使用了一些Google的东西，需要科学上网才能使用。
  - [DK7ZB Antennas](https://www.qsl.net/dk7zb/start1.htm)：有很多天线图纸，我自己手搓的很多天线的图纸就是这里来的，亲测好用。
  - [YO3DAC Homebrew RF Circuit Design Ideas](https://www.qsl.net/va3iul/Homebrew_RF_Circuit_Design_Ideas/Homebrew_RF_Circuit_Design_Ideas.htm)：收集了一些业余无线电设备的电路图。

## Android APP
绝大多数Android业余无线电APP都是老外写的，他们一般会把APP放在Google Play或者F-Droid里，这两个网站都需要一些特殊手段进行访问。好在大多数业余无线电APP也都是开源的，Github上面一般也都有Release版的。如果您连Github都没办法访问，那……就考虑微信联系本站作者吧，主页有邮箱。
- 业余卫星通联
  - Look4Sat：个人认为的卫星追踪软件的扛把子。可以使用手机的陀螺仪和罗盘进行卫星追踪，可以使用在线或者离线TLE源，在线默认的TLE源卫星很全。甚至还可以通过蓝牙向天线旋转器发送角度信息。需要注意的是，利用手机追踪卫星时要防止铁磁材料（比如一些手台）靠近手机，否则手机的卫星指向会漂移。[Look4Sat Github](https://github.com/rt-bishop/Look4Sat)，[F-Droid](https://f-droid.org/packages/com.rtbishop.look4sat/)，[Google Play](https://play.google.com/store/apps/details?id=com.rtbishop.look4sat)
  - Heavens Above：另一款卫星追踪软件。TLE库不能更改，卫星不是很全，不过有ISS基本就够用了。Heavens Above还有一个特点就是默认有星图，还可以显示部分卫星的可见性（部分卫星，如ISS、CSS等，在天气晴朗的清晨或傍晚等时间可以反射太阳光，肉眼可见）。[Heavens Above 官网](https://www.heavens-above.com/)，[Google Play](https://play.google.com/store/apps/details?id=com.heavens_above.viewer)
- SSTV
  - SSTV Encoder 2：SSTV编码器。[SSTV Encoder 2 Github](https://github.com/olgamiller/SSTVEncoder2?tab=readme-ov-file#sstv-encoder-2)，[F-Droid](https://f-droid.org/packages/om.sstvencoder/)，[Google Play](https://play.google.com/store/apps/details?id=om.sstvencoder)
  - Robot 36：SSTV解码器。虽然支持自动判断SSTV模式，但有时候判断不准，而且似乎校正时钟偏差也有点不太行。感觉收SSTV正经方法还是手机录音再送给电脑端的[MMSSTV](https://hamsoft.ca/pages/mmsstv.php)之类的软件。[Robot 36 Github](https://github.com/xdsopl/robot36/tree/android)，[F-droid](https://f-droid.org/packages/xdsopl.robot36)，[Google Play](https://play.google.com/store/apps/details?id=xdsopl.robot36)
- CW & 摩尔斯电码
  - 若干摩尔斯电码练习器，不过感觉摩尔斯电码还是iOS那边的Morse-It更好用一些。
  - Morse Expert：CW译码器。支持自动检测CW音频频率，效果挺不错，满足基本需求。[Morse Expert 官网](https://ve3nea.github.io/MorseExpert/)，[Google Play](https://play.google.com/store/apps/details?id=com.ve3nea.morse_expert&pcampaignid=pcampaignidMKT-Other-global-all-co-prtnr-py-PartBadge-Mar2515-1)
- APRSdroid APRS模式几乎唯一指定的Android程序。[APRSdroid 官网（官网服务器即可下载APK）](https://aprsdroid.org/)，[Github](https://github.com/ge0rg/aprsdroid/wiki)，[Google Play](https://play.google.com/store/apps/details?id=org.aprsdroid.app)
- FT8CN：FT8 Android程序。声称可以通过OTG、蓝牙、Wi-Fi等方式连接支持的电台进行控制，但我连我个人的X6100反正不太成功。感觉甚至空气耦合更好用一些。[FT8CN Github](https://github.com/N0BOY/FT8CN)，[Gitee](https://gitee.com/bg7yoz/ft8cn)
- 短波传播监测：软件就叫这个名字，我也忘了从哪里下载的了。其内容感觉是爬[HF Propagation and Solar-Terrestrial Data](https://www.hamqsl.com/solar.html)网站的数据然后翻译一下得到，可以作为传播好坏的参考。感觉甚至是一个套壳的小程序。很多业余无线电小程序里面就有这个功能，可以从其他小程序里面查看。

## 微信小程序
- 业余无线电工具集：BDKZS写的，内容很全，有HAM考试题库、中继信息，以及一些其他的小功能，几乎是国内业余无线电必备。
- HAM模拟考试：有国内ABC证的题库，甚至还有美国FCC的TGA证的题库，可以考前刷题用。
- 云端卫星：业余卫星小程序，可在线查看卫星信息、TLE信息，有卫星过境时间总结，还有罗盘，尤其方便iOS用户（目前主流的iOS卫星追踪APP似乎都没有罗盘功能）。
