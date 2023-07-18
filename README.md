# esp8266_smartcard

Use esp8266's GPIO to simulate a smart card,
while running an oscam client,
connecting to the cccam server via esp8266's wifi.

So as to achieve the set-top box DVB CW sharing.

使用 esp8266 来模拟智能卡，把 esp8266 接到标准的机顶盒读卡器上，从而实现 cccam 共享。
要用到四根数据线连接读卡器和 esp8266 的 gpio 端口。
分别是 vcc、gnd、5、2。
gpio 2 为 io，连接到到读卡器 io
gpio 5 为 rst，连接到到读卡器 rst。

在某些情况下，需要在 esp8266 的 io 和 rst 到读卡器间，要串联一个 470 欧的电阻。

本项目用 arduino 打开编译，需要安装 esp8266 支持库和 ESPAsyncTCP 库。
目前支持了永新同方卡的模拟。长时间观看会出现不稳定现象，原因未知。
想折腾的可以添加其它卡支持。

Use o GPIO do esp8266 para simular um cartao enquandto executa um oscam
