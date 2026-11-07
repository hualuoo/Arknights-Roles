# 黍 · 角色卡与语音模型

[返回项目首页](../README.md)

本目录提供《明日方舟》干员**黍**适用于 **MaiBot、AstrBot、qq-bridge** 的精简版与完整版角色卡，配套的 **GPT-SoVITS 语音模型**已在 [Hugging Face](https://huggingface.co/hualuoo/Arknights-Roles/tree/main/%E9%BB%8D) 开源。

## 角色卡

| 框架 | 精简版 | 完整版 |
| --- | --- | --- |
| MaiBot | [黍-精简.json](MaiBot/黍-精简.json) | [黍.json](MaiBot/黍.json) |
| AstrBot | [黍-精简.json](AstrBot/黍-精简.json) | [黍.json](AstrBot/黍.json) |
| qq-bridge | [黍-精简.md](qq-bridge/黍-精简.md) | [黍.md](qq-bridge/黍.md) |

MaiBot 使用 JSON 内容粘贴导入，AstrBot 使用 JSON 文件导入，qq-bridge 则将 Markdown 文件放入 `roles/` 目录。具体导入与角色切换方法见[项目使用说明](../README.md#使用方法)。

使用 qq-bridge 时，精简版角色名为 `黍-精简`，默认注入上限即可使用；完整版角色名为 `黍`，需[调高角色注入上限](../README.md#qq-bridge)。

## 语音模型

模型基于 **GPT-SoVITS v5turbo** 微调，使用前需准备以下底模：

- **GPT 底模**：`s1v3.ckpt`。
- **SoVITS 底模**：`s2Gv5turbo.pth`，角色权重采用 **LoRA rank 32**，推理时需配合该底模加载。

模型提供**通用模型**以及**中立、吃惊、开心、生气、难过**五种情绪模型。权重托管于 [Hugging Face 的黍目录](https://huggingface.co/hualuoo/Arknights-Roles/tree/main/%E9%BB%8D)：

- GPT 权重：`GPT_weights_v5turbo/` 中的 `.ckpt` 文件。
- SoVITS 权重：`SoVITS_weights_v5turbo/` 中的 `.pth` 文件。

使用时按下表选择**同一行的两份权重**。文件名无情绪后缀的 `黍.ckpt` 与 `黍.pth` 是通用模型；**“中立”是单独的情绪版本**。

| 模型 | GPT 权重（`.ckpt`） | SoVITS 权重（`.pth`） |
| --- | --- | --- |
| 通用（无情绪后缀） | [黍.ckpt](https://huggingface.co/hualuoo/Arknights-Roles/resolve/main/黍/GPT_weights_v5turbo/黍.ckpt?download=true) | [黍.pth](https://huggingface.co/hualuoo/Arknights-Roles/resolve/main/黍/SoVITS_weights_v5turbo/黍.pth?download=true) |
| 中立 | [黍_中立.ckpt](https://huggingface.co/hualuoo/Arknights-Roles/resolve/main/黍/GPT_weights_v5turbo/黍_中立.ckpt?download=true) | [黍_中立.pth](https://huggingface.co/hualuoo/Arknights-Roles/resolve/main/黍/SoVITS_weights_v5turbo/黍_中立.pth?download=true) |
| 吃惊 | [黍_吃惊.ckpt](https://huggingface.co/hualuoo/Arknights-Roles/resolve/main/黍/GPT_weights_v5turbo/黍_吃惊.ckpt?download=true) | [黍_吃惊.pth](https://huggingface.co/hualuoo/Arknights-Roles/resolve/main/黍/SoVITS_weights_v5turbo/黍_吃惊.pth?download=true) |
| 开心 | [黍_开心.ckpt](https://huggingface.co/hualuoo/Arknights-Roles/resolve/main/黍/GPT_weights_v5turbo/黍_开心.ckpt?download=true) | [黍_开心.pth](https://huggingface.co/hualuoo/Arknights-Roles/resolve/main/黍/SoVITS_weights_v5turbo/黍_开心.pth?download=true) |
| 生气 | [黍_生气.ckpt](https://huggingface.co/hualuoo/Arknights-Roles/resolve/main/黍/GPT_weights_v5turbo/黍_生气.ckpt?download=true) | [黍_生气.pth](https://huggingface.co/hualuoo/Arknights-Roles/resolve/main/黍/SoVITS_weights_v5turbo/黍_生气.pth?download=true) |
| 难过 | [黍_难过.ckpt](https://huggingface.co/hualuoo/Arknights-Roles/resolve/main/黍/GPT_weights_v5turbo/黍_难过.ckpt?download=true) | [黍_难过.pth](https://huggingface.co/hualuoo/Arknights-Roles/resolve/main/黍/SoVITS_weights_v5turbo/黍_难过.pth?download=true) |

## 使用语音模型

1. 准备支持 **GPT-SoVITS v5turbo** 的环境，并下载上述 GPT 与 SoVITS 底模，安装与运行方法参见 [GPT-SoVITS 项目](https://github.com/RVC-Boss/GPT-SoVITS)。
2. 根据需要下载通用模型或某种情绪模型的两份权重，在推理界面中分别加载 GPT（`.ckpt`）与 SoVITS（`.pth`）文件。
3. 提供参考音频及对应文本，输入待合成的文本并生成语音。也可以将角色卡生成的回复文本用于语音合成。

例如，使用通用模型时，加载 `GPT_weights_v5turbo/黍.ckpt` 与 `SoVITS_weights_v5turbo/黍.pth`；使用开心模型时，加载 `GPT_weights_v5turbo/黍_开心.ckpt` 与 `SoVITS_weights_v5turbo/黍_开心.pth`。
