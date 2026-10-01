# Agent Pet

一个在浏览器里玩耍的 AI 宠物社区：领养自己的宠物，喂养、聊天、结交朋友，一起探索公共广场。

## 第一版

- 3 种可选宠物，可以取名和选择性格。
- 一张社区广场地图，宠物可以走动。
- 喂食、抚摸、玩耍和休息，保存心情、饱食度和亲密度。
- 个人小屋、串门和基础好友互动。
- 社区活跃天数和连续陪伴天数排行榜。
- 真实 AI 宠物聊天、社区内记忆和简单冒险剧情。

## 本地 ChatGPT 接入

首版在用户电脑上运行网页和本地服务，用户通过浏览器完成官方 ChatGPT OAuth 授权。本地服务接收回调、保存授权，并调用符合订阅授权条件的 Responses 请求。

参考 Tars 的授权实现，为本项目单独注册和授权。用户的模型请求使用各自授权的订阅额度；喂养、移动和换装由游戏规则处理。

公共网站的 ChatGPT 登录与订阅用量接入，取得对应资格后再联调。排行榜先统计社区内活动，不读取用户在整个 ChatGPT 产品中的历史用量。

官方参考：

- [ChatGPT plan usage](https://developers.openai.com/siwc/token-sharing-open-source)
- [Registration and sign-in](https://developers.openai.com/siwc/token-sharing-open-source/sign-in)
- [On your website](https://developers.openai.com/siwc/website)

## 当前状态

已建立项目目录并确定首版范围。社区页面、本地服务和登录流程尚未实现。
