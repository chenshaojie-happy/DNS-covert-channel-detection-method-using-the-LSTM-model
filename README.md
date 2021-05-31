# DNS-covert-channel-detection-method-using-the-LSTM-model

##1. 整体介绍(Overview)

&ensp;&ensp;&ensp;&ensp;这是文章《DNS covert channel detection method using the LSTM model》 (DOI: https://doi.org/10.1016/j.cose.2020.102095) 用到的数据集，本数据集由北京航空航天大学软件开发环境国家重点实验室海量信息处理与信息安全课题组构建。  
&ensp;&ensp;&ensp;&ensp;This is the dataset that the paper "DNS covert channel detection method using the LSTM model" (DOI: https://doi.org/10.1016/j.cose.2020.102095) used, which was collected by Massive Data Processing and Information Security Group of State Key Laboratory of Software Development Environment, Beihang University.

##2. 数据集说明(Dataset description)
&ensp;&ensp;&ensp;&ensp;由于白样本涉及到真实用户的行为，不合适公开，这里仅公开我们在独立组网的环境中运行DNS隐蔽信道工具生成流量的pcap文件。   
&ensp;&ensp;&ensp;&ensp;Since the benign samples involve the hehaviors of real users and is not suitable for disclosure, here we only disclose the pcap files of the traffic generated by running the DNS covert channel tools in an independent network. 


&ensp;&ensp;&ensp;&ensp;这些pcap文件中的IP仅为独立组网环境中的IP，与现实网络中的IP无关。  
&ensp;&ensp;&ensp;&ensp;The IPs in these pcap files is only the IPs in the independent network, and are not releated to the IPs in the actual network.

&ensp;&ensp;&ensp;&ensp;我们总共运行了iodine, dnscat2, dns2tcp, ozymandns, dnshell v1.7, cobaltstrike, det, dnsexfiltrator这8中工具，在独立环境中模拟文件传输。文件传输的方向分为上行(client -> server)和下行(server -> client)，两个方向样本独立采集。   
&ensp;&ensp;&ensp;&ensp;We have run 8 tools to simulate file transfer in an independent environment, including iodine, dnscat2, dns2tcp, ozymandns, dnshell v1.7, cobaltstrike, det, dnsexfiltrator. The direction of file transfer is divided into upstream (client -> server) and downstream (server -> client), and samples in the two directions are collected separately.

##3. 引用(Reference)
&ensp;&ensp;&ensp;&ensp;如使用该数据集，请添加对我们文章的引用。  
&ensp;&ensp;&ensp;&ensp;If used this dataset, please cite our paper.  
```
Chen, S., Lang, B., Liu, H., Li, D., & Gao, C. (2021). DNS covert channel detection method using the LSTM model. Computers & Security, 104, 102095.
```

##4. 其他说明(Other instructions)
&ensp;&ensp;&ensp;&ensp;这些pcap文件中可能包含少量非DNS协议的packets，在解析的时候需注意过滤。  
&ensp;&ensp;&ensp;&ensp;These pcap files may contain a small number of packets of non-DNS protocols, so please filter them when parsing. 