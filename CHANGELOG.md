# WEX API 文档更新日志

> 更新日期：2026-04-02
> 参考来源：XT 最新 API 文档 (xt-api)
> 范围：现货交易 + 合约交易（中英文双语）

---

## 一、基础设施变更

| 文件 | 变更内容 |
|------|----------|
| `_config.yml` | 新增 14 个合约交易 Jekyll collections（7 英文 + 7 中文） |
| `_layouts/default.html` | 添加 Spot / Futures 标签切换、合约侧边栏、更新 JS 导航逻辑 |
| `index.html` | 添加合约交易内容区块 `{% include futures.html %}` |

---

## 二、现货文档更新

### 2.1 接入说明

| 文件 | 变更内容 |
|------|----------|
| apiBasicInfo | 添加 bold 格式强调 "query Params"、"request body"、"signed" |
| limitRules | 重构为项目符号列表 + bold 格式，结构更清晰 |
| signStatement | 全部重写：改为 5 步结构化说明，新增 recvwindow 详细解释，添加"时间戳超前 1 秒即拒绝"的说明 |
| signSteps | 更新示例密钥；重写 Data Part / Header Part / Generate Signature / Complete Example 四大章节；添加 Content-Type 一致性和 raw JSON 签名注意事项 |
| applyApi | 更新 Zendesk 链接为 WEX 支持地址 |
| apiDemo | 更新 SDK 链接到 GitHub（Java / Golang / C# demo），添加 sample request 链接 |
| returnFormat | 修复 JSON 格式（缺少逗号等） |
| errorCode | 新增错误码：SYMBOL_007、SYMBOL_010、SYMBOL_011、ORDER_F0503、ORDER_F0504、ORDER_F0704，更新已有错误码描述 |
| publicModule | 更新 IOC / GTX 描述，改善中文标签 |
| FAQ | 重新格式化为结构化项目符号 + bold 强调 |
| **contactUs** | **新建**：Telegram 群组、Zendesk 客服、在线支持链接 |

### 2.2 订单

| 文件 | 变更内容 |
|------|----------|
| orderPost | 新增 `nftId` 参数；限流 50 → **20**/s/apikey；新增 Remark（买入/卖出市价单规则）；响应新增 `ip` 字段 |
| orderGet | 限流 100 → **10**/s/apikey；响应新增 `ip` 字段；更新响应注释 |
| orderGetQueryParam | 新增限流 50/s/apikey（原来缺失）；更新参数/响应描述 |
| orderDel | 限流 100 → N/A；修正英文标题拼写 "Cancell" → "Cancel" |
| openOrderGet | 响应新增 `ip` 字段 |
| openOrderDel | `bizType` 参数从 mandatory=false 改为 **mandatory=true** |
| batchOrderGet | 响应新增 `ip` 字段；改善 content_markdown 文本 |
| batchOrderDel | 描述和说明文本微调 |
| historyOrderGet | 响应新增 `ip` 字段；改善 startTime / endTime / hiddenCanceled / state 参数描述 |
| **batchOrderPost** | **新建**：POST `/v4/batch-order`，含 item.* 嵌套参数，限流 30/s/apikey |
| **orderUpdate** | **新建**：PUT `/v4/order/{orderId}`，参数 orderId / price / quantity，限流 50/s/apikey |

### 2.3 市场数据

| 文件 | 变更内容 |
|------|----------|
| 1serverInfo | 清理空参数占位符 |
| 2symbol | 限流 100 → **10**/s/ip；响应移除废弃字段（`id`、`baseCurrencyId`、`quoteCurrencyId`、`plates`）；新增 `takerFeeRate`、`makerFeeRate`；简化 Filter 文档 |
| 3depth | 默认 limit 50 → **100**；限流 200 → **10**/s/ip |
| 4kline | 限流 100 → **10**/s/ip |
| 5tradeRecent | 限流 100 → **10**/s/ip；ranges 格式修正 `1，1000` → `1~1000` |
| 6tradeHistory | 限流 100 → **10**/s/ip；ranges 格式修正 |
| 7allTicker | 限流 100 → **10**/s/ip；更新响应注释 |
| 8tickerPrice | 限流 100 → **10**/s/ip；修复 JSON 语法（缺少逗号） |
| 9tickerBook | 限流 100 → **10**/s/ip；更新响应注释 |
| 10ticker24h | 限流 100 → **10**/s/ip |
| **11clientInfo** | **新建**：GET `/v4/public/client`，返回客户端 IP |

