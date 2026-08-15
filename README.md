# 📺 0816iptv — TVBox / 影梭 订阅配置

> 聚合多源影视点播 + IPTV 直播源，开箱即用，适合影视仓、TVBox、影梭等兼容 TVBox 协议的视频播放 App。

---

## 📦 仓库文件

| 文件 | 说明 |
|------|------|
| `pz.json` | 主订阅配置（影视点播源 + 直播源 + DNS 配置） |
| `fm.jar` | Spider 解析引擎（MD5 校验） |
| `hotel.txt` | 直播源（M3U HTTP-TS 直链，`#genre#` 分类） |
| `IPTV.txt` | 直播源（rtp 组播流，按省份/运营商标注） |
| `bz.jpg` | 播放器壁纸背景图 |

---

## 🚀 如何订阅

### 方式一：GitHub Pages（推荐，CDN 加速）

```
https://raw.githubusercontent.com/zhongyuan689/0816iptv/master/pz.json
```

### 方式二：Raw 直链

```
https://zhongyuan689.github.io/0816iptv/pz.json
```

> 提示：仓库需开启 GitHub Pages（Settings → Pages → Source: master branch）。如果尚未开启，请使用方式一的 Raw 链接。

---

## 📱 在 TVBox / 影梭 中添加订阅

1. 打开 App，进入「**设置 → 直播配置 / 订阅配置 / 导入配置**」
2. 选择「**添加订阅**」或「**网络订阅**」
3. 粘贴上方任意一个订阅地址
4. 确认加载，等待源列表刷新完成
5. 开始观影 🎉

---

## 📺 内置影视点播源（9 个）

| 名称 | 类型 | 特点 |
|------|------|------|
| 豆瓣 | 内置 CSP | 电影/剧集评分数据 |
| 非凡 | 外部 API | 资源丰富 |
| 优质 | 外部 API | 资源丰富 |
| 天堂 | 外部 API | 资源丰富 |
| 无尽 | 外部 API | 资源丰富 |
| 百度 | 外部 API | 资源丰富 |
| 极速 | 外部 API | 资源丰富 |
| 哔哩 | 内置 CSP | 纪录片 / CCTV / 评书 |
| 推送 | 内置 CSP | 投屏推送 |

---

## 🖥️ 直播源说明

- `hotel.txt` — **M3U HTTP-TS 直链**，适合大多数播放器，频道覆盖：
  - 央视：CCTV1 ~ CCTV16 等
  - 卫视：湖南/浙江/东方/北京等
  - 各省市地方台

- `IPTV.txt` — **rtp 组播流**，按省份/运营商标注（天津联通、江苏电信、浙江联通等），适合局域网/支持组播的设备

> ⚠️ 直播源来自第三方采集，部分链路可能随时失效。如遇全红，请联系源维护者或等待更新。

---

## ⚙️ DNS-over-HTTPS

内置四组公共 DoH（可在 `pz.json` 中查看/修改）：

| 提供商 | 地址 |
|--------|------|
| 114 DNS | `114.114.114.114` |
| 阿里 DNS | `https://dns.alidns.com/dns-query` |
| 腾讯 DoH | `https://doh.pub/dns-query` |
| 360 DoH | `https://doh.360.cn/dns-query` |

---

## 🔄 手动更新源

如果直播源失效，可手动替换 `hotel.txt` / `IPTV.txt` 内容，或等待上游维护者更新后重新拉取订阅。

---

## 📝 相关项目

- 原始项目：[lisa3456.github.io](https://github.com/lisa3456/lisa3456.github.io)
- TVBox 官方仓库：[github.com/catvod/CatVodOpen](https://github.com/catvod/CatVodOpen)

---

## 📄 License

本仓库仅供个人学习与研究使用，请勿用于任何商业或非法用途。
