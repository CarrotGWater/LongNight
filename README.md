# 长夜 (LongNight)

> 太阳渐渐熄灭，现在要面对的，将是无尽的长夜……

**开发中项目，敬请期待。**

## 项目结构
```
longnight/
├── packages/                             # 所有内容包存放处
│   └── CarrotS/                          # 核心内容包
│       ├── manifest.json                 # ★ 包入口，声明路径与元数据
│       ├── dependences.json              # 依赖声明（默认为空）
│       ├── blocks/                       # 方块定义（每方块单文件）
│       │   ├── default.json              #   默认模板
│       │   ├── air.json                  #   空气
│       │   ├── grass.json                #   草方块
│       │   ├── stone.json                #   石头
│       │   └── water.json                #   水
│       ├── items.json                    # 物品定义（未来扩展）
│       ├── entities/                     # 实体定义（生物、掉落物等）
│       │   ├── animals/                  #   动物实体
│       │   └── monsters/                 #   怪物实体
│       ├── structures/                   # 结构模板（村庄、树木、地牢等）
│       ├── generation_rules/             # 生成规则（结构、矿物、生物群系）
│       ├── behaviors/                    # 行为脚本（AI、特殊逻辑）
│       ├── textures/                     # 方块/物品/实体纹理
│       ├── sounds/                       # 音效文件
│       └── lang/                         # 多语言翻译文件
├── saves/                                # 世界存档目录
│   └── MyWorld/                          # 默认世界
├── config.json                           # 全局游戏设置（语言、包加载顺序等）
├── README.md                             # 本文件
├── LICENSE                               # 开源协议
└── longnight.exe                         # 主程序（编译产物）
```

> **Wiki 数据流**: `packages/CarrotS/blocks/*.json` (游戏数据) 通过 `wiki/generate_blocks_data.py` 解析，合并 `wiki/blocks-meta.json` (展示元数据)，自动生成 `wiki/blocks-data.js` 供前端使用。新增方块只需建 JSON + 加元数据 + 运行脚本即可同步。

在这个世界中，你需要保护自己庇护所的微光，在漫漫长夜中生存下去……