### 2.4 成交

| 文件 | 变更内容 |
|------|----------|
| tradeGet | 更新参数描述（Business type / Order side / Order type / Query direction / 时间格式示例）；响应新增字段：`deductType`、`deductFee`、`couponAmount`、`couponCurrency` |

### 2.5 资产

| 文件 | 变更内容 |
|------|----------|
| balanceGet | 修复 `currency` 参数名（去除尾部空格）；新增响应字段注释（currency / frozen / available / total / btcValuation） |
| balancesGet | 更新限流文本；改善参数描述；新增响应字段注释 |
| currenciesGet | 更新响应注释（币种符号 / 全名 / CoinMarketCap 链接 / 权重排名 / 最大精度 / 充提状态描述） |

### 2.6 WebSocket Public

| 文件 | 变更内容 |
|------|----------|
| base | 从简单 URL 扩展为完整内容：新增请求头 `Sec-WebSocket-Extensions: permessage-deflate`，新增 Python 连接示例和响应示例 |
| requestFormat | 新增 Subscribe / Unsubscribe 代码块 + 响应示例 |
| heartBeat | 明确说明发送文本 `"ping"` 接收 `"pong"`，新增请求/响应代码块 |
| pushMessage | 新增 `oi`（orderId）和 `v`（quoteQty）字段 |
| dealRecord | 新增 `oi`（orderId）和 `v`（quoteQty）字段 |
| subscribeParam | 新增响应示例 |
| orderBook | URL 域名更新 |
| limitDepth | 响应数据对齐（移除多余 `t` 字段） |
| tickerRealTime | 修复 JSON 尾部逗号 |

### 2.7 WebSocket Private

| 文件 | 变更内容 |
|------|----------|
| base | URL 更新为 `wss://stream.wexex.io/private` |
| getToken | 新增限流说明（1 req/10s/apikey）、token 有效期（2 天）、重置行为、listenKey 等价关系；新增 curl 示例 |
| requestFormat | 新增 listenKey 必填说明 + id 匹配说明 |
| responseFormat | 修复中文版 code 值文档（1=成功 → **0=成功**） |
| pushMessage | 新增 `oi`、`v` 字段 |
| balanceChange | 新增订阅示例（含 listenKey）；新增 SPOT / LEVER 支持说明 |
| entrustChange | 新增订阅示例；新增触发单跟踪描述 |
| orderChange | 新增订阅示例；新增完整订单状态列表（NEW / PARTIALLY_FILLED / FILLED / CANCELED / REJECTED / EXPIRED） |
| orderDeal | 新增 `oi`（orderId）、`v`（quoteQty）、`b`（buyerMaker）、`tm`（taker/maker）字段；新增订阅示例 |

---

## 三、合约文档（全部新建）

### 3.1 接入说明（6 个文档）

| 文件 | 内容 |
|------|------|
| apiBasicInfo | USDT-M `fapi.wexex.io` / Coin-M `dapi.wexex.io`，请求方式、认证头、限流说明 |
| signStatement | 第三方平台安全性说明、防篡改 / 防重放 / 防过期机制 |
| signSteps | Data Part + Header Part + HMAC-SHA256 生成 + 完整示例 |
| applyApi | Zendesk 创建 API Key 流程 |
| errorCode | 合约特有错误码表 |
| changelog | API 版本变更记录 |

### 3.2 订单（16 个接口）

