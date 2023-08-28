# Blockchain Systems in Embedded Internet of Things: Systematic Literature Review, Challenges Analysis, and Future Direction Suggestions

>  This article discusses blockchain technology and embedded devices in distant areas where IoT devices may encounter 
> network shortages and possible cyber threats. This study aims to examine existing research while also 
> outlining prospective areas for future work to use blockchains in smart settings. Finally, the efficiency 
> of the blockchain is evaluated through performance parameters, such as latency, throughput, storage, 
> and bandwidth. The obtained results showed that blockchain technology provides security and 
> privacy for the IoT.

该文章讨论如下几点：

- 检验已有的有关嵌入式区块链的研究
- 预测嵌入式区块链的未来发展方向
- 从延迟、吞吐量、存储（耗费）和带宽的角度评估区块链的效率

## 1. 引言

> In the IoT context, privacy, permission, information storage, access control, and system configuration present the most security problems.

嵌入式领域面临如下问题：

- 隐私保护
- 权限管理
- 信息存储
- 准入管理
- 系统配置

由于嵌入式设备算力有限，其使用的安全措施（例如基础的非对称加密）不足以应对潜在的威胁，无法满足数据安全的五项原则：availability, integrity, authentication, confidentiality, nonrepudiation。

区块链拥有的几个特性之一（scalability, decentralization, and trustworthiness）对此给出了一个较为可行的解决方案。但其局限性为：

- 延迟
- 并发
- 防护

## 2. 研究设计、方法论及数据收集

作者使用关键词在三个文献库中搜索，以解答如下问题：

- RQ1: How does the development of the IoT affect the publication trend in the blockchain system? This statistical inquiry focuses on published articles that address IoT security, trust, and blockchain, employing datasets or benchmarks, and evaluating the case studies. 物联网行业的发展是如何影响区块链系统的？
- RQ2: What role do trust and security play in the IoT’s expanding use of blockchain technology? The inquiry aims to assess IoT security and trust metrics over time in published research and emphasize the importance of blockchain accuracy in IoT. 在物联网广泛应用区块链技术的大背景下，信任和安全可以为它带来什么？
- RQ3: Which blockchain system flaws and solutions were found for potential IoT developments in the future? This inquiry looks at IoT suggestion weaknesses and appropriately identifies methods to boost security and trustworthiness. 区块链系统的物联网发展的未来有何潜在危险？
- RQ4: What are the key research drivers behind securing the IoT using a blockchain system? To learn more about blockchain solutions for the IoT environment and how successful they are in terms of security. 用区块链提升物联网安全性的关键研究驱动力为何？
- RQ5: What are the current blockchain-based solutions to security issues in the IoT environment? Recognize, evaluate, and categorize blockchain-based IoT security techniques.当下物联网采用的区块链解决方案使用何种安全措施？

经过对搜索数据进行分析，作者得出结论：对于物联网和区块链的研究于近几年方才出现，在呈现逐年增长的趋势下，2021年出现了一次大爆发。最终，作者将物联网上区块链平台的推荐架构（“Proposed Architectures for the IoT on the Blockchain Platform”）作为其研究领域，并将搜索到的资料规整总结为了四个派别：

### 2.1 双区块链架构

该派别认为，物联网平台必须解决如下三个问题：入侵检测、连接安全和信息压缩存储。双区块链架构为这三个问题提出一个解决方案。它是一个基于云雾通信网络构造的私有区块链（云，指利用互联网上的远程服务器来存储、管理和处理数据，而不是使用本地服务器或个人电脑；雾，指利用互联网边缘的设备来执行大量的计算、存储和通信，而不是将所有数据上传到云端）。双区块链架构由如下组件构成：

- 雾层级：信誉值区块链，存储各个物联网设备的信誉信息
- 云层级：信息区块链，存储物联网上真正的数据

文中提及了一些例子，以下是一部分：

| 提出人    | 特点                                                         |
| --------- | ------------------------------------------------------------ |
| Li Hao    | 用双层区块链分离了抵押/注册和控制操作。                      |
| Aldriwish | 使用椭圆曲线密码学，提升了通信交易的安全性；使用压缩感知技术（compressed sensing technique）提升了数据压缩的效率。 |
| Ren, Wan  | 使用分布式文件系统存储数据，并以类似Oracle数据库的方法提取这些数据。 |

> 抵押/注册是指用户在区块链上注册自己的身份和资源，并将一定数量的通证作为抵押物锁定在智能合约中，以保证自己的诚信和可信度；控制操作是指用户在区块链上控制自己的身份和资源的访问权限，以保证自己的安全和隐私。用户可以通过发送数字签名来验证自己的身份和授权他人访问自己的资源，也可以随时撤销或修改授权策略。

