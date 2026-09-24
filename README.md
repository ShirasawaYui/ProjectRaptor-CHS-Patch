# Project Raptor: War Commanders 9.1.27 简体中文汉化补丁

适用 MOD：**Project Raptor: War Commanders 9.1.27**（含 ENG Voice 版）
汉化内容：**8650 条游戏文本**（菜单 / 阵营 / 单位 / 将军档案 / 技能提示 / 任务脚本）+ 微软雅黑字体配置
制作：梅莉 🔮（术语表以 EA 官方繁体中文为基底转简体，MOD 新增内容人工翻译），2026-09-24

---

## 一、先搞清楚：你的 MOD 装在哪？

补丁的覆盖目标只有一个——**你现有 9.1.27 MOD 的 `Data\English` 文件夹**，
特征是里面有 `generals.csf`、`Версия.csf` 等 6 个文件。

按你的安装方式对号入座：

- **用 GenLauncher 管理的**：MOD 在 GenLauncher 的 mods 目录下的
  `Generals Project Raptor War Commanders\9.1.27\` 里（默认是 `<游戏根目录>\GLM\`，
  如果你自定义过安装路径，以 GenLauncher 设置里显示的实际路径为准——它不一定在游戏根目录）。
- **没用 GenLauncher、手动解压覆盖原版的**：MOD 就是你解压出来的那个文件夹，
  里面直接能看到 `Data` 和 `generals.exe`，位置随你放。

## 二、前置条件

1. 已安装好 9.1.27，且**英文原版能正常进入游戏**。
2. Windows 10 / 11（系统自带「微软雅黑」字体，无需另装）。
3. **仅 GenLauncher 用户**：设置中已开启 **Install and autoupdate gentool**。
   此项必须开启——9.1.27 的新引擎依赖 GenTool 才能启动，不开会「无报错但不进游戏」。

## 三、安装步骤

### 方式 A：GenLauncher 用户

1. 打开补丁包里的 `方式A_GenLauncher用户` 文件夹，把其中的
   **`Generals Project Raptor War Commanders`** 整个文件夹复制到你的
   **GenLauncher mods 目录**（即现有 `Generals Project Raptor War Commanders`
   文件夹所在的位置，参考第一节）。
   系统提示「合并文件夹 / 替换目标中的文件」时，选 **是 / 全部替换**。
2. 打开 GenLauncher → 设置 → 勾选 **Install and autoupdate gentool**。
3. 在 MOD 的**启动器 / 可执行文件下拉框**中选择 **Project Raptor 9.1.27 Engine**
   （不要用默认的 generals.exe 启动），启动游戏，看到中文主菜单即成功。

> 补丁已附带 Executables 引擎挂载文件。如果重装 MOD 后启动报
> 「launcher will be skipped」之类错误，重新执行一次第 1 步即可修复。

### 方式 B：手动覆盖用户（无 GenLauncher）

1. 打开补丁包里的 `方式B_手动覆盖用户` 文件夹，把其中的 **`Data`**
   文件夹复制到你的 9.1.27 MOD 根目录（就是有 `Data`、`generals.exe` 的那层），
   与现有 `Data` 合并，提示替换时选 **是 / 全部替换**。
2. 按你平时的方式启动 MOD（MOD 自带启动器或直接运行 generals.exe），看到中文主菜单即成功。

## 四、恢复英文原版

把补丁包里 `恢复英文原版\Data\English\` 中的全部文件复制到你的
`Data\English`（就是你第二步覆盖过的那个位置）覆盖，即可还原英文出厂状态。

## 五、常见问题

**Q：点了启动没报错，但就是不进游戏、Steam 也不显示运行中？**（GenLauncher 用户）
A：九成是 **gentool 没开**。去 GenLauncher 设置里勾选 Install and autoupdate gentool
再启动。9.1.27 引擎必须依赖 GenTool，本体和 9.1.25 无此要求。

**Q：启动时 GenLauncher 弹「跳过启动器 / launcher will be skipped」之类的报错？**
A：`Executables\Project Raptor 9.1.27 Engine\9.1.27\generals.exe` 缺失了
（重装 MOD 会清掉它）。重新按方式 A 第 1 步复制一遍即可。

**Q：文字显示成方块 / 乱码？**
A：确认系统装有微软雅黑（Windows 10/11 默认自带）；不要改动 `Language.ini` 里的字体名。

**Q：切换 Steam 语言会影响汉化吗？**
A：**强烈建议游玩此 MOD 期间，将 Steam 游戏库中 Zero Hour（绝命时刻）的「游戏语言选项」保持为英文，不要切换任何其他语言选项！（注意：是游戏属性里的语言选项，不是 Steam 客户端的界面语言）**
实测切换 Zero Hour 的游戏语言不仅会重写游戏文本、破坏汉化文件（可能与 GenLauncher 镜像穿透），
还会影响游戏的美术资源载入——部分图片会直接缺失，显示为紫色色块。
若已经切过语言导致异常：切回英文让 Steam 完整校验一次，再重新复制一遍补丁文件即可。

**Q：个别文本想改？**
A：CSF 为取反态存储（引擎加载时逐字符取反），直接改二进制会坏，需用专用工具重编译。

---

## 补丁包内容清单

```
├── README.md                        ← 本文件
├── 方式A_GenLauncher用户\
│   └── Generals Project Raptor War Commanders\
│       ├── 9.1.27\Data\English\     ← 6 个中文 CSF + Language.ini + HeaderTemplate.ini
│       └── Executables\Project Raptor 9.1.27 Engine\9.1.27\generals.exe
├── 方式B_手动覆盖用户\
│   └── Data\English\                ← 6 个中文 CSF + Language.ini + HeaderTemplate.ini
└── 恢复英文原版\
    └── Data\English\                ← 8 个原版文件（通用还原）
```

*汉化基于 9.1.27 原始分发版制作，全部文本 8650 条：EA 官方繁中灌底（繁转简校订）+ MOD 新增内容人工翻译。转载请保留本说明。*
