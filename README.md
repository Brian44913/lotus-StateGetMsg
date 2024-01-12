# lotus-StateGetMsg

* 实现了类似`lotus-shed msg 消息CID`的api请求
* 仅上传了需要修改的文件，方便自行合并
* 基于 v1.25.2 
* [代码修改查看 · Brian44913/lotus-StateGetMsg](https://github.com/Brian44913/lotus-StateGetMsg/commit/d846fb216b7067ffd3189cfb7283fec04e577104)


#### 一键合并代码
```
cd lotus && \
wget  https://raw.githubusercontent.com/Brian44913/lotus-StateGetMsg/main/update-StateGetMsg.patch && \
patch -p1 < update-StateGetMsg.patch
```


#### api 请求方法
```
curl -X POST  -H "Content-Type: application/json"  \
--data '{"jsonrpc":"2.0","method":"Filecoin.StateGetMsg","params":[{"/": "bafy2bzaced4bmzg6igjnfpcyn2mtl7dlawmaal6yjxi72mz3upyua6ucy36a6"}],"id":3}'  \
'http://127.0.0.1:1234/rpc/v0' | jq
```