| 文件 | 接口路径 | 说明 |
|------|----------|------|
| createOrder | POST `/future/trade/v1/order/create` | 创建订单 |
| updateOrder | POST `/future/trade/v1/order/update` | 修改订单 |
| bulkOrders | POST `/future/trade/v1/order/create-batch` | 批量下单 |
| batchOrderPlacement | POST `/future/trade/v2/order/atomic-create-batch` | 原子批量下单 |
| seeOrdersById | GET `/future/trade/v1/order/detail` | 按 ID 查询 |
| seeOrders | GET `/future/trade/v1/order/list` | 查询订单列表 |
| cancelOrder | POST `/future/trade/v1/order/cancel` | 取消订单 |
| batchCancelOrders | POST `/future/trade/v1/order/cancel-batch` | 批量取消 |
| cancelAllOrders | POST `/future/trade/v1/order/cancel-all` | 取消全部 |
| getOpenOrderList | GET `/future/trade/v1/order/list-open` | 当前挂单 |
| seeOrderHistory | GET `/future/trade/v1/order/list-history` | 历史订单 |
| seeTransactionDetails | GET `/future/trade/v1/order/trade-list` | 成交明细 |
| partialCanceledOrders | GET `/future/trade/v1/order/list-canceled` | 部分撤单 |
| orderList | GET `/future/trade/v1/order/OrderList` | 订单列表 |
| quantOrderHistory | GET `/future/trade/v1/order/quant-list-history` | 量化历史订单 |
| quantTradeList | GET `/future/trade/v1/order/quant-trade-list` | 量化成交列表 |

### 3.3 行情数据（22 个接口）

| 文件 | 接口路径 | 说明 |
|------|----------|------|
| 1-get-client-ip | GET `/future/market/v1/public/client` | 客户端 IP |
| 2-get-trading-pair-currency | GET `/future/market/v1/public/symbol/coins` | 交易对币种 |
| 3-get-config-single-trading-pair | GET `/future/market/v1/public/symbol/detail` | 单交易对配置 |
| 4-get-config-listed-tradeable-symbols | GET `/future/market/v1/public/symbol/list` | 可交易配置列表 |
| 5-leverage-stratification | GET `/future/market/v1/public/leverage/bracket` | 杠杆分层 |
| 6-get-market-info-specific | GET `/future/market/v1/public/q/ticker` | 指定交易对行情 |
| 7-get-market-info-all | GET `/future/market/v1/public/q/tickers` | 全部行情 |
| 8-get-latest-transaction | GET `/future/market/v1/public/q/deal` | 最新成交 |
| 9-get-depth-data | GET `/future/market/v1/public/q/depth` | 深度数据 |
| 10-get-index-price-single | GET `/future/market/v1/public/q/index-price` | 指数价格（单） |
| 11-get-index-price-all | GET `/future/market/v1/public/q/index-prices` | 指数价格（全） |
| 12-get-mark-price-single | GET `/future/market/v1/public/q/mark-price` | 标记价格（单） |
| 13-get-mark-price-all | GET `/future/market/v1/public/q/mark-prices` | 标记价格（全） |
| 14-get-kline | GET `/future/market/v1/public/q/kline` | K 线 |
| 15-get-agg-ticker-specific | GET `/future/market/v1/public/q/agg-ticker` | 聚合行情（单） |
| 16-get-agg-ticker-all | GET `/future/market/v1/public/q/agg-tickers` | 聚合行情（全） |
| 17-get-funding-rate | GET `/future/market/v1/public/q/funding-rate` | 资金费率 |
| 18-get-funding-rate-records | GET `/future/market/v1/public/q/funding-rate-record` | 资金费率记录 |
| 19-get-ask-bid-specific | GET `/future/market/v1/public/q/ticker-book` | 买卖盘（单） |
| 20-get-ask-bid-all | GET `/future/market/v1/public/q/ticker-books` | 买卖盘（全） |
| 21-get-risk-fund-balance | GET `/future/market/v1/public/q/risk-fund` | 风险基金 |
| 22-get-open-interest | GET `/future/market/v1/public/q/open-interest` | 持仓量 |

### 3.4 账户（25 个接口）

