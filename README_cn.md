<div align="center">

[English](README.md) | [中文版](README_cn.md)

# Tiny-M

一款基于 [Voron V0](https://github.com/VoronDesign/Voron-0) 的紧凑型 CoreXY 3D 打印机

**成型体积** `150×150×150mm` &nbsp;|&nbsp; **运动系统** `CoreXY` &nbsp;|&nbsp; **固件** `Klipper` &nbsp;|&nbsp; **供电** `24V`

<img src="images/tiny-m_v4.jpg" width="460">

</div>

---

> **致敬 gsl12** — Tiny-M 由 gsl12 设计并在 Voron V0 基础上做了大量优化。2023 年 8 月因健康原因停止维护，V5 永久停留在 beta。本仓库延续开源精神继续维护。

## 🛠 复刻进度

<table>
<tr><th>阶段</th><th>状态</th><th>说明</th></tr>
<tr><td>BOM 与采购</td><td>🔄 <strong>进行中</strong></td><td>型材框架 BOM 已完成，嘉立创已下单 19 根</td></tr>
<tr><td>框架组装</td><td>⬜ 待开始</td><td>等待型材到货</td></tr>
<tr><td>运动系统</td><td>⬜ 待开始</td><td>导轨、电机、同步带</td></tr>
<tr><td>热端与挤出</td><td>⬜ 待开始</td><td></td></tr>
<tr><td>热床</td><td>⬜ 待开始</td><td></td></tr>
<tr><td>电气</td><td>⬜ 待开始</td><td></td></tr>
<tr><td>封箱</td><td>⬜ 待开始</td><td></td></tr>
<tr><td>软件配置</td><td>⬜ 待开始</td><td>Klipper 调试</td></tr>
</table>

<details>
<summary><strong>📝 最近更新</strong></summary>

- **BOM 重构** — 将 gsl12 原版和小辰DIY V2.2 的 BOM 转为中英双语 Markdown（[BOM/](BOM/)）
- **框架已下单** — 19 根 2020 铝型材通过嘉立创（TXCJ）定制加工。详见 [BOM-Frame-JLCFA](BOM/BOM-Frame-JLCFA.md)
- **嘉立创工具** — [`tools/jlc_reorder.py`](tools/jlc_reorder.py) 自动将加工代码重排为嘉立创标准顺序
- **双语文档** — 所有文档均有英文版（`*.md`）和中文版（`*_cn.md`）

</details>

---

## 📦 项目引用

| 项目 | 说明 |
|------|------|
| [gsl12/Tiny-M](https://github.com/gsl12/Tiny-M) | 原作者仓库，V4 |
| [gsl12/Tiny-M-V5-beta](https://github.com/gsl12/Tiny-M-V5-beta) | V5 beta（未完成） |
| [pangqc/voron-tiny-m](https://gitee.com/pangqc/voron-tiny-m) | 小辰DIY 修改版 — 完整 BOM、封箱方案、组装教程 |

## ⚙️ 硬件规格

| | |
|---|---|
| **框架** | 2020 铝型材 |
| **X 轴** | 1× MGN12H 200mm |
| **Y 轴** | 2× MGN9H 200mm |
| **Z 轴** | 2× MGN12H 200mm |
| **电机** | NEMA 17 |

## 🔧 挤出机选项

- [CroXY Sailfin](https://github.com/CroXY3D/Sailfin-Extruder) — 直接驱动
- [Annex Sherpa Mini](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder) — 直接驱动
- [Bondtech LGX Lite](https://www.bondtech.se/product/lgx-lite-extruder-custom/) — 直接驱动
- E3D V6 远程热端 — Bowden

## 📂 目录结构

```
├── BOM/              # 物料清单与采购
├── CAD/              # CAD 源文件
├── DXFs/             # 加工图纸
├── STLs/             # 打印件
├── klipper_firmware/  # Klipper 配置
├── slicer/           # 切片配置
├── tools/            # 工具脚本
└── usermods/         # 社区修改方案
```

## 🖨 打印建议（ABS/ABS+）

| 参数 | 值 |
|------|-----|
| 喷嘴 | 0.4mm |
| 挤出宽度 | 0.48mm |
| 层高 | 0.2–0.3mm |
| 顶/底层 | 5 层 |
| 墙壁 | 4 圈 |
| 填充 | 40%（三角形） |

## 🔗 社区

- [CroXY Discord](https://discord.gg/tmZkjWs) — Tiny-M 频道
- [Mark Hoy's Build Log](https://github.com/mark-hoy/tiny-m-build)
- [小辰DIY B站](https://space.bilibili.com/437455484) — 组装视频教程

## 💎 致谢

**gsl12** · **Voron Design** · **小辰DIY (pangqc)** · 所有 Tiny-M 贡献者

## 📄 许可证

本项目遵循原仓库的开源许可证。
