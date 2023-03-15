# SimplifyLiveroomTemp

由于哔哩哔哩改版，导致直播间的礼物屏蔽有点问题。如下图所示。 
![problem.png](img%2Fproblem.png)

为了解决这个问题，通过对原版组件"简化直播间"进行了极为粗糙的修改，发现可行。

## 粗糙的办法
1. 卸载原版的"简化直播间"插件；
2. 在添加组件的界面上，填入我魔改的临时的live.js文件，如下图所示：
live.js地址：https://raw.githubusercontent.com/fortandh/SimplifyLiveroomTemp/main/live.js
![steps.png](img%2Fsteps.png)
3. 然后按照原来的方式，屏蔽"付费礼物"就可以了。

## 原因分析
改版后，添加了三个内容：
* .gift-section.recharge-ent: 电池充值
* .gift-control-panel .section: 魔法奇遇
* #gift-control-vm: 整个礼物栏，如果display不为none的话，会出现一片黑色区域
![reason.png](img%2Freason.png)

## Q&A
问：为啥不另外起个名字，比如"简化直播间（临时版）"？  
答：因为，尝试改过里面的name和displayName，但是，改了名字后，脚本不生效了……

问：为啥不按照官方的教程，自己编译一个改名字的，然后分享呢？  
答：编译过，发现没有生效……我对TS和JS不太熟悉，因此后面准备抽时间看看。

问：既然做的这么烂，你怎么好意思分享呢？  
答：分享是我的意愿，怎么看是你的意愿。