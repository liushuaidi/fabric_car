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
npm install express --save  # 会安装一个 express node后端，如果不用，可以忽略这一句，对应的后端在 web.js 中，用 node web.js 启动，localhost:3000 查看
node enrollAdmin.js
node registerUser.js
node query.js
```

## 停止
在 ./webapp/ 目录下
在命令行中输入
```bash
./stopFabric.sh
# 清理残留 docker volume 
docker volume prune
# 输入 y 确认清理
```