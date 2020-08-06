# 项目介绍
车辆管理系统Demo，基于 Fabric v1.4.6 构建

## 前提
- 1.curl
- 2.docker >=1.19.*
- 3.docker-compose >=1.24.*
- 4.python
- 5.node >=8.* (or node 10.*)
- 6.npm (cnpm)
- 7.go >= 1.13.*

## 启动运行
在 ./webapp/ 目录下
在命令行中输入
```bash
cd webapp
./startFabric.sh
cnpm install
node enrollAdmin.js
node registerUser.js
node query.js

# 安装一个 express nodejs后端，如果不用，可以忽略此部分
npm install express --save  
# 对应的后端代码在 web.js 中
node web.js #启动
localhost:3000 #查看
```

## 停止
在 ./webapp/ 目录下
在命令行中输入
```bash
# 关闭网络
./stopFabric.sh

# 清理残留 docker volume，输入 y 确认清理 
docker volume prune
```
