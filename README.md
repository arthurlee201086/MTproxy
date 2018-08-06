# MTproxy
telegram专用Mt代理一键部署脚本(逗比根据地出品)
原博客地址：https://doub.io/shell-jc7/
# 最关键一步骤提醒：要你输入IP时，如果你是阿里云腾讯云谷歌云等大厂的，只要是NAT主机模式（ifconfig确定下你的公网IP，不是你一个在用这个IP的话），请输入ifconfig看到的你的主机内网地址。如果这都不懂，那呵呵呵。
系统要求
CentOS 7 / Debian 7+ / Ubuntu 14.04 +

推荐 Debian 7/8 x64，这个是我一直使用的系统，我的脚本在这个系统上面出错率最低。

注意：因为 CentOS 6 系统的 GCC 版本过低，会导致编译失败，请使用更高版本的系统！

脚本版本
Ver: 1.0.4

安装步骤
执行下面的代码下载并运行脚本。

wget -N --no-check-certificate https://softs.loan/Bash/mtproxy.sh && chmod +x mtproxy.sh && bash mtproxy.sh
 
# 如果上面这个脚本无法下载，尝试使用备用下载：
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/mtproxy.sh && chmod +x mtproxy.sh && bash mtproxy.sh
运行脚本后会出现脚本操作菜单，选择并输入 1 就会开始安装。

点击展开 查看更多

使用说明
进入下载脚本的目录并运行脚本：

./mtproxy.sh
然后选择你要执行的选项即可。

  MTProxy 一键管理脚本 [v1.0.0]
  ---- Toyo | doub.io/shell-jc7 ----
  
  0. 升级脚本
————————————
  1. 安装 MTProxy
  2. 更新 MTProxy
  3. 卸载 MTProxy
————————————
  4. 启动 MTProxy
  5. 停止 MTProxy
  6. 重启 MTProxy
————————————
  7. 设置 账号配置
  8. 查看 账号信息
  9. 查看 日志信息
 10. 查看 链接信息
————————————
 
 当前状态: 已安装 并 已启动
 
 请输入数字 [0-10]:
其他操作
启动：/etc/init.d/mtproxy start

停止：/etc/init.d/mtproxy stop

重启：/etc/init.d/mtproxy restart

查看状态：/etc/init.d/mtproxy status

安装目录：/usr/local/mtproxy

配置文件：/usr/local/mtproxy/mtproxy.conf

日志文件：/usr/local/mtproxy/mtproxy.log

Telegram 使用方法说明：
如果你的 TG 客户端没有 Mtproto 代理选项，那么请更新到最新版本！

Telegram 内置了 Mtproto 代理选项，所以TG客户端内点击 tg://proxy?xxxx... 链接就会自动配置代理，非常方便。

PC 使用步骤如下：
点击展开 查看更多

其他说明
注意：MTProxy 仅支持 Telegram 客户端使用，无法用于其他软件！

启动失败，日志提示 'S' option requires exactly 32 hex digits 错误
该问题只出现于自定义密码时，因为 MTProxy 为了安全性而要求密码必须是 32位（多了少了都不行），如果数量不对就会提示这个，建议用脚本随机生成！

提示wget: unknown host “softs.loan” 之类的错误
点击展开 查看更多

提示 wget: command not found 的错误
点击展开 查看更多

升级脚本
升级脚本只需要重新下载脚本文件就可以了，会自动覆盖原文件。
