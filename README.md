基于原作者修改，删除依赖安装的脚本。自用
# Tailscale on OpenWRT :smiley: [![Page Views Count]()](`uname -m` 出来的结果 ***可能*** 不是脚本中预设的内容，)

> 注：clash for windows/clash verge的TUN模式与DockerDesktop、Tailscale不兼容, 解决办法: 暂时关闭TUN, 登录/使用完毕后再打开.
>  [原理](https://chengyunzhe.notion.site/chengyunzhe/clash-for-windows-docker-tailscale-fccff782bd2c482cb9b7d3dd08c58b18)
------------

## 0x00 安装
全新安装
```
wget -O- https://ghproxy.cc/https://raw.githubusercontent.com/waltermanpro/tailscale-openwrt/chinese_mainland/install.sh | sh
```



------------

## 0x01 卸载
- ***请注意不要在ssh连接期间卸载，因为ssh连接将丢失！使用风险自负。***

```
wget -O- https://ghproxy.cc/https://raw.githubusercontent.com/waltermanpro/tailscale-openwrt/chinese_mainland/uninstall.sh | sh
```
------------
## 0x02 升级
- 升级tailscale
- ***每次启动openwrt时tailscale_downloader都会通过网络下载最新版本的TailScale的可执行文件。***
```shell
reboot
```

- 保留配置升级
- ***如果下载器脚本(tailscale_downloader)存在版本更新(更新代理地址等), 运行以下命令更新最新下载器脚本***:
```
rm -rf /tmp/tailscale* && wget -O- https://ghproxy.cc/https://raw.githubusercontent.com/waltermanpro/tailscale-openwrt/chinese_mainland/install.sh | sh && reboot
```
------------

#### 如果好用，麻烦动动小手点个Star，谢谢啦！
## 如果有新版本可用, 但是还没到actions运行时间, 你可以手动点击start触发actions运行, 更新最新版本.
------------
### 特别感谢:
[adyanth [openwrt-tailscale-enabler]](https://github.com/adyanth/openwrt-tailscale-enabler) 

[adyanth [CH3NGYZ/tailscale-openwrt]](https://github.com/CH3NGYZ/tailscale-openwrt) 
