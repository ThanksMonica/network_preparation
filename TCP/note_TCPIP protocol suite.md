  # 《TCP/IP协议族》读书笔记
  @(网络的本质与作用)[分层|以太网vsTCP/IP网络|分组转发|通信->地址]
  @[以太网交换机|一卡通专网网络拓扑]
  

## OSI模型

<table width=500px><tr><td bgcolor=#81C0C0>
  7. 应  用  层：允许访问网络资源</td></tr></table>
<table width=500px><tr><td bgcolor=#81C0C0>
  6.  表 示 层：数据的转换、加密、压缩</td></tr></table>
<table width=500px><tr><td bgcolor=#81C0C0>
  5. 会 话 层：建立、管理、终止会话</td></tr></table>
<table width=500px><tr><td bgcolor=#5CADAD>
  4. 运 输 层：提供可靠的进程-进程交付&差错恢复</td></tr></table>
<table width=500px><tr><td bgcolor=#4F9D9D>
  3. 网 络 层：从源到终点传送分组，提供网络互连</td></tr></table>
<table width=500px><tr><td bgcolor=#3D7878>
   2. 数据链路层：将比特组织成帧结构，提供逐跳交付</td></tr></table>
<table width=500px><tr><td bgcolor=#336666>
  1. 物 理 层：经过媒体传送比特，提供机械和电气的规约</td></tr></table>


* :heart: 层与层之间通信->接口
- :heart:数据->封装


st=>start: Start
e=>end
op=>operation: My Operation
cond=>condition: Yes or No?

st->op->cond
cond(yes)->e
cond(no)->op


### 1\.物理层(physical layer)
>- 定义传输媒体间的接口特性与传输媒体类型
>- 定义比特编码
>- 定义传输速率
>- 比特同步
>- 线路配置
>- 物理拓扑
>- 传输方式（全双工、半双工）

:peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach:


### 2\.数据链路层(data link layer)
>- 组帧：将从网络层接收到的比特流划分为数据单元（帧）
>- **物理编址：** 
  ```mermaid
    graph LR;
      发送帧-->本网;
      本网-->加首部;
      加首部-->接收方\发送方地址;
      发送帧-->外网;
      外网-->加首部;
      加首部-->下一网络的连接设备地址;
  ```
>- 流量控制：预防接收方（接受速率<发送方产生速率）过负荷
>- 差错控制：
  ```mermaid
  graph LR;
  发送帧-->帧丢失
  发送帧-->帧错误
  帧丢失-->加尾部;
  帧错误-->加尾部
  加尾部-->差错控制;
  ```
>- 接入控制：多个设备接入链路时，决定哪一设备对链路的控制权

:peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach::peach:

### 3\.网络层(network layer)
### 4\.运输层
### 5\.会话层
### 6\.表示层
### 7\.应用层
