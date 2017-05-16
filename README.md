# Zeng-Swoole-Framework
An php mvc framewrok base Swoole
# 安装
基于linux环境，运行需要先安装swoole 2.0扩展
支持PHP7 

#运行

cd frame/shell
//启动http服务
php server.php testHttpServ start 

# http测试站点配置
[server]
;添加所有配置


//所有的server信息
;服务类型
type = http
; 监听端口

listen[] = 10001
; 入口文件

root = '/data/git/Zeng-Swoole-Framework/example/httpsrc/index.php'
;init = ''
;用来支持多php版本

php = '/usr/bin/php'
;server_name='testserver'


[setting]
; worker进程数
worker_num = 24
; task进程数
task_worker_num = 0
; 转发模式
dispatch_mode = 2
; 守护进程
daemonize = 1

;post数据最大
package_max_length = 12582912
buffer_output_size = 12582912
; 系统日志
log_file = '/data/log/server/newapi/BusinessServ.log'

; 心跳  遍历所有连接 interval 内没有发送数据 强制关闭
heartbeat_check_interval = 60
heartbeat_idle_time = 600

;关闭Nagle合并算法，立即发送数据到客户端，提升http服务响应数据
open_tcp_nodelay = true

;关闭eof检测
open_eof_check = false
open_eof_split = false



