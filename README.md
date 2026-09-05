# 聚影TV · 订阅仓库（分发）

本仓库仅托管「订阅仓库」功能的每日更新产物：

| 路径 | 内容 |
|---|---|
| `dist/repo.b64` | 每日订阅清单（RC4+Base64 加密 blob，App 端解密消费） |
| `dist/repo.json` | 同上的明文 manifest（供 App 建立清洗镜像映射） |
| `generated/subs/*.json` | 清洗后的各订阅配置内容（App 添加订阅时直连下载） |
| `generated/subs_bundle.json` | 全部清洗订阅的整包（加速批量加载） |
| `generated/*.txt` | 筛选后的直播源文件 |
| `generated/sources.json` / `parsers.json` | 采集站 / 解析端口清单 |

产物由**私有构建流水线**每日 05:00（北京时间）自动重建并同步到本仓库。
构建脚本、筛选与维护逻辑不在本仓库公开。

> ⚠️ 请勿 fork 本仓库做分发：产物每日更新且已加密，fork 副本会立即失效。
