# 家宽vps怎么选：$25/月的美国家宽够用吗？双ISP和单ISP差在哪？AS9929回程值不值每月多花$10？（附SixtyNet全套餐价格表与IP验真三步法）

家宽 VPS 现在的行情大致分两档：美国住宅 IP 的入门款月付 $25 上下，带回中国优化线路的版本 $35 起。SixtyNet 两条线都在卖，官网当前列出的 13 个套餐里，普通读者真正需要看的其实只有四个，其余要么是机房 IP，要么是给批量业务和大带宽场景准备的。

下面把价格表、两条住宅线的实际差别、以及付款前怎么验证 IP 是不是真家宽讲清楚。验 IP 那部分建议先看完再下单，因为商家页面写“住宅 IP”和 `ipinfo.io` 查出来 `type` 是 `isp`，是两件事。

> **选购速览**：既要美国住宅 IP、又在意国内访问速度，选 IRVINE-PRO-STARTER，$35/月或 $350/年，2 核 2G、40G NVMe、5TB 流量、AS9929 回程、Cox 双 ISP 住宅 IP。预算优先、能接受普通国际线路的，选 Residential-STARTER，$25/月或 $260/年。
> 👉 [查看 SixtyNet 住宅 IP 全部套餐与当前库存](https://sixtynet.net/vps-hosting?aff=39)

## SixtyNet 全套餐价格表

官网把产品分成四条线：AT&T Mobility 住宅 IP、Cox 双 ISP 住宅 IP（IRVINE-PRO）、洛杉矶机房 IP、以及一条 BGP 大带宽。全部美元计价，年付都有 13%–17% 的折扣。

### 住宅 IP 系列（AT&T Mobility）

| 套餐 | CPU / 内存 / 硬盘 | 端口 / 流量 | 价格 | 购买 |
| --- | --- | --- | --- | --- |
| Residential-STARTER | 2 核 / 2G / 40G NVMe | 2G / 5TB 月 | $25/月；$260/年（原价 $300） | [订购 STARTER](https://sixtynet.net/index.php?rp=/store/at-and-t-mobility-residential/att-moble-starter&aff=39) |
| Residential-MICRO | 4 核 / 4G / 80G NVMe | 4G / 10TB 月 | $45/月；$460/年（原价 $540） | [订购 MICRO](https://sixtynet.net/index.php?rp=/store/at-and-t-mobility-residential/att-moble-micro&aff=39) |
| Residential-MEDIUM | 8 核 / 8G / 160G NVMe | 10G / 20TB 月 | $85/月；$860/年（原价 $1,020） | [订购 MEDIUM](https://sixtynet.net/index.php?rp=/store/at-and-t-mobility-residential/att-moble-medium&aff=39) |
| Residential-LARGE | 16 核 / 16G / 320G NVMe | 10G / 40TB 月 | $165/月；$1,660/年（原价 $1,980） | [订购 LARGE](https://sixtynet.net/index.php?rp=/store/at-and-t-mobility-residential/att-moble-large&aff=39) |

### 住宅 Pro 系列（Cox 双 ISP + AS9929，加州尔湾）

| 套餐 | CPU / 内存 / 硬盘 | 端口 / 流量 | 价格 | 购买 |
| --- | --- | --- | --- | --- |
| IRVINE-PRO-STARTER | 2 核 / 2G / 40G NVMe | 2G / 5TB 月 | $35/月；$350/年（原价 $420） | [订购 IRVINE-PRO-STARTER](https://sixtynet.net/vps-hosting?aff=39) |
| IRVINE-PRO-MICRO | 4 核 / 4G / 80G NVMe | 4G / 10TB 月 | $55/月；$550/年（原价 $660） | [订购 IRVINE-PRO-MICRO](https://sixtynet.net/vps-hosting?aff=39) |

### 洛杉矶机房 IP 系列（含 DDoS 防护）

| 套餐 | CPU / 内存 / 硬盘 | 端口 / 流量 | 价格 | 购买 |
| --- | --- | --- | --- | --- |
| LAX-STARTER | 2 核 / 2G / 40G NVMe | 2G / 5TB 月 | $240/年，现 $200 | [查看 LAX 系列](https://sixtynet.net/vps-hosting?aff=39) |
| LAX-MICRO | 4 核 / 4G / 80G NVMe | 4G / 10TB 月 | $480/年，现 $400 | [查看 LAX 系列](https://sixtynet.net/vps-hosting?aff=39) |
| LAX-MEDIUM | 8 核 / 8G / 160G NVMe | 10G / 20TB 月 | $960/年，现 $800 | [查看 LAX 系列](https://sixtynet.net/vps-hosting?aff=39) |
| LAX-LARGE | 8 核 / 16G / 320G NVMe | 10G / 40TB 月 | $1,920/年，现 $1,600 | [查看 LAX 系列](https://sixtynet.net/vps-hosting?aff=39) |
| LAX-Storage-500G | 4 核 / 4G / 300G + 200G RAID10 | 10G / 10TB 月 | $480/年，现 $400 | [查看存储型](https://sixtynet.net/vps-hosting?aff=39) |
| LAX-Storage-1TB | 8 核 / 8G / 700G + 300G RAID10 | 10G / 15TB 月 | $840/年，现 $700 | [查看存储型](https://sixtynet.net/vps-hosting?aff=39) |

### BGP 大带宽（非住宅）

| 套餐 | 线路 | 端口 / 计费 | 价格 |
| --- | --- | --- | --- |
| Los Angeles China Unicom-Premium | 联通 AS9929，免费 BGP 会话 | 100M 基础，3 倍突发，95 计费 | $2,500/年（原价 $3,000） |

这条是给有 AS 号和 BGP 需求的团队准备的，个人用户不用看。

## 两条住宅线差在哪

**Residential 系列用 AT&T Mobility 的住宅 IP，走普通国际线路，$25/月起。IRVINE-PRO 系列用 Cox Communications 的家宽 IP，回程接了 AS9929，$35/月起。** 每月多花 $10，买到的是国内访问体验的差别，不是 IP 纯净度的差别。

公开的第三方测评显示，Cox 这条线三网去程是电信 CN2、联通和移动直连洛杉矶，回程电信和移动走 CN2、联通走 AS9929 + CUII。同一份测评里，`ipinfo` 判定为双 ISP 属性、原生美国 IP、流媒体解锁表现良好。这些结论来自测评方，不是厂商自述，可信度相对高一些。

AT&T Mobility 那条线没有同等级别的第三方回程数据，官网也没有标注中国优化。按常识，普通国际线路的家宽 VPS 在国内晚高峰的体验通常不理想，需要中转才好用。你要是不打算搭中转，$10 的差价别省。

两台机器的硬件都是 AMD EPYC 加 NVMe，页面上标了 IOPS：STARTER/MICRO 是 12500，MEDIUM/LARGE 是 25000。第三方测评提到 I/O 实测约 188MB/s，CPU 跑分不错，不支持 IPv6。

## 家宽 IP 和机房 IP 差在 ASN 这一层

平台风控查的是 IP 的 ASN 归属，不是商家在页面上写了什么。机房 IP 的注册组织是 AWS、DigitalOcean 这类云厂商，住宅 IP 的注册组织是 Comcast、AT&T、Cox 这类民用宽带运营商。TikTok、Netflix、亚马逊这类平台拿到你的连接，第一步看的就是这个字段。

判断方法很直接，SSH 上去跑一条命令：

bash
curl ipinfo.io


返回结果里看 `type` 字段：

json
"org": "AS4134 No.31,Jin-rong Street",
"type": "isp"


`type` 是 `isp`，说明这个 IP 在数据库里挂的是运营商；是 `hosting`，那就是机房 IP，页面写“住宅”“双 ISP”都没用。

顺带把三个常被混用的词分清。原生 IP 说的是 IP 注册国家和机房实际所在国家一致，跟是不是家宽没关系。住宅 IP 说的是 ASN 归属民用宽带运营商。双 ISP 说的是同一个 IP 在两个 ISP 名下都有注册记录，比如 Cox 加另一家。双 ISP 不是给你两个 IP，SixtyNet 的页面也没标注多 IP 配额，需要多个独立 IP 得开多台实例，或者下单前问客服能不能加购。

### 付款前做完这三步验证

1. **查类型**。向客服要测试 IP，`curl ipinfo.io/测试IP` 看 `type`，不是 `isp` 直接放弃。
2. **查黑历史**。`curl https://ipinfo.io/你的IP/abuse` 看历史滥用记录，再用 `curl https://api.abuseipdb.com/api/v2/check?ipAddress=你的IP` 查黑名单库。住宅 IP 是稀缺资源，被反复转卖过的那批早被平台拉黑了。
3. **测回程**。`mtr -rwzbc 100 测试IP地址`。判断标准是国内最后一跳延迟波动超过 5ms、高峰期单方向丢包高于 1%，这种线路 IP 再干净也白搭。SixtyNet 官方屏蔽了 ICMP，普通 mtr 拿不到数据，得用 TCP 模式打 SSH 端口，或者直接让客服提供可测的地址。

👉 [用 $25/月的 STARTER 先验一台，确认 IP 属性再决定要不要上年付](https://sixtynet.net/index.php?rp=/store/at-and-t-mobility-residential/att-moble-starter&aff=39)

## 真实成本：年付省多少，第二年怎么算

以 IRVINE-PRO-STARTER 为例。月付 $35，一年 $420。年付 $350，一次付清省 $70，折合每月 $29.17。第二年如果按页面标价续费，仍然是 $350，两年总支出 $700，比按月付两年 $840 少 $140。

Residential-STARTER 的账：月付 $25，年付 $260，省 $40，折合每月 $21.67。省得不多，但这档本来就是价格敏感型选择。

四个住宅档位的年付折扣分别是：STARTER 省 $40（13%）、MICRO 省 $80（15%）、MEDIUM 省 $160（16%）、LARGE 省 $320（16%）。折扣力度随配置上升，LARGE 的年付省下的钱够再买一台 STARTER。

跟市场比，这个价格不算便宜。普通美国机房 VPS 年付 $20–30 就能拿下，带双 ISP 住宅 IP 的同配置年付通常在 $60–80 以上。SixtyNet 的 STARTER 是 $260/年，贵出来的部分在配置和流量：2 核 2G、40G NVMe、5TB 月流量、2G 端口，这套参数放在 $80/年 的机器上基本见不到。你付的钱有一部分是买硬件，不全是买 IP。

有两点要提前想清楚。年付一旦过了退款期就退不了，家宽 IP 的可用性受平台风控政策影响，某个段被批量标记的情况行业里发生过。另外 IRVINE-PRO 两个套餐在官网页面上明确标注了“退款仅退到网站余额”，不是退回原支付方式，这条对现金流敏感的人是实打实的成本。

## 按用途选：五种场景对应哪一档

**只访问 ChatGPT、Claude 这类 AI 工具。** 配置要求极低，IP 能过风控就行。Residential-STARTER 的 $25/月够用，年付 $260 更划算。这档不需要 AS9929，AI 工具对延迟不敏感。

**TikTok 单账号或小团队运营。** 选 IRVINE-PRO-STARTER。$35/月买的是稳定回程，视频上传和后台操作对丢包敏感，晚高峰掉包会直接影响发布成功率。

**多账号矩阵。** SixtyNet 每个套餐只配一个 IPv4，多账号意味着多开实例，成本线性叠加。三个号就是三台 STARTER，$75/月。这个场景下它的性价比不如那些明确支持加购 IP 的商家，下单前先问清 IP 加购政策。

**流媒体 4K 解锁。** 4K 需要持续 25Mbps 以上带宽，Residential-MICRO 的 4G 端口和 10TB 流量绰绰有余，$45/月。但如果你只是自己看片、不涉及账号运营，先拿 LAX 机房系列试一下能不能解锁，能解锁就不用为住宅 IP 付溢价。

**跨境电商多店铺。** 每个店铺配独立 IP，逻辑和多账号矩阵一样。IRVINE-PRO-MICRO 的 4 核 4G 能同时跑 ERP 同步和图片上传，$55/月一台，店铺多了要按店数乘。

## 这几类人不用买家宽 VPS

**建站的别买住宅系列。** 官网在 Residential 四个套餐下面都写了同一句提示：出于 IP 风控原因，住宅 IP 产品不开放 80 和 443 端口。IRVINE-PRO 更严格，直接拒绝所有外部探测和扫描，只允许白名单或端口转发的设备访问。拿它建站、跑公开服务，从端口这一层就走不通。要建站选 LAX 系列，$200/年起，带 DDoS 防护。

**跑脚本、做中转、搭代理的也别买。** 这些场景对 IP 的 ASN 归属没有要求，普通 IDC VPS 年付 $20–30 就够，多花的钱买不到对应的收益。

**只想科学上网的同样不必。** 家宽 IP 的价值在于让平台认不出你是机房流量，纯粹的跨境访问用不上这个属性，普通线路加中转更便宜。

## 下单前要确认的四件事

**库存。** 抓取官网时，Residential 四个套餐的订购页面上都标着 0 Available。这个状态随时会变，下单前先问客服补货时间，别付了钱等机器。

**退款条款。** IRVINE-PRO 系列明确写了只退网站余额。其余系列官网没有公开完整的退款说明，问清楚是退原路还是退余额、期限几天，再付款。

**IP 段。** 不同批次上架的段不一样，某些段在特定平台的风控更严。在工单里问当前分配的是哪个段，比买完才发现不能用要省事。

**付款方式。** 公开介绍提到支持支付宝、USDT 和 PayPal，结账页能实际看到可选项，用哪种在你下单那一步确认。
