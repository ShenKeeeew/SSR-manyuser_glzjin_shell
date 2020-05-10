# sspanel v3 glzjin 后端一键安装配置管理脚本

* 适用于glzjin面板ssr后端的一键安装脚本 实现输入配置信息、以及全自动安装，配置一键修改，一键启动暂停等功能 支持 modwebapi 及 glzjinmod（mysql connect）

# 安装方法 （ 2017/12/21 更新）
```
git clone https://github.com/Tiktoking/SSR-manyuser_glzjin_shell.git SSR

cd SSR
```
旧版本停止维护，目前不可用

新版本安装：
```
chmod +x shadowsocks_new.sh

./shadowsocks_new.sh install | tee ss.log

chmod +x /root/shadowsocks/*.sh
```
# 相关目录

后端默认安装目录：`/root/shadowsocks`

supervisor 默认配置目录 ：`/etc/supervisor/conf.d/shadowsocks.conf （Centos:/etc/supervisord.conf）`

# 启动方式（）

### 旧版本：

* 启动：`/root/shadowsocks/log.sh`
* 启动（日志模式）：`/root/shadowsocks/logrun.sh`
* 停止：`/root/shadowsocks/stop.sh`
* 日志：`/root/shadowsocks/tail.sh`

### 新版本：

* 启动  shadowsocks ：`./shadowsocks_new.sh start`
* 停止  shadowsocks ：`./shadowsocks_new.sh stop`
* 重启  shadowsocks ：`./shadowsocks_new.sh restart`
* 强制停止 shadowsocks ：`./shadowsocks_new.sh fstop`
* 配置信息变更：`./shadowsocks_new.sh modify`
* 添加 supervisor 开机启动： `systemctl enable supervisor (centos6:chkconfig --add supervisord)`
* 日志 ：`tail -f /var/log/sslog.txt`




