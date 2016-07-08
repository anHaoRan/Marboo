# forever

> 以前使用nohup node app &的形式启动后台运行，但是总是不自动结束，退出就停止服务了

```shell
npm i -g forever # 安装
forever start app.js # 启动 
forever stop app.js # 关闭
forever list # 输出forever启动的所有服务
forever stop 1 # 停止指定服务
forever start -c "npm run build" ./project-name # 启动npm run 模式的服务
```