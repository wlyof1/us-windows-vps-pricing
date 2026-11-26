# 美国 Windows VPS 要花多少钱：授权另算吗、几个人能同时远程、入门档装不装得下（附 sixtynet 全套餐表）

美国 Windows VPS 的公开起步价多在每月 6 到 13 美元之间，但月费只覆盖到第 180 天左右。之后要不要再掏钱，取决于商家怎么处理 Windows 授权，而这件事各家写法完全不同。

sixtynet 是洛杉矶的一家 VPS 商家，卖的是住宅 IP 属性的机器，年付 $200 起，配置为 2 核 / 2 GB / 40 GB NVMe / 5 TB 月流量。它能不能当成"美国 Windows VPS"来买，取决于两件官网没有写清的事：提不提供 Windows Server 镜像、Windows 授权怎么算。价格、套餐和限制下面拆开讲。

> **选购速览**：只跑 1–2 个人的远程桌面、挂 MT4/MT5 或浏览器自动化，看 LAX-STARTER（2 核 2G / 40 GB NVMe / 5 TB，年付 $200，原价 $240）。要同时开多个浏览器实例或跑轻量数据库，直接上 LAX-MICRO（4 核 4G / 80 GB / 10 TB，年付 $400）。下单前问清两件事：有没有 Windows 镜像、授权怎么算；住宅 IP 套餐不开放 80 和 443 端口。
> 👉 [查看 sixtynet 当前套餐与年付价格](https://sixtynet.net/aff.php?aff=39)

## sixtynet 的全部美国套餐

官网把 VPS 分成几条线：洛杉矶住宅 IP 系列（LAX）、中国联通 AS9929 优化线路、存储 VPS，另外还有一条移动网络 IP 的套餐线。页面上展示的是年付价，年付比月付省 17%，季付也有折扣，具体比例页面上没有逐项标注。

| 套餐 | vCPU / 内存 / NVMe | 月流量 | 年付价格 | 购买 |
| --- | --- | --- | --- | --- |
| LAX-STARTER | 2 核 / 2 GB / 40 GB | 5 TB | $200（原 $240） | [ 订购 STARTER](https://sixtynet.net/aff.php?aff=39) |
| LAX-MICRO | 4 核 / 4 GB / 80 GB | 10 TB | $400（原 $480） | [ 订购 MICRO](https://sixtynet.net/aff.php?aff=39) |
| LAX-MEDIUM | 8 核 / 8 GB / 160 GB | 20 TB | $800（原 $960） | [ 订购 MEDIUM](https://sixtynet.net/aff.php?aff=39) |
| LAX-LARGE | 8 核 / 16 GB / 320 GB | 40 TB | $1,600（原 $1,920） | [ 订购 LARGE](https://sixtynet.net/aff.php?aff=39) |
| LAX-Storage-500G | 4 核 / 4 GB / 500 GB RAID 10 | 10 TB | $400 | [ 订购存储 500G](https://sixtynet.net/aff.php?aff=39) |
| LAX-Storage-1TB | 8 核 / 8 GB / 1 TB RAID 10 | 15 TB | $700 | [ 订购存储 1TB](https://sixtynet.net/aff.php?aff=39) |
| Mobile-STARTER | 2 核 / 2 GB / 40 GB | 50 GB | $50 | [ 订购移动 STARTER](https://sixtynet.net/aff.php?aff=39) |
| Mobile-MICRO | 4 核 / 4 GB / 80 GB | 50 GB | $100 | [ 订购移动 MICRO](https://sixtynet.net/aff.php?aff=39) |
| 洛杉矶 联通 AS9929 住宅 IP | 2–16 核 / 2–16 GB / 40–320 GB | 5–40 TB | $2,500（原 $3,000） | [ 查看 AS9929 档](https://sixtynet.net/aff.php?aff=39) |

AS9929 那一档页面上给的是一个整体年价，2/4/8/16 核四组配置列在同一个区块里，没有逐档标价，实际下单时以购买页显示的配置为准。

其余参数单独看：

- 网络：LAX 住宅系列标 2 G 到 10 G Premium Network，存储系列 10 G
- IOPS：2 核与 4 核档 12,500，8 核及以上 25,000
- IP 属性：LAX 与 AS9929 系列为美国住宅 IP，存储系列不是
- DDoS 防护：LAX 与存储系列均标注包含
- 端口：住宅 IP 系列不开放 80 和 443

## Windows 授权：月费之外的第二笔钱

行业内目前有三种做法，都写在商家自己的公开页面上。

第一种，送 180 天评估版，到期自备授权。USAVPS 在 Windows VPS 页写明，每次安装都从微软的 180 天免费评估版开始，到期前必须激活自己的授权才能继续正常运行。

第二种，授权单列为附加项。HostFinch 把 Windows Server 2019 / 2016 Standard 授权挂在结账页，$19.99/月，2022 版要单独询价。一台 $12.99/月 的机器加上授权，实际月支出变成 $32.98。

第三种，宣称不加价。Kamatera 明确写任何操作系统的 VPS 价格相同，Windows 不额外收费。

同一件事三种做法，意味着"$X/月"这个数字单独看没有意义。要问的是第 181 天会发生什么。

sixtynet 官网的 VPS 产品页没有出现 Windows 授权条款，也没有列出 Windows 镜像清单。官网没写的东西不能替它补。下单前用客服问清楚，比事后补授权省事。

## 默认只有 2 个人能同时远程

Windows Server 默认允许两个管理员 RDP 会话同时在线，第三个人登进来，前两个中的一个会被踢掉。要让 5 个人同时用，得向微软买 RDS CAL，按人头或设备计费，和 VPS 配置无关。

所以"我们 6 个人的小团队，买台 8 核 16G 够不够"这个问题，答案不在 CPU 上。配置买多大解决的是性能，会话数解决的是授权。

sixtynet 的 LAX 系列跑的是标准 Windows Server，这条限制一样适用。1–2 人用，STARTER 或 MICRO 的配置完全够；3 人以上，先算 CAL 的钱，再回头看要不要升到 8 核。

👉 [对比 STARTER 与 MICRO 的配置和年付价](https://sixtynet.net/aff.php?aff=39)

## 40 GB 的入门档装 Windows 会偏紧

Windows Server 对系统盘有下限。USAVPS 公开的口径是至少 50 GB，所以他们家 30 GB 的最小档不卖 Windows，Windows 从下一档起。

按这条口径看 sixtynet 的 LAX 系列：40 GB 的 STARTER 装完系统、累积更新和常驻软件之后剩余空间不多，跑挂机脚本没问题，装 SQL Server 或存本地素材会很紧张。80 GB 的 MICRO 是更稳的起点，160 GB 的 MEDIUM 才谈得上"装得下"。

磁盘之外还要看 IOPS。LAX 的 2 核和 4 核档标 12,500 IOPS，8 核及以上 25,000。这个差距在数据库和大量小文件读写上比 CPU 更明显。

👉 [从 80 GB 磁盘的 MICRO 档开始](https://sixtynet.net/aff.php?aff=39)

## Windows Server 版本：2019 别再选，2022 的主流支持刚过

| 版本 | 发布 | 主流支持结束 | 扩展支持结束 |
| --- | --- | --- | --- |
| Server 2019 | 2018 年 11 月 | 2024 年 1 月 | 2029 年 1 月 |
| Server 2022 | 2021 年 8 月 | 2026 年 10 月 | 2031 年 10 月 |
| Server 2025 | 2024 年 11 月 | 2029 年 10 月 | 2034 年 10 月 |

现在是 2026 年 11 月，Server 2022 的主流支持刚过去一个月，安全更新照常发，新功能不再有了。新部署直接要 2025，能省掉几年后的一次迁移。Server 2019 已经过了主流支持快三年，除了老软件兼容，没有理由再选。

sixtynet 提供哪些 Windows 版本，官网没有列。这条和授权一样，得问。

## 住宅 IP 封了 80 和 443，建站直接排除

sixtynet 的 LAX 系列主打美国住宅 IP。第三方测评提到它用的是 Cox Communications 这类家庭宽带运营商，IP 为双 ISP 属性，流媒体解锁表现好，三网回程走 CN2 和 AS9929 高端线路。

住宅 IP 带来两个直接后果。

80 和 443 端口不开放。官网在住宅 IP 套餐下明确写了这一点，原因是 IP 风控。想拿它建站、跑需要公网访问的 Web 服务，这条产品线直接排除。

官方屏蔽 ICMP。测评里提到 PING 不通，排障只能靠控制面板的 VNC 或远程桌面本身。

这台机器适合的场景是"需要一个看起来像美国家庭宽带的 IP，在上面跑 Windows 软件"：流媒体、社媒多账号、广告投放验证、数据采集、挂机脚本。想把 Windows VPS 当 Web 服务器用的，它不是对口的选择，存储系列也不是为建站设计的。

## 按场景选档

- 1–2 人远程桌面、MT4/MT5 挂机、自动化脚本：LAX-STARTER，2 核 2G / 40 GB，年付 $200。前提是确认 Windows 镜像可用，且接受 40 GB 系统盘。
- 多人共用桌面、QuickBooks 或 Sage 50 这类财务软件、轻量 MSSQL：LAX-MICRO，4 核 4G / 80 GB，年付 $400。
- 多个浏览器实例、中型数据库、需要 160 GB 以上本地空间：LAX-MEDIUM，8 核 8G / 160 GB，年付 $800。
- 大量素材、备份、冷数据：LAX-Storage 系列，500 GB RAID 10 与 1 TB 两档，年付 $400 / $700。存储系列不是住宅 IP。
- 需要移动网络 IP：Mobile-STARTER / MICRO，年付 $50 / $100，流量只有 50 GB，跑不了大流量业务。

LAX-LARGE 是 8 核 16 GB 配 320 GB，年付 $1,600。它的核数和 MEDIUM 一样是 8 核，多出来的是内存、磁盘和流量。只有内存确实成为瓶颈时才值得这 $800 的差价。

## 常见问题

**sixtynet 的套餐包含 Windows 授权吗？**
官网 VPS 页面没有公开授权收费条款，也没有列出 Windows 镜像清单。下单前需要确认镜像是否提供、授权是自带还是另购。

**一台机器能几个人同时远程？**
Windows Server 默认 2 个管理员会话。超过 2 人同时使用需要微软的 RDS CAL，和 VPS 套餐无关。

**能装 SQL Server 吗？**
能装。SQL Server Express 免费，但有 10 GB 单库上限和内存限制；标准版和企业版要单独买授权。磁盘上，40 GB 的入门档装完系统和 SQL Server 之后余量很少，建议从 80 GB 起。

**为什么住宅 IP 不能建站？**
住宅 IP 套餐不开放 80 和 443 端口，官网注明是 IP 风控原因。需要对外提供 Web 服务的，这条产品线不适合。

**年付可以退吗？**
官网在 AS9929 住宅 IP 那一档注明退款只退到网站余额。整体退款窗口的公开信息不多，有第三方整理提到是 3 天，比常见的 7 到 30 天短不少。年付金额不小，下单前把退款条款问清楚。

## 下单前的最后判断

只需要一台美国 IP 的 Windows 桌面，1–2 个人用，跑挂机和浏览器：LAX-STARTER，年付 $200。
需要多人共用，或要跑数据库和财务软件：LAX-MICRO 起步，年付 $400。
需要的是标准 Windows 建站环境：住宅 IP 产品线直接排除，80 和 443 关着。

下单前确认两件事：Windows 镜像与授权口径、退款条款。这两条官网都没写全，问一句能省掉后面的麻烦。

👉 [到 sixtynet 看当前套餐与年付折扣](https://sixtynet.net/aff.php?aff=39)
