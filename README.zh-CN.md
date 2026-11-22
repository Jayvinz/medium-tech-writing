# medium-tech-writing

<img src="assets/medium-tech-writing-icon-512.png" width="96" alt="medium-tech-writing icon">

一个给 AI Agent 用的技能包，按成熟英文技术出版物的风格产出 Medium 级别的技术长文。
写作规范提炼自大量真实文章的量化分析，自带一道"去 AI 味"质检，让产出读起来像人写的，
而不是模型生成的。

English version: [README.md](README.md).

## 你能得到什么

一个技能，覆盖七类文体：教程、清单文（Pro-tips）、概念讲解、迁移指南、案例分析、
版本公告、系列总结。每一类都有对应的章节骨架、标题公式、开篇写法、代码呈现规则、
收尾动作，以及一份发布前检查清单。清单里的每条规范背后都有语料统计数据支撑。

去 AI 味不是事后补救，而是工作流的一部分。它清除生成文风的典型痕迹：
"不是 X 而是 Y"式对比句、铺垫式排演、单句戏剧化收尾、凑数三连排比、破折号通病、
夸张意义、AI 高频词、装饰性加粗。当去味规则与出版物惯例冲突时，以出版物惯例为准，
所以 **Note** 提示框、bookend 式收尾这些刊物惯例能安全保留。

## 安装

### 给 AI Agent 的一键安装语句

复制下面这段话，粘贴给你的 AI Agent（任何能克隆仓库、复制文件的 Agent 都适用）。
这段话与具体 Agent 无关：

> 请帮我安装 medium-tech-writing 技能：克隆仓库
> https://github.com/Jayvinz/medium-tech-writing ，把其中的 `skills/medium-tech-writing/`
> 目录整个复制到本 Agent 加载用户级 `SKILL.md` 技能的目录（父目录不存在就创建）。
> 完成后确认安装路径下 SKILL.md 存在，并把路径告诉我。

### 手动安装

```bash
git clone https://github.com/Jayvinz/medium-tech-writing.git
cp -r medium-tech-writing/skills/medium-tech-writing <你的Agent技能目录>/
```

Windows（PowerShell）：

```powershell
git clone https://github.com/Jayvinz/medium-tech-writing.git
Copy-Item -Recurse medium-tech-writing\skills\medium-tech-writing <你的Agent技能目录>\
```

`<你的Agent技能目录>` 是你的 Agent 扫描 `SKILL.md` 格式技能的文件夹。不确定的话，
直接问它："你从哪个目录加载技能？"

安装位置选择：

| 范围 | 位置 | 适用场景 |
|---|---|---|
| 用户级 | Agent 的用户级技能目录 | 默认；所有项目可用 |
| 项目级 | 工作区的项目级技能目录 | 随仓库共享给团队 |

### 验证安装

对你的 Agent 说一句：

> 用 medium-tech-writing 给"Gradle 配置缓存"出一个教程大纲。

如果技能接上了，它会先报文体选择、给出章节大纲，然后才开始写正文。
直接说"用 Medium 风格写一篇关于 X 的文章"也能触发（触发词在技能描述里）。

## 上手使用

四个典型用法，可以混着来。

**1. 从一个主题直接写。**

> 用 medium-tech-writing 写一篇教程：Android View 迁移到 Jetpack Compose。
> 读者是中级 Android 开发。

技能会选定文体（迁移指南）、加载骨架、先出标题和开篇，再逐节成文。
默认输出英文；要中文直接说。

**2. 把已有草稿改写成 Medium 风格。**

> 这是我的草稿（见下）。用 medium-tech-writing 改写成一篇 Medium 教程。

结构、标题、节奏会按出版物规范重排。事实仍以你的为准：技能不会编造 benchmark、
版本号或 API 名，缺的地方留 `[TODO: verify]` 标记。

**3. 给现成的稿子去 AI 味。**

> 对这份草稿跑一遍 medium-tech-writing 的去 AI 味质检，不要动结构。

内容没问题但文风像机器生成时用这个。质检完会汇报改了什么。

**4. 对照检查清单审稿。**

> 用 medium-tech-writing 的发布前检查清单审一下这篇文章。

返回具体缺口：篇幅对照文体中位数、标题层级形态、代码与讲解比例、缺不缺 Note 提示、
收尾动作强弱、有没有漏网的 AI 腔。

## 技能怎么工作

七步流程，每步按需加载对应的参考文件：

1. 确定文体（教程 / 清单 / 讲解 / 迁移 / 案例 / 公告 / 总结）。
2. 加载对应骨架，先出 H3 大纲再动笔。
3. 用语料公式起草标题和开篇，开篇末尾给出明确的阅读承诺句。
4. 逐节成文，套用出版物语气：短段落、"我们/你/Let's"、预判读者疑问、
   代码块配走读讲解、**Note** 提示、诚实的范围声明。
5. 收尾用 2–3 个收尾动作：bookend 重申建议、下一步 CTA、致谢审稿人、可选签名档。
6. 对照发布前检查清单过稿，补齐缺口。
7. 跑去 AI 味质检，并确认它没有误伤刊物惯例。

技能内的参考文件：

| 文件 | 内容 |
|---|---|
| `references/article-templates.md` | 七类文体骨架 |
| `references/titles-and-hooks.md` | 标题公式与开篇模式 |
| `references/writing-voice.md` | 语气、代码呈现、配图规范 |
| `references/corpus-stats.md` | 量化规范与发布前检查清单 |
| `references/de-ai-flavor.md` | 去味规则、保留清单与质检流程 |

## 仓库结构

```
medium-tech-writing/
├── README.md                 ← 英文说明
├── README.zh-CN.md           ← 中文说明（本文件）
├── LICENSE                   ← MIT
└── skills/
    └── medium-tech-writing/  ← 可安装的技能本体
        ├── SKILL.md
        └── references/
            ├── article-templates.md
            ├── titles-and-hooks.md
            ├── writing-voice.md
            ├── corpus-stats.md
            └── de-ai-flavor.md
```

`skills/` 布局沿用多技能仓库的通行惯例，之后想加伴生技能不用改安装脚本。

## 环境要求

- 一个能加载 `SKILL.md` 格式技能、并按需读取 `references/` 文件的 AI Agent。
- 无运行时依赖，技能本体就是指令和参考资料。

**Note**：写作规范面向 Medium 的英文技术出版物。技能可按要求切换输出语言，
去味质检同样适用于中文稿，但文体骨架和标题公式的统计口径来自英文文章。

## Release 构建

推送 `v*` 标签会触发 CI：校验 SKILL.md frontmatter、比对标签与 `version` 字段，
然后把技能打成 SkillHub 可上传的 zip（第一层为技能目录），挂到 GitHub Release。

```bash
git tag v1.0.0
git push origin v1.0.0
```

## 许可证

MIT，见 [LICENSE](LICENSE)。
