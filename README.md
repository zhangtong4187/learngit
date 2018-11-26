照着这个视频 https://youtu.be/gImm4CfAnRs 部署镜像

环境变量： CONFIG_JSON（配置）、

用notepad++将上述变量中 \r\n 替换为\n，变成一行，导入容器。

客户端： android Actinium、windows v2ray 可用同一个服务端。

youtube频道：https://www.youtube.com/channel/UClceV39J1Z_9D4_mHkBZrMg


下拉第一个里填写CONFIG_JSON
第二个里复制下面的代码，注意uuid要填写。这个很重要，后面还要用到。UUID生成网址：https://www.uuidgenerator.net/

{
  "log": {
    "loglevel": "warning"
  },
  "inbound": {
    "protocol": "vmess",
    "port": 8080,
    "settings": {
      "clients": [
        {
          "id": "uuid换成你自己的",
          "alterId": 64,
          "security": "aes-128-cfb"
        }
      ]
    },
    "streamSettings": {
      "network": "ws"
    }
  },
  "inboundDetour": [],
  "outbound": {
    "protocol": "freedom",
   "settings": {}
  }
}