这些例子聚焦于准入控制、通信安全等痛点，设计了诸如双层区块链、椭圆曲线、分布式存储等方法，缓解了通信延迟，提升了响应速度。

### 2.2 基于软件定义网络（Software Defined Networks）的架构

>  Software Defined Network是一种软件定义网络的技术，它可以通过软件来控制网络中的设备，如交换机、路由器、防火墙等，而不需要对每个设备进行单独的配置和管理。其核心思想是将网络的控制层和数据层分离，即将负责网络的转发和处理的数据层设备与负责网络的逻辑和策略的控制层设备分开，通过一个统一的接口进行通信和协调。这种架构的优势在于：可以实现网络的灵活配置和管理，根据不同的应用需求和业务场景，动态地调整网络的拓扑、流量、安全等参数，提高网络的性能和效率。

该学派认为，基础设施应当在满足高安全性和高保密性的前提下，尽量保持可持续发展、高适应性的特点，以满足应用多样性及其较高的更新迭代速度。为此，人们提出了多种设计范式，其中一种叫做软件定义网络，另一种就是区块链。

文中例子专注于安全和隐私保护的方面，结合SDN和区块链技术，达成了提升吞吐量，高效识别攻击流量，减少延迟和丢包的成果。

### 2.3 边缘计算/雾计算

为支持不同延迟要求、不同计算密度的物联网应用，人们将目光投向了云雾计算的结合。

例如，Cho, Wu提出了一种充电式无线传感器网络方案，以提升该网络的生存周期。他们利用雾计算，将计算压力分摊到多个传感器上，从而改善了在单个传感器电池容量有限的前提下传感器的电池续航问题。

其他例子也已雾计算为契机，做到了诸如提升能源利用效率，降低延迟等效果。

### 2.4 轻量级架构

对于像智慧城市这样的应用场景，区块链需要能做到快速建立共识，并妥善处理巨量交易。因此，轻量级的区块链架构逐渐引起了人们的注意。

Seok, Park提出了一种可以根据交易量动态调节哈希函数的区块链。他们选择了三种轻量级的哈希算法，在满足足够安全且空间占用和计算负担足够小的前提下，分别面向需要更优的实现空间、能源消耗和吞吐量的应用场景。模拟显示，该算法可以将区块链系统的延时降低到1s以下。

> 实现空间是指算法在硬件上的占用情况，包括逻辑资源、存储资源和时钟资源等。 实现空间越小，说明算法越节省硬件资源，越适合在有限资源的设备上运行。

## 3. 结果分析

分析以上文献之后，作者总结了区块链技术面临的难题和可能的机遇。

### 3.1 区块链与人工智能结合，保障物联网大数据分析安全

机器学习中有一个名为联邦学习（Federated Learning）的概念，允许在保障隐私的前提下进行分布式的模型训练。利用这种学习方式，可以保证供给AI学习的数据的准确性。

### 3.2 物联网区块链的规模化问题

现有的很多区块链网络在节点数目很多时表现不尽如人意。若无法解决该问题，则中心化的解决方案可能会占据上风。这是区块链在物联网领域急需解决的重大问题之一。

### 3.3 区块链保障软件定义物联网安全

边缘计算在降低延迟的同时也带来了设计和维护方面的新难题。使用软件定义网络的方法解决该难题，又可能引入安全方面的隐患。可使用区块链环缓解安全方面的问题。

### 3.4 可信的智能合约物联网区块链

将智能合约应用在区块链上，可以让数据的加密和存储过程全部自动化。这种方法兼顾了区块链的安全性以及操作上的便利性。

### 3.5 区块链让数据分享更安全

在受信任的利益相关者之间通过可靠的数据共享达成共识，而非使用付费的中心化的分享机构提供的服务，是实现物联网广泛合作的关键。在工业物联网中实现安全和智能数据交换的一种可能方法是区块链与联邦学习的结合。

### 3.6 工业物联网中的区块链

由于区块链节点会相互进行信息传递，在工业物联网中，一处发生故障，所有节点都将知道此事，从而降低发生事故的概率。其缺点是引入了很多额外的计算开销，故轻量化架构的区块链迫在眉睫。

### 3.7 用于物联网身份认证的区块链

大多数身份认证算法均是为集中式网络设计。区块链的目标之一，就是提出一种新型数据格式，支持存储不受外界扰动的分布式交易记录。

## 4.  区块链的工业化应用

泰国的电力市场正在考虑采用P2P技术进行升级，降低交易成本。