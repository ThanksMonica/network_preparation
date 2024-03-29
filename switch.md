# 交换机
允许多端口通道同时工作，可以将网络系统划分为多个物理网段，具有**存储转发**和**直接转发**两种帧转发方式，等待时间短（无需接受完整数据帧和经过32bitCRC计算校验时间）。

> - **二层交换机：** 工作在数据链路层，支持物理层与数据链路层协议，根据 **MAC地址** 过滤及转发数据帧，防止形成环路；
> - **三层交换机：** 二层交换+三层转发



| 工作位置   |   作用 |       功能特性       |  要求    |
| :-------- | :--------:| :--: |:--: |
| 核心层    |联通网络、保证高校传输| 可靠性、高效性、冗余性、容错性、可管理性、适应性、低延时性   | 采用高带宽千兆以上交换机|
| 汇聚层     | 减轻核心层负担 |     实施策略、安全、工作组接入、链路流量聚合、VLAN间路由、广播域定义|采用支持三层交换技术和VLAN的交换机
| 接入层      | 将工作站接入本地网段 | 减少同一网段工作站数量、向工作组提供高速带宽  | 交换机无特殊要求|
