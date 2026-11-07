<div align="center">

# 明日方舟 · 干员角色卡

**QQ 交流群：1131116861。**欢迎访问角色卡分享站点 **[RoleHomes](https://role.homes/)**，一起分享和交流角色卡。

适用于 [MaiBot](https://github.com/Mai-with-u/MaiBot)、[AstrBot](https://github.com/AstrBotDevs/AstrBot) 和 [qq-bridge](https://github.com/Derpyu520/qq-bridge) 的明日方舟干员角色卡

[![适用于 MaiBot](https://img.shields.io/badge/%E9%80%82%E7%94%A8%E4%BA%8E-MaiBot-8fd6a0)](https://github.com/Mai-with-u/MaiBot)
[![适用于 AstrBot](https://img.shields.io/badge/%E9%80%82%E7%94%A8%E4%BA%8E-AstrBot-76bad9)](https://github.com/AstrBotDevs/AstrBot)
[![适用于 qq-bridge](https://img.shields.io/badge/%E9%80%82%E7%94%A8%E4%BA%8E-qq--bridge-blue)](https://github.com/Derpyu520/qq-bridge)
![分析模型 Claude Opus 5.5 · max](https://img.shields.io/badge/%E5%88%86%E6%9E%90%E6%A8%A1%E5%9E%8B-Claude%20Opus%205.5%20%C2%B7%20max-d97757)
![剧情范围 明日方舟（不含终末地）](https://img.shields.io/badge/%E5%89%A7%E6%83%85%E8%8C%83%E5%9B%B4-%E6%98%8E%E6%97%A5%E6%96%B9%E8%88%9F%EF%BC%88%E4%B8%8D%E5%90%AB%E7%BB%88%E6%9C%AB%E5%9C%B0%EF%BC%89-333333)

</div>

> 博士，干员们已经在群里等你了。

将对应框架的角色卡导入 MaiBot、AstrBot 或 qq-bridge，QQ 群里的 AI 就会以对应干员的身份和大家聊天。每位干员在三种框架下都提供**精简版**和**完整版**，按需选用。

## 关于角色卡

- **人设来源**：干员的性格、爱好、特点等人物设定，均由 AI 分析《明日方舟》剧情得到。
- **外貌认知**：结合干员立绘图片分析外貌特征，让角色了解自己的发色、服饰等细节，描述自身形象时更贴合原作。
- **制作工具**：使用 Claude Code 辅助阅读剧情与干员资料，梳理人物设定、记忆和人物关系，并编写精简版与完整版角色卡。
- **分析模型**：Anthropic Claude Opus 5.5，推理强度 max。
- **记忆范围**：干员的记忆目前仅限《明日方舟》游戏内的内容，**暂不包含**约 500 年后发生在塔卫二的《明日方舟：终末地》（如再旅者等）。

AI 的理解难免有偏差或遗漏，与官方设定冲突时请以游戏为准。觉得哪位干员 OOC 了，欢迎[反馈](#交流与反馈)。

## 精简版与完整版

本仓库为每位干员、每种框架同时提供两个版本：

| 版本 | 包含内容 | 使用建议 |
| --- | --- | --- |
| **精简版** | 性格、爱好、特点等人物设定 | 上下文开销较小，适合日常群聊 |
| **完整版** | 在精简版基础上，额外加入干员记忆、人物关系等 | 设定更丰富，上下文开销也更高；qq-bridge 需[调高注入上限](#qq-bridge) |

不确定选哪个时，可以先用精简版；想让干员记得过往经历和身边的人，再换成完整版。

## 收录干员

角色卡按 `<干员名>/<框架名>/` 分类存放。精简版文件名带 `-精简`，完整版使用干员名；MaiBot 和 AstrBot 使用 `.json`，qq-bridge 使用 `.md`。请下载自己所用框架对应的文件。

| 干员 | MaiBot（JSON） | AstrBot（JSON） | qq-bridge（Markdown） | 语音模型 |
| --- | --- | --- | --- | --- |
| [黍](黍/README.md) | [精简版](黍/MaiBot/黍-精简.json) · [完整版](黍/MaiBot/黍.json) | [精简版](黍/AstrBot/黍-精简.json) · [完整版](黍/AstrBot/黍.json) | [精简版](黍/qq-bridge/黍-精简.md) · [完整版](黍/qq-bridge/黍.md) | [Hugging Face](https://huggingface.co/hualuoo/Arknights-Roles/tree/main/%E9%BB%8D) |
| 焰影苇草 | [精简版](焰影苇草/MaiBot/焰影苇草-精简.json) · [完整版](焰影苇草/MaiBot/焰影苇草.json) | [精简版](焰影苇草/AstrBot/焰影苇草-精简.json) · [完整版](焰影苇草/AstrBot/焰影苇草.json) | [精简版](焰影苇草/qq-bridge/焰影苇草-精简.md) · [完整版](焰影苇草/qq-bridge/焰影苇草.md) | — |

持续更新中，以仓库中的文件为准。

## 语音模型

黍的 **GPT-SoVITS 语音模型**已在 [Hugging Face](https://huggingface.co/hualuoo/Arknights-Roles/tree/main/%E9%BB%8D) 开源，提供**通用模型**及**中立、吃惊、开心、生气、难过**五种情绪模型。每个版本都包含配套的 GPT（`.ckpt`）和 SoVITS（`.pth`）权重。

下载链接、权重配对与使用方法见[黍的说明](黍/README.md#语音模型)。

## 使用方法

开始前，请先部署好所用的机器人框架，并确认能正常对话，再按对应小节导入角色卡。

### MaiBot

部署方法见 [MaiBot 文档](https://docs.mai-mai.org/manual/)，角色卡导入流程见官方[人设导入说明](https://github.com/Mai-with-u/MaiBot/blob/main/docs/personality-import.md)。

1. **选择角色卡**：下载 `<干员名>/MaiBot/` 中所需版本的 `.json` 文件，打开并复制完整内容。
2. **导入并保存**：进入 MaiBot WebUI 的机器人配置页，点击「导入」并粘贴 JSON。确认预览后点击「继续编辑」，再点击「创建人设」保存。
3. **切换角色**：在 WebUI 的人设库中选择并启用刚导入的角色。导入只会新增人设，不会自动切换当前使用的角色。

### AstrBot

部署与配置方法见 [AstrBot 文档](https://docs.astrbot.app/)。

1. **选择角色卡**：下载 `<干员名>/AstrBot/` 中所需版本的 `.json` 文件。
2. **导入文件**：进入 AstrBot WebUI 的角色管理页面，通过导入功能选择该 JSON 文件，导入角色设定及预设对话。
3. **选用角色**：在需要使用的会话或配置中选择导入的角色，工具与技能按需另行设置。

### qq-bridge

部署方法见 [qq-bridge 安装指南](https://github.com/Derpyu520/qq-bridge/blob/main/docs/guides/DSH_SETUP.md)。qq-bridge 版精简卡不超过 8000 字符，完整版约 16000 字符。

1. **放入角色卡**：下载 `<干员名>/qq-bridge/` 中所需版本的 `.md` 文件，直接放进 qq-bridge 的 `roles/` 目录。qq-bridge 不读取 `roles/` 下的子文件夹，所以不要把整个文件夹放进去；角色名以实际放入的文件名为准。
2. **使用完整版时，调高注入上限**：qq-bridge 默认单次最多注入 8000 字符，完整版放进去只有前 8000 字符生效。请在控制台的角色设置中把「注入上限（字符）」调到 16000 以上，建议直接设为最大值 20000，下一条消息即生效。也可以改 `config.json` 中的 `role.maxInjectChars`，但需要重启 qq-bridge。使用精简版可跳过这一步。
3. **切换角色**，两种方式任选：
   - 在 qq-bridge 本地控制台（默认 `http://127.0.0.1:3100`）的角色设置中选择干员；
   - 由管理员在白名单会话中发送命令（普通群友发送无效）：

     ```text
     /role <角色名>
     /role off
     ```

     前者切换为该干员，后者退出角色扮演。**文件名去掉 `.md` 就是角色名**，例如 `黍.md` 对应 `/role 黍`，`黍-精简.md` 对应 `/role 黍-精简`。
4. **无需重启**：切换角色或修改卡片内容后，下一次唤醒即生效。

> [!WARNING]
> 只复制干员角色卡，**不要**把根目录或干员目录中的 `README.md` 放进 `roles/`。它会覆盖 qq-bridge 自带的 `roles/README.md`，而且 `README` 不能作为角色名。
> qq-bridge 本身的部署与运行问题，请前往 [qq-bridge Issues](https://github.com/Derpyu520/qq-bridge/issues)。

> [!TIP]
> 完整版每次完整注入约 16000 字符，上下文开销明显高于精简版（qq-bridge 估算 8000 字符约合 6～8k token，实际取决于模型）。如果控制台提示「超出注入上限」，说明上限还没调够。想自己修改卡片，可以参考 qq-bridge 的[角色卡写作规范](https://github.com/Derpyu520/qq-bridge/blob/main/roles/README.md)。

## 声明

- 本项目为玩家自制的非官方同人项目，与上海鹰角网络科技有限公司、MaiBot、AstrBot、qq-bridge 项目均无隶属关系。
- 《明日方舟》及其角色、剧情、名称等相关版权归上海鹰角网络科技有限公司所有。
- 角色卡仅供交流与娱乐，请勿用于商业用途。如有侵权，请联系删除。

## 交流与反馈

欢迎在本仓库的 **Issues** 中留言，例如：

- 干员 OOC、剧情理解有误；
- 想看的干员（许愿）；
- 使用中遇到的问题。

## 致谢

- **[鹰角网络（Hypergryph）](https://www.hypergryph.com/)**：感谢《[明日方舟](https://ak.hypergryph.com/)》官方创造了泰拉世界与这些令人难忘的干员。
- **[MaiBot](https://github.com/Mai-with-u/MaiBot)**：提供人设配置与自然群聊能力。
- **[AstrBot](https://github.com/AstrBotDevs/AstrBot)**：提供角色管理与多平台聊天支持。
- **[qq-bridge](https://github.com/Derpyu520/qq-bridge)**：让干员们得以走进 QQ 群。
- **[PRTS Wiki](https://prts.wiki/)**：玩家共同构筑的明日方舟中文 Wiki，整理了详实的剧情与干员资料。

<p align="center">
  <a href="images/claude.png">
    <img src="images/claude.png" alt="使用 Claude Code 分析明日方舟剧情的过程截图" width="960">
  </a>
</p>
