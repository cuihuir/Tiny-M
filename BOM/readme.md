# BOM / Bill of Materials

## Directory Structure

```
BOM/
├── readme.md              # This file - directory index
├── BOM.md                 # Our main BOM (English)
├── BOM_cn.md              # Our main BOM (Chinese)
└── reference/             # Reference BOMs from original sources
    ├── DRAFT-BOM-gsl12.md           # gsl12 original draft BOM (English)
    ├── DRAFT-BOM-gsl12_cn.md        # gsl12 original draft BOM (Chinese)
    ├── XiaoChen-DIY-BOM-v2.2.md     # XiaoChen DIY V2.2 complete BOM (English)
    ├── XiaoChen-DIY-BOM-v2.2_cn.md  # XiaoChen DIY V2.2 complete BOM (Chinese)
    └── DRAFT-BOM-Tiny-M.xlsx        # gsl12 original Excel (preserved)
```

## Our Main BOM

- **[BOM.md](BOM.md)** / **[BOM_cn.md](BOM_cn.md)** - Based on XiaoChen DIY V2.2 with personal modifications. This is the active BOM used for the actual build.

## Reference Sources

These are preserved for reference and comparison:

- **gsl12 Original** - [DRAFT-BOM-gsl12.md](reference/DRAFT-BOM-gsl12.md) - The original draft BOM from the Tiny-M creator. Sourced from `DRAFT - BOM - Tiny M.xlsx`.
- **XiaoChen DIY V2.2** - [XiaoChen-DIY-BOM-v2.2.md](reference/XiaoChen-DIY-BOM-v2.2.md) - Complete BOM with detailed per-assembly screw/nut breakdown, extrusion drilling/tapping guide, and assembly jigs. Source: [pangqc/voron-tiny-m](https://gitee.com/pangqc/voron-tiny-m).

## Tools

### JLC Extrusion Model Reorder (`tools/jlc_reorder.py`)

嘉立创铝型材加工代码排序工具。手工填写型号时加工代码顺序可能不符合嘉立创要求，此工具将 TXCJ 型号中的加工代码重排为嘉立创标准顺序。

**支持的加工代码（按嘉立创标准顺序）：**

| 序号 | 代码 | 含义 |
|------|------|------|
| 1 | SC | 铣端面 |
| 2 | LA / RA / DA | 左端/右端/两端攻牙 |
| 3 | LU/RU/LD/RD/LF/RF/LB/RB | 45°斜切 |
| 4 | LH/RH/LDH/RDH/LG/RG/LDG/RDG | 盲孔 |
| 5 | LC / RC | 左端/右端水平沉头孔 |
| 6 | LE / RE | 左端/右端垂直沉头孔 |
| 7 | LBC / RBC | 背面水平沉头 |
| 8 | LBE / RBE | 背面垂直沉头 |
| 9 | LK / RK | 水平扳手孔 |
| 10 | LM / RM | 垂直扳手孔 |

**Excel 模式（直接转换嘉立创 BOM 模板）：**

```bash
# 读取 xlsx，转换 JLC型号 列，输出新文件
python3 tools/jlc_reorder.py -x 嘉立创FA模板.xlsx -o 嘉立创FA输出.xlsx

# 不指定 -o 则自动命名为 原文件名_jlc.xlsx
python3 tools/jlc_reorder.py -x 嘉立创FA模板.xlsx

# 指定目标列名（默认匹配 "JLC型号"）
python3 tools/jlc_reorder.py -x 嘉立创FA模板.xlsx -c "我的型号"
```

**命令行 / 管道模式：**

```bash
# 单个型号
python3 tools/jlc_reorder.py "TXCJ-H7-2020D-L300-LC-Z5-A10-RC-Z5-A60-DA-SC"
# output: TXCJ-H7-2020D-L300-SC-DA-LC-Z5-A10-RC-Z5-A60

# 批量管道
cat models.txt | python3 tools/jlc_reorder.py

# 交互模式（Ctrl+D 退出）
python3 tools/jlc_reorder.py
```

**示例：**

```
input:  TXCJ-H7-2020D-L260-LC-Z5-A36-DA-SC
output: TXCJ-H7-2020D-L260-SC-DA-LC-Z5-A36

input:  TXCJ-H7-2020D-L130-DA-SC-LC-Z5-A40-RC-Z5-A40
output: TXCJ-H7-2020D-L130-SC-DA-LC-Z5-A40-RC-Z5-A40
```
