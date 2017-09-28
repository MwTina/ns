# Ex1 基于VirtualBox的网络攻防基础环境搭建 # 
----------
## 完成度 ##
### 已完成： ###
攻击者主机无法直接访问靶机  
网关可以直接访问攻击者主机和靶机  
靶机的所有对外上下行流量必须经过网关  
所有节点制作成基础镜像（多重加载的虚拟硬盘）
### 未完成： ###
所有节点均可以访问互联网    
靶机可以直接访问攻击者主机

----------
## 网络配置 ##
## 攻击机 ###
![](file:///C:/Users/Surface/Pictures/Screenshots/攻击机/set.PNG)
## 网关 ###
![](file:///C:/Users/Surface/Pictures/Screenshots/网关/eth0.PNG)
![](file:///C:/Users/Surface/Pictures/Screenshots/网关/eth1.PNG)
## 靶机 ###
![](file:///C:/Users/Surface/Pictures/Screenshots/靶机/set.PNG)


----------
## 证明截图 ##
### 攻击者主机无法直接访问靶机 
![](file:///C:/Users/Surface/Pictures/Screenshots/攻击机/捕获.PNG)  
### 网关可以直接访问攻击者主机和靶机 
![](file:///C:/Users/Surface/Pictures/Screenshots/网关/捕获.PNG)  
### 靶机的所有对外上下行流量必须经过网关
![](file:///C:/Users/Surface/Pictures/Screenshots/靶机/捕获.PNG) 
### 所有节点制作成基础镜像（多重加载的虚拟硬盘） 
![](file:///C:/Users/Surface/Pictures/Screenshots/网关/多重加载.PNG)  


----------
## 思考&&问题 ##
1. 网关和攻击机都是桥接模式本应可以上网，网上资料说桥接模式想上网需要支持混杂模式的网卡，一般无线网卡都不支持混杂模式。不知道是不是这个原因？  
2. 本来考虑过host-only模式，但是打开virtual box host-only网卡的网络共享之后，宿主机也没办法上网了。
3. 靶机通过NatNetwork与网关相连，攻击机对于靶机来说是外网，本应可以ping通。