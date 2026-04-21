**[English](README.md)**

# Tiny-M

一款基于 [Voron V0](https://github.com/VoronDesign/Voron-0) 的紧凑型 CoreXY 3D 打印机，成型体积 150x150x150mm。

<img src="images/tiny-m_v4.jpg" width="400">

> **致敬原作者 gsl12**
>
> Tiny-M 由 gsl12 设计并在开源社区发布，作者在 Voron V0 基础上做了大量优化改进。遗憾的是，2023 年 8 月作者因健康原因停止了项目维护，V5 版本永久停留在了 beta 阶段。
>
> 本仓库 fork 自 [gsl12/Tiny-M](https://github.com/gsl12/Tiny-M)，旨在延续原作的开源精神，继续维护和改进这个优秀的打印机项目。

## 复刻进度

| 阶段 | 状态 | 说明 |
|------|------|------|
| BOM 与采购 | **进行中** | 型材框架 BOM 已完成，嘉立创已下单 |
| 框架组装 | 待开始 | 等待型材到货 |
| 运动系统 | 待开始 | 导轨、电机、同步带 |
| 热端与挤出 | 待开始 | |
| 热床 | 待开始 | |
| 电气 | 待开始 | |
| 封箱 | 待开始 | |
| 软件配置 | 待开始 | Klipper 调试 |

<details>
<summary><strong>最近更新</strong></summary>

- **BOM 重构** - 将 gsl12 原版和小辰DIY V2.2 的 BOM 转为中英双语 Markdown，建立了自己的活跃 BOM
- **框架型材已下单** - 19 根 2020 铝型材通过嘉立创（TXCJ）定制加工，含打孔攻丝。详见 [BOM-Frame-JLCFA](BOM/BOM-Frame-JLCFA.md)
- **嘉立创工具** - 创建 `tools/jlc_reorder.py`，自动将铝型材加工代码重排为嘉立创标准顺序
- **双语文档** - 所有文档均有英文版（`*.md`）和中文版（`*_cn.md`）

</details>

## 项目引用

| 项目 | 说明 |
|------|------|
| [gsl12/Tiny-M](https://github.com/gsl12/Tiny-M) | 原作者仓库，当前版本 V4 |
| [gsl12/Tiny-M-V5-beta](https://github.com/gsl12/Tiny-M-V5-beta) | V5 beta 版（未完成） |
| [pangqc/voron-tiny-m](https://gitee.com/pangqc/voron-tiny-m) | 小辰DIY 修改版，包含完整 BOM、封箱方案及组装教程 |

## 关于本项目

这是一个复刻维护项目，目标包括：

- 整理和更新 BOM（物料清单），方便国内采购
- 参考小辰DIY的修改方案（光电限位、封箱、近程挤出等），结合实际复刻经验进行优化
- 补充和完善组装文档
- 持续更新个人复刻过程中的改进方案

## 硬件规格

- 成型体积：150 x 150 x 150 mm
- 运动系统：CoreXY
- 框架：2020 铝型材
- X 轴导轨：1x 200mm MGN12H
- Y 轴导轨：2x 200mm MGN9H
- Z 轴导轨：2x 200mm MGN12H
- 电机：NEMA 17 步进电机
- 供电：24V
- 固件：Klipper

## 挤出机选项

支持 Bowden 和直接驱动方案：

- [CroXY Sailfin](https://github.com/CroXY3D/Sailfin-Extruder) - 直接驱动
- [Annex Engineering Sherpa Mini](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder) - 直接驱动
- [Bondtech LGX Lite](https://www.bondtech.se/product/lgx-lite-extruder-custom/) - 直接驱动
- E3D V6 远程热端 - Bowden 方案

## 控制板

- FYSETC Cheetah V1.1b (TMC2209)
- SKR Mini E3 + TMC2209
- MKS Robin E3D（小辰DIY 修改版方案）

## 目录结构

```
├── BOM/              # 物料清单
├── CAD/              # CAD 源文件
├── DXFs/             # 加工图纸
├── STLs/             # 打印件 STL 文件
├── images/           # 图片
├── klipper_firmware/ # Klipper 固件配置
├── slicer/           # 切片软件配置
└── usermods/         # 用户修改方案
```

## 打印建议

推荐使用 ABS 或 ABS+ 耗材打印结构件：

- 喷嘴：0.4mm
- 挤出宽度：0.48mm
- 层高：0.2 - 0.3mm
- 顶/底层：5 层
- 墙壁：4 圈
- 填充：40%（推荐三角形填充）

裙边件可使用其他耗材类型打印。

## XY 接头版本说明

共有 3 个版本的 XY 接头，推荐使用 V4：

- **V2** - 使用 2GT 20T 同步轮（无定位螺丝法兰），需要打磨法兰以适配
- **V3** - 使用 2GT 20T 齿形惰轮，无 M5 螺母
- **V4** - 拆分为 3 个部件，移除一颗 M5 螺钉以改善对齐，优化皮带路径，刚性更好

## 用户修改方案

详见 [usermods](https://github.com/gsl12/Tiny-M/tree/master/usermods) 目录，包括：

- 皮带 Z 轴方案 (Belted Z Mod)
- 190mm Prusa Mini 热床方案
- 全金属热床底座
- 5mm 肩螺丝方案
- 5mm 定位销方案
- 后部走线槽
- 顶盖方案 (Tophat)

## 社区

- [CroXY Discord](https://discord.gg/tmZkjWs) - Tiny-M 频道
- [Mark Hoy's Build Log](https://github.com/mark-hoy/tiny-m-build)
- [小辰DIY B站频道](https://space.bilibili.com/437455484) - 组装视频教程

## 致谢

- **gsl12** - Tiny-M 原作者，设计了这台优秀的紧凑型打印机
- **Voron Design** - Voron V0 原始设计
- **小辰DIY (pangqc)** - 完善了 BOM、封箱方案、组装教程等中文资料
- 所有 Tiny-M 社区的贡献者

## 许可证

本项目遵循原仓库的开源许可证。
