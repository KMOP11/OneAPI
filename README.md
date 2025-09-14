## Description/简介

OneAPI，提供：Douyin（抖音）、Xiaohongshu（小红书）、Kuaishou（快手）、Bilibili（哔哩哔哩）、Weibo（微博）、Toutiao（今日头条）、Xigua（西瓜视频）、Lemon8、Tiktok、Youtube等接口、数据、API、爬虫、采集。包括但不限于用户信息、视频列表、视频详情、点赞数据、评论数据、综合搜索等 

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

- 小红书用户信息
- 小红书用户笔记列表
- 小红书笔记详情
- 小红书笔记评论
- 小红书笔记子评论
- 小红书笔记搜索
- 小红书用户搜索
- 小红书获取搜索联想词
- ...

### Douyin/抖音

- 抖音用户信息
- 抖音用户作品列表
- 抖音视频详情
- 抖音视频一级评论
- 抖音视频子评论
- 抖音直播间信息
- 抖音直播间用户列表
- 抖音检查用户是否直播
- 抖音综合搜索
- 抖音搜索视频
- 抖音搜索用户
- 抖音搜索话题
- 抖音话题详情
- 抖音话题下的视频
- 抖音搜索音乐
- 抖音音乐相关的视频
- 抖音用户标签
- 抖音用户合集
- 抖音合集下的视频
- ...

### Kuaishou/快手

- 快手用户信息
- 快手用户作品列表
- 快手视频详情
- 快手视频评论
- 快手热搜榜单
- 快手视频分享短链
- ...

### Bilibili/哔哩哔哩

- 用户信息
- 用户主页作品列表
- 作品详情
- 作品评论
- 搜索数据
- 综合热门
- 排行榜
- ...

### Weibo/微博

- 用户信息
- 用户发布
- 用户视频列表
- 作品详情
- 作品评论
- 作品子评论
- 话题数据
- 话题详情
- 微博热搜列表
- 综合搜索
- ...


### Toutiao/今日头条

- 用户信息
- 用户发布
- ...

### Xiguashipin/西瓜视频

- 用户信息
- 用户发布
- ...

### Tiktok

- 用户信息
- 用户发布
- ...

### Youtube

- 用户信息
- 用户发布
- ...

### Lemon8

- 用户信息
- 用户发布
- ...

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

虽然大多数 API 请求会在几秒钟内响应，但我们建议将请求超时设置为至少 60 秒。
这并不表示我们的 API 很慢——它只是有助于避免由于临时网络问题或客户端超时而导致的意外错误或重复收费。


#### Request rate/速率限制

- API 使用没有通用速率限制。
- 少数高流量端点可能有特定的速率限制（例如每分钟/小时），这将在各自的文档中注明。

## Support&Feedback/支持与反馈
如有任何疑问、定价详情、定制API，请随时通过我们的支持页面联系我们：

[联系我们](https://getoneapi.com/contact)

⭐ 如果这个项目对您有帮助，请给我们一个Star！
