### 版本22.02.25  
**重大更新**  
**1.全面切换到动态调频**  
**2.为原神、幻塔进行优化（需要Scene启用动态响应并后台保持Scene运行才能正常使用）**  
3.增加G90T支持，修复天玑720错误的频率选择  
***需要Scene启用动态响应并后台保持Scene运行才能正常使用本调度***  

### 版本22.02.13  
支持天玑810  
添加天玑9000的识别  
增加低温保护模式，在电池温度低于22度且切换配置为省电模式或者均衡模式时生效  
天玑1200系列待机省电优化  
  
### 版本22.02.09  
修复导致部分设备重启的问题

### 版本22.02.08 
**重大更新**  
适应增强模块解除温度墙，性能模式和极速模式互换    
天玑1200、1100均衡模式、省电模式恢复到原版7.25  

### 版本22.02.02
强制修改系统属性生效  
修改打包方式  
**等待天玑9000、天玑8000发布，非必要情况将减慢更新**  

### 版本22.01.31
修复不能启用超大核问题  
新年快乐

### 版本22.01.30
**重大更新**  
启用新的Magisk模块模板
Magisk限制版本为23.0及以上    
彻底分离增强模块，只保留取消官方锁帧等负优化的选项（在K40G MIUI和realme GT Neo官方系统测试正常）  
优化锁核策略，避免原版锁核导致MIUI13上应用不使用大核的问题（发现于K40G 22.1.19 com.android.settings)  
加强UI线程绑定  
为天玑1000+、天玑820的特殊机型增加特别配置，解决启用部分功能导致系统崩溃  
使用Magisk的Busybox，减少重复  
天玑1100/1200频率采用优化的Scene经典调度的频率表  
适配SoC为天玑1100且平台为MT6893或1+3+4调度的机型  
动态刷新率默认最高  
解除部分应用限频锁帧  
日志将记录加载调度时候的错误  
修复由于sh的原因导致的启动失败  
（上版本未提及）极速模式GPU频率优化  

### 版本22.01.28  
修复开机自动重启、自动进入fastboot的问题  
异步化修改，解决开机第一屏时间过长  
删除多余空格  
天玑1000、1100、1200、1000L均衡模式频率提高,省电模式频率降低  
直接使用Magisk的Busybox  

### 版本22.01.26  
**配置更新**  
添加天玑700、720  
天玑1200配置优化  
上一版本修改可选化（集中于“解除限制”这个修改内）  

### 版本22.01.25  
省电模式频率大幅降低  
内存加速加入锁频方法  
根据嘟嘟斯基的方法替换性能配置文件，解决游戏锁帧锁核问题  
启用PSI内存管理，优化后台（需要ZRAM或SWAP保持开启）  
回退部分没有影响的修改  
支持Magisk内更新模块（Magisk 23018版本开始）  

### 版本22.01.20  
将部分修改剥离为独立子模块，允许自由选择  
略微调低省电模式频率  

### 版本22.01.15  
**配置文件修改** 
分开K30U、MIUI、非MIUI设备  
取消过度严格的核心分配策略（系统分配的无法处理）  
针对MIUI13的优化扩展到所有SoC  
性能模式改为系统自动进行CPU降频，不在调度内降频  
**版本说明**  
MIUI：仓库版本迭代  
General：撤销针对MIUI设备的修改  
FixReboot：在General版本基础上撤销更多修改，缓解部分手机重启  

### 版本22.01.13
根据反馈的启动日志，尝试修复K30U重启问题  
调整GPU按需启动节点为通用节点  
调整省电模式设置，临时缓解MIUI桌面动画不识别为系统动画触发SsAnim而触发Touch的问题  
