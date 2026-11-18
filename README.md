# muse-usage-widget

Muse 订阅用量的数据仓库，供小组件 / 脚本读取。每 30 分钟由 Muse 自动查询用量并更新数据文件、推送到本仓库。

## 数据直链

- 首选（GitHub Pages，国内网络一般可直连）：https://xqqhygmh8v-rgb.github.io/muse-usage-widget/data/muse_usage.json
- 备用（raw 源站）：https://raw.githubusercontent.com/xqqhygmh8v-rgb/muse-usage-widget/main/data/muse_usage.json

两个地址内容相同。Pages 地址在每次推送后自动重新发布，通常一两分钟内更新。

## 字段说明（data/muse_usage.json）

| 字段 | 含义 |
|---|---|
| `updated_at` | 这份数据的更新时间（ISO 8601，+08:00） |
| `plan` | 套餐名（如 `Free`） |
| `percent_used` | 本周额度已用百分比 |
| `resets_at` | 本周额度重置时间（ISO 8601，+08:00） |
| `additional_tokens.percent_used` | 永久（额外）额度已用百分比 |
| `additional_tokens.left_label` | 永久额度剩余量文本，如 `31B tokens left` |

本仓库的提交均为自动同步产生。
