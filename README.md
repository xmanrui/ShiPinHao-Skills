# ShiPinHao-Skills：让日更100条更简单
素人起号最好的方法是模仿，我把多个视频号的大博主蒸馏为skill，方便大家写某个博主风格的文案，让日更100条更简单

## Skills 列表

| 博主.skill                                              | 简介                               | 状态    |
|-------------------------------------------------------|----------------------------------|-------|
| <h3>[福饱饱.skill](./fubaobao/README.md)</h3>            | 微信视频号素人妈妈博主，做带货 + 口播 vlog + 素人创作教程 | done  |
| <h3>[俞浩.skill](./yuhao/README.md)</h3>                | 追觅CEO，日更100条                     | doing |
| <h3>[不答哥.skill](./budage/README.md)</h3>              | 大博主，日更100条                       |doing |
| <h3>[刘思毅.skill](./liusiyi/README.md)</h3>             | 群响创始人，日更100条                     |doing |
| <h3>[熬霸马.skill](./aobama/README.md)</h3>              | 素人，日更100条                        |doing |
| <h3>[海涛小同学.skill](./haitaoxiaotongxue/README.md)</h3> | 素人，受熬巴马影响，日更100条                 |doing |
| <h3>[陈昌文.skill](./chenchangwen/README.md)</h3>        | 日更100条                 |doing |
| <h3>[懂十一.skill](./dongshiyi/README.md)</h3>           | 日更100条                 |doing |

## 目录约定
![img.png](doc/img.png)
每个博主文件夹遵循统一结构：

```
<博主名>/
├── README.md                         # 第一行为「<博主中文名>.skill」（H1 居中加粗），用作总目录引用
├── SKILL.md                          # 默认入口：人设 + 工作能力合体（带 frontmatter，可被 Claude Code 识别）
├── work_skill.md                     # 子入口：仅工作方法论
├── persona_skill.md                  # 子入口：仅人物性格
├── work.md                           # work 原始文档（无 frontmatter）
├── persona.md                        # persona 原始文档（无 frontmatter）
├── meta.json                         # skill 元数据
├── manifest.json                     # 安装清单
├── .gitignore
└── knowledge/
    └── research/
        ├── raw/                      # 关键金句索引（带时间戳）
        ├── merged/                   # 6 维度研究（writings/conversations/expression_dna/decisions/external_views/timeline）
        └── reviews/                  # audit / synthesis / validation
```

## 命名约定

- 文件夹名：博主拼音或英文 slug（如 `fubaobao`），全小写，连接符可用 `_` 或 `-`
- README 第一行：`<h1 align="center">博主中文名.skill</h1>`，作为本目录引用的标准来源
- SKILL.md frontmatter 的 `name`：与文件夹名一致（如 `name: fubaobao`）
- 子 skill 命名：`<slug>_work` / `<slug>_persona`

## 添加新博主

1. 在本目录新建 `<slug>/` 文件夹
2. 按上述结构填入文件（SKILL.md / persona.md / work.md / knowledge/）
3. 在本 README 的「Skills 列表」加一行链接
4. 软链到 `~/.claude/skills/<slug>` 即可在 Claude Code 中通过 `/<slug>` 调用



## 联系方式

<table>
  <tr>
    <td align="center"><img src="doc/wechat.png" width="200"/><br/>微信</td>
    <td align="center"><img src="doc/shipinhao.jpg" width="200"/><br/>视频号</td>
    <td align="center"><img src="doc/xhs.png" width="200"/><br/>小红书</td>
  </tr>
</table>

## License

MIT
