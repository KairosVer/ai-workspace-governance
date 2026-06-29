# 安全规则

本文件记录全库最高优先级的安全规则。任何整理、迁移、清理、脚本操作都必须遵守。

## 删除确认铁律

任何涉及以下关键字的命令，执行前必须列出清单、说明风险、等待用户确认：

- `rm -rf`
- `rm -r`
- `Remove-Item -Recurse`
- `del /s`
- `rd /s`
- 批量 `git clean`
- `git reset --hard`
- 任何涉及 3 个以上文件或目录的删除操作

## 删除替代策略

优先移动到 `7-Archive`，而不是直接删除。

## PowerShell 编码

当前机器已安装 PowerShell 7.6.3。处理中文文件时优先使用 PowerShell 7 (`pwsh`)；但为了避免不同终端、旧脚本或 Windows PowerShell 5.1 混用导致乱码，读写中文 Markdown 仍建议显式指定 UTF-8。

PowerShell 7 默认文本输出通常是 UTF-8，但规则仍是：显式编码优先于依赖默认值。

读取中文 Markdown：

```powershell
Get-Content -LiteralPath "file.md" -Encoding UTF8
```

写入中文 Markdown：

```powershell
Set-Content -LiteralPath "file.md" -Encoding UTF8
```

跨 PowerShell 版本最稳妥的方式：

```powershell
[System.IO.File]::ReadAllText($file, [System.Text.Encoding]::UTF8)
[System.IO.File]::WriteAllText($file, $content, [System.Text.UTF8Encoding]::new($false))
```

禁止在未确认编码的情况下批量改写中文文件。

## 图片安全

外部图片处理流程：下载到 `1-Attachment/`，使用清晰文件名，正文替换为 `![[filename.jpg]]`，确认图片可用后再删除原外部链接。

图片文件名用主题前缀，便于在数量增长后按主题检索。例如 `自制力-xxx.jpg`、`电荷转移电阻_xxx.png`、`合成-反应名_image1.png`。不强制建子目录，扁平结构配合主题前缀即可。

## Wiki-link 规则

vault 内正文链接使用 Obsidian wiki-link，不在笔记正文中写绝对路径。

链接优先用短名（`[[文件名]]`），仅在重名时加路径前缀（`[[子目录/文件名]]`）。这样文件移动后链接不易断。Atlas 地图页也优先用短名，必要时才写完整路径。

## 批量移动规则

批量移动前必须列出来源路径、目标路径、文件数量、是否覆盖同名文件、是否影响已有链接。移动后检查文件是否到位、链接是否需要修复、是否需要记录。

## AI 整理边界

AI 可以建议目录结构、提炼规则、生成模板、整理格式、创建索引。AI 不应未经确认批量删除、覆盖用户笔记、改写原始实验数据、编造来源或为了美观删掉关键数据。