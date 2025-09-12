## Description/简介

`OneAPI`专业的接口数据服务。提供：Douyin（抖音）、Xiaohongshu（小红书）、Kuaishou（快手）、Bilibili（哔哩哔哩）、Weibo（微博）、Toutiao（今日头条）、Xigua（西瓜视频）、Lemon8、Tiktok、Youtube等接口、数据、API

我们是一家专业的数据服务提供商，提供标准的 HTTP 接口服务，并可根据您的需求定制化数据服务。

[官网](https://getoneapi.com/) | [接口文档](https://doc.getoneapi.com/)

## Contact information/联系方式

可通过以下方式联系我们：

- **邮箱**: support@getoneapi.com
- **Telegram**: [t.me/GetOneAPI](https://t.me/GetOneAPI)

如有任何问题，欢迎联系我们。

## API list/API 列表

以下是我们目前提供的各平台接口服务。此列表可能更新不及时，可通过在线实时接口文档，查看最新 API 列表。

### Xiaohongshu/小红书

- 小红书笔记详情
- 小红书用户
- 小红书用户笔记列表
- 小红书笔记评论
- 小红书笔记子评论
- 小红书笔记搜索
- 小红书用户搜索
- 小红书主页Feed流

### 抖音（视频）

- 抖音视频详情
- 抖音用户详情
- 抖音用户视频列表
- 抖音搜索视频
- 抖音搜索用户

### 快手

- 快手视频详情
- 快手用户详情
- 快手用户视频列表
- 快手搜索用户

### 淘宝

- 淘宝商品详情(带优惠券信息，券后价，销量，sku信息)
- 淘宝商品评论
- 淘宝店铺商品列表
- 淘宝商品销量（滚动30天精确销量）
- 淘宝搜索商品
- 淘宝商品描述（商品底部描述图）

### 拼多多（可合作）

- 商品详情
- 商品搜索
- 店铺商品列表


### 京东外卖

- 按经纬度获取商家信息

### 美团

- 美团商超药店

### 抖音电商

- 抖音商品详情

### 抖音（电商）

- 抖音小黄车（小黄车直播间商品列表）
- 抖音店铺商品列表
- 抖音商品评论

### Temu

- Temu商品详情

### Lazada

- Lazada商品详情

### SHEIN

- SHEIN商品详情

### Shopee

- Shopee商品详情

### 京东

- 京东商品详情

### 微信公众号

- 微信公众号用户发文
- 微信公众号文章阅读点赞
- 微信公众号文章评论
- 微信公众号搜索

### 小红书蒲公英

- 蒲公英平台KOL各类数据

### 抖音星图

- 蒲公英平台KOL各类数据

### 腾讯广告互选

- 腾讯广告互选平台KOL各类数据

### 大众点评

- 店铺基本信息

### 微博

- 微博搜索
- 微博详情

### 其他

- 哔哩哔哩
- 知乎
- Bigo
- 贝壳
- 百度指数
- 携程
- Boss直聘
- 智联招聘
- 拉钩
- 今日头条
- Facebook
- YouTube
- Instagram
- Twitter

## User Guide/使用导览

#### 注册账号

注册地址  [https://getoneapi.com/register](https://getoneapi.com/register)

#### Authorization/鉴权

要访问我们的 API，您必须在每个请求的请求头中添加您的API秘钥进行身份验证：

- 请求头
```js
Authorization: Bearer <your_apikey>
```
- 示例请求

```js
curl -X POST https://api.getoneapi.com/api/douyin/user_detail 
     -H "Content-Type: application/json" 
     -H "Authorization: Bearer 5hlBzQDigT4GZJRTL3GeUSxIAC2W0t4gjvn8fizJCCsawhFS1I2R4T8DbhqXYV6v" 
     -d '{"sec_user_id": "xxxxx"}'
```
要获取API密钥，请[注册](https://getoneapi.com/register)。

#### Response/响应
- 所有 API 响应都返回 HTTP 状态代码 200 OK，无论业务结果如何。
- 您必须依赖 JSON 响应主体中的 code 字段来确定业务级结果。

示例响应
```js
{
  "code": 200,
  "message": "",
  "data": { ... }
}
```
业务代码参考
| code | 说明 | 计费 |
| --- | --- |--- |
| 200 | 成功 | YES |
| 0 | 失败 | NO |
| 401 | 未授权，APIKey无效 | NO |
| 403 | 账户不可用 | NO |
| 404 | API未找到或不可用 | NO |
| 301 | 余额不足 | NO |


超时建议
:::highlight blue 💡
虽然大多数 API 请求会在几秒钟内响应，但我们建议将请求超时设置为至少 60 秒。
这并不表示我们的 API 很慢——它只是有助于避免由于临时网络问题或客户端超时而导致的意外错误或重复收费。
:::

#### Request rate/速率限制

- API 使用没有通用速率限制。
- 少数高流量端点可能有特定的速率限制（例如每分钟/小时），这将在各自的文档中注明。

## Support&Feedback/支持与反馈
如有任何疑问、定价详情、定制API，请随时通过我们的支持页面联系我们：

[联系我们](https://getoneapi.com/contact)

⭐ 如果这个项目对您有帮助，请给我们一个Star！