| 文件 | 接口路径 | 说明 |
|------|----------|------|
| 1-get-account-info | GET `/future/user/v1/account/info` | 账户信息 |
| 2-get-contract-account-assets | GET `/future/user/v1/account/assets` | 合约账户资产 |
| 3-get-listen-key | GET `/future/user/v1/user/listen-key` | ListenKey |
| 4-open-contract | POST `/future/user/v1/account/open` | 开通合约 |
| 5-get-single-currency-fund | GET `/future/user/v1/balance/detail` | 单币种资金 |
| 6-get-user-funds | GET `/future/user/v1/balance/list` | 用户资金 |
| 7-get-account-flow | GET `/future/user/v1/balance/bills` | 账户流水 |
| 8-get-fund-fee | GET `/future/user/v1/balance/fund-fee` | 资金费用 |
| 9-get-active-position | GET `/future/user/v1/position/active-list` | 活跃持仓 |
| 10-get-position-info | GET `/future/user/v1/position/list` | 持仓信息 |
| 11-get-step-rate | GET `/future/user/v1/account/step-rate` | 阶梯费率 |
| 12-adjust-leverage | POST `/future/user/v1/position/adjust-leverage` | 调整杠杆 |
| 13-alter-margin | POST `/future/user/v1/position/margin` | 调整保证金 |
| 14-alter-auto-margin | POST `/future/user/v1/position/auto-margin` | 自动追加保证金 |
| 15-close-all | POST `/future/user/v1/position/close-all` | 一键平仓 |
| 16-get-adl-info | GET `/future/user/v1/position/adl` | ADL 信息 |
| 17-collect-trading-pair | POST `/future/user/v1/user/collection/add` | 收藏交易对 |
| 18-cancel-collection | POST `/future/user/v1/user/collection/cancel` | 取消收藏 |
| 19-list-collected-pairs | GET `/future/user/v1/user/collection/list` | 收藏列表 |
| 20-change-position-type | POST `/future/user/v1/position/change-type` | 切换持仓模式 |
| 21-get-margin-call-info | GET `/future/user/v1/position/margin-call` | 强平信息 |
| 22-get-auto-deleverage-history | GET `/future/user/v1/position/adl-history` | ADL 历史 |
| 23-get-single-coin-balance | GET `/future/user/v1/balance/coin` | 单币余额 |
| 24-get-taker-over-list | GET `/future/user/v1/position/taker-over` | 接管列表 |
| 25-get-profit-list-history | GET `/future/user/v1/position/profit-history` | 盈亏历史 |

### 3.5 委托（28 个接口）

| 文件 | 接口路径 | 说明 |
|------|----------|------|
| createStopLimit | POST `/future/trade/v1/entrust/create-profit` | 创建止盈止损 |
| seeStopLimit | GET `/future/trade/v1/entrust/profit-list` | 查询止盈止损 |
| seeStopLimitByProfitId | GET `/future/trade/v1/entrust/profit-detail` | 按 ID 查询 |
| alterStopLimit | POST `/future/trade/v1/entrust/update-profit` | 修改止盈止损 |
| cancelStopLimit | POST `/future/trade/v1/entrust/cancel-profit` | 取消止盈止损 |
| cancelAllStopLimit | POST `/future/trade/v1/entrust/cancel-all-profit` | 取消全部止盈止损 |
| createTriggerOrders | POST `/future/trade/v1/entrust/create-plan` | 创建触发单 |
| seeTriggerOrders | GET `/future/trade/v1/entrust/plan-list` | 查询触发单 |
| seeTriggerOrdersByEntrustId | GET `/future/trade/v1/entrust/plan-detail` | 按 ID 查询触发单 |
| seeTriggerOrdersHistory | GET `/future/trade/v1/entrust/plan-list-history` | 触发单历史 |
| cancelTriggerOrders | POST `/future/trade/v1/entrust/cancel-plan` | 取消触发单 |
| cancelAllTriggerOrders | POST `/future/trade/v1/entrust/cancel-all-plan` | 取消全部触发单 |
| createTrack | POST `/future/trade/v1/entrust/create-track` | 创建追踪单 |
| getTrackList | GET `/future/trade/v1/entrust/track-list` | 查询追踪单 |
| getHistoryTrackList | GET `/future/trade/v1/entrust/track-list-history` | 追踪单历史 |
| getSingleTrackDetail | GET `/future/trade/v1/entrust/track-detail` | 追踪单详情 |
| cancelTrack | POST `/future/trade/v1/entrust/cancel-track` | 取消追踪单 |
| cancelAllTrack | POST `/future/trade/v1/entrust/cancel-all-track` | 取消全部追踪单 |
| queryReversePlan | GET `/future/trade/v1/entrust/reverse-plan` | 反向计划查询 |
| reversePlanListHistory | GET `/future/trade/v1/entrust/reverse-plan-history` | 反向计划历史 |
| getPositionHistory | GET `/future/trade/v1/entrust/position-history` | 持仓历史 |
| getLeverageInfo | GET `/future/trade/v1/entrust/leverage-info` | 杠杆信息 |
| getCrossMargin | GET `/future/trade/v1/entrust/cross-margin` | 全仓保证金 |
| getActivePosition | GET `/future/trade/v1/entrust/active-position` | 活跃持仓 |
| profitListHistory | GET `/future/trade/v1/entrust/profit-list-history` | 盈亏历史 |
| tradeHistory | GET `/future/trade/v1/entrust/trade-history` | 成交历史 |
| tradeListAll | GET `/future/trade/v1/entrust/trade-list-all` | 全部成交 |
| queryAllOrders | GET `/future/trade/v1/entrust/order-all` | 全部订单 |

