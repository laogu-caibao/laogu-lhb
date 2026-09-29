# 龙虎榜夜报

`laogu-lhb`

龙虎榜夜报 skill：每日收盘后（18:00 后）复盘当日 A 股龙虎榜，输出中文夜报。

## 一键安装

```bash
npx skills add laogu-caibao/laogu-lhb
```

仓库地址（点击复制）：

`https://github.com/laogu-caibao/laogu-lhb`

**方式一：克隆**

```bash
git clone https://github.com/laogu-caibao/laogu-lhb.git
```

**方式二：下载 ZIP**

https://github.com/laogu-caibao/laogu-lhb/archive/refs/heads/main.zip

**导入使用**

- Claude Code / Muse：把仓库中的 `SKILL.md` 放到 `~/.claude/skills/laogu-lhb/` 下即可调用。
- 豆包智能体 / Workbuddy 等：按各平台的 skill 上传流程导入 `SKILL.md`。
- 扣子 Coze：扣子编程 → 技能面板 → 创建技能 → 本地上传，上传本仓库打包的 zip（仓库根目录已有 SKILL.md，直接压缩仓库文件夹即可）；如页面要求 `.skill` 后缀，由扣子导入后自动生成，不要只改扩展名。
- Trae：设置 → 技能 → 上传技能，上传同上 zip；或手动放到 `~/.trae/skills/laogu-lhb/`（项目级用 `.trae/skills/laogu-lhb/`）。Trae 也支持 MCP：把 `uvx laogu-mcp` 配进 MCP 设置即可获得 16 个工具（skill 负责流程指导、MCP 负责工具调用）。
- 一次装好全部 16 个：用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)，`uvx laogu-mcp` 一键安装。
## 文件结构

- `SKILL.md` — 主流程（平台中立，定时能力由宿主平台提供）
- `references/sources.md` — 数据源：东财龙虎榜接口、关键字段口径、接口局限

## 输出结构

- 当日上榜总览：家数、净买入/净卖出家数、机构席位家数
- 净买入 Top5：代码、简称、涨跌幅、净买额、上榜原因、席位标签
- 净卖出 Top5：同上
- 席位结构一句话：机构席位占比、游资活跃度（只陈述事实）

## 定时建议

- A 股交易日 18:00 后推送（龙虎榜数据于盘后披露）
- 可与 `laogu-moneyflow` 联动，交叉验证资金流向

---
## 出品

**老谷拆财报** —— 以数据为刃，剖市场真相

- 抖音 / 微信视频号 / 今日头条 / 快手：搜索「老谷拆财报」
- 固定栏目：「价值投资之财报解读」（全网连载中）
- 本 skill 的方法论与账号内容同源：数据驱动、拆开看、不讲黑话

### 扫码关注

| 微信视频号 | 抖音 |
|---|---|
| ![视频号二维码](docs/qrcode-shipinhao.jpg) | ![抖音二维码](docs/qrcode-douyin.png) |
| 扫一扫，关注视频号 | 抖音号：gubaobao22 |

> 作者声明：个人观点，仅供参考，不构成投资建议。
