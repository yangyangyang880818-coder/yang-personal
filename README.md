# YangPersonal · 充满智慧的小羊同学

> 专属工作空间 — 一个淡蓝/渐变蓝主题的单文件个人工作台 SPA，集成记账/资产管理等日常模块。

## ✨ 功能一览

- **首页总览**：今日计划、待办、灵感、体重、运动、饮食、资产（含结余/总资产/股票基金）、明日热量预测
- **每日计划 / 待办事项 / 灵感记录**：每日待办清单，支持重要标记、日期安排
- **体重控制**：体重记录与历史趋势
- **资产管理**（含完整记账模块）：
  - 总览：本月收入/支出、结余
  - 账单：日历筛选、收入/支出记录、9 类支出 + 4 类收入、5 个支付渠道、4 个购物平台
  - 退货标记（记录运费扣减净支出）、预算预警
  - 统计：每日支出日历（点击日期查看当日账单）、饼图（分类占比）、柱状图（近 7 天）、排行榜（Top 10）
  - 设置：分类增删、预算调整、JSON/CSV 导入导出、个人资料
  - 旧数据自动迁移（`localStorage` key `yang-bill-v1` → `yangpersonal_data_v1`）
- **运动打卡 / 饮食记录**：卡路里追踪
- **图表**：Chart.js 4.4（CDN）

## 🚀 快速开始

```bash
# 直接打开
open YangPersonal.html          # macOS
# 或在浏览器中打开该文件

# 本地预览（推荐，便于手机扫码访问）
python3 -m http.server 8765
# 然后访问 http://127.0.0.1:8765/YangPersonal.html
# 局域网手机访问：http://<电脑IP>:8765/YangPersonal.html
```

所有数据通过 `localStorage` 本地持久化，无需后端、可离线使用。

## 📱 iOS 移动端适配

- 底部 Tab 栏（≤960px 自动切换），毛玻璃 + 横向滚动
- 安全区内边距（`env(safe-area-inset-*)`）
- 输入框 16px 字号防止 iOS 聚焦放大
- `100dvh` + `touch-action: manipulation`

## 🛠 技术栈

- 单文件 HTML + CSS + 原生 JavaScript（**无任何框架/构建步骤**）
- Chart.js 4.4（CDN）
- localStorage 持久化
- FileReader + Canvas 头像压缩（256px base64）
- 响应式布局、CSS 变量主题

## 📂 项目结构

```
.
├── YangPersonal.html      # 主程序（全部 HTML + CSS + JS）
├── README.md              # 本文件
└── LICENSE                # 可选
```

## 🔒 隐私

数据全部保存在浏览器本地（`localStorage`），不上传任何服务器。

## 📦 版本

v1.0 · 2026-08-06