### 3.6 WebSocket Public（10 个频道）

| 文件 | 订阅 Topic | 说明 |
|------|------------|------|
| generalWssInfo | `wss://fstream.wexex.io/ws/market` | 基本信息 |
| orderbookManage | — | 订单簿管理指南 |
| tradeRecord | `trade@{symbol}` | 成交记录 |
| kline | `kline@{symbol},{interval}` | K 线 |
| aggTicker | `agg_ticker@{symbol}` | 聚合行情 |
| indexPrice | `index_price@{symbol}` | 指数价格 |
| markPrice | `mark_price@{symbol}` | 标记价格 |
| incrementalDepth | `depth_update@{symbol}` | 增量深度 |
| limitedDepth | `depth@{symbol},{levels}` | 限制深度 |
| fundRate | `fund_rate@{symbol}` | 资金费率 |

### 3.7 WebSocket Private（6 个频道）

| 文件 | 订阅 Topic | 说明 |
|------|------------|------|
| generalWssInfo | `wss://fstream.wexex.io/ws/user` | 基本信息 |
| userOrder | `order@{ListenKey}` | 用户订单 |
| balanceChange | `balance@{ListenKey}` | 余额变更 |
| changePosition | `position@{ListenKey}` | 持仓变更 |
| transactions | `trade@{ListenKey}` | 成交推送 |
| message | `notify@{ListenKey}` | 通知消息 |

---

## 四、全局品牌替换

| 替换项 | 原值 | 新值 |
|--------|------|------|
| 现货 REST | `sapi.xt.com` | `sapi.wexex.io` |
| 现货 WS | `stream.xt.com` | `stream.wexex.io` |
| 合约 USDT-M | `fapi.xt.com` | `fapi.wexex.io` |
| 合约 Coin-M | `dapi.xt.com` | `dapi.wexex.io` |
| 合约 WS | `fstream.xt.com` / `fstream.x.group` | `fstream.wexex.io` |
| 交易对示例 | `XT_USDT` | `BTC_USDT` |
| Telegram | `t.me/XT_api` | `t.me/WEX_api` |
| 客服 | `xtsupport.zendesk.com` | `wexsupport.zendesk.com` |
| 品牌文本 | `XT API` / `XT` | `WEX API` / `WEX` |

---

## 五、统计

| 类别 | 数量 |
|------|------|
| 修改文件 | 113 |
| 新增文件 | 235 |
| 总计 | 348 |
| 新增行数 | 19,257 |
| 修改行数 | 1,961 |
