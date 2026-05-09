# figma-mcp-skill

在写代码前先和用户对齐：**Figma** 不擅自加稿外文案/图/功能；**涉及后端**时先把完整实现路径（含所有分支与数据源）说清楚，确认后再动手。

Skill 定义文件：`.cursor/skills/confirm-before-implement/SKILL.md`。

---

## 安装到你自己的项目

把本仓库里的整个文件夹 **`confirm-before-implement`** 复制到你的项目：

`.cursor/skills/confirm-before-implement/`

若项目中还没有 `.cursor/skills`，请先创建目录再粘贴。

用 **Cursor 打开该项目**，在对话里输入 **`@`**，选择 **`confirm-before-implement`** 即可调用。

---

## 安装为全局（所有仓库可用）

将同名文件夹复制到本机：

```text
~/.cursor/skills/confirm-before-implement/
```

（若没有 `skills` 目录，请先新建。）

---

## 发布到 GitHub

1. 在 GitHub 新建空仓库（不要勾选添加 README，避免冲突）。
2. 在本机仓库目录执行（把下面的 URL 换成你的仓库地址）：

```bash
cd ~/confirm-before-implement-skill
git remote add origin git@github.com:<你的用户名>/<仓库名>.git
git branch -M main
git push -u origin main
```

他人 **克隆**本仓库后，按上文「安装到你自己的项目」或「全局」复制文件夹即可。

---

## License

沿用你对个人作品集仓库采用的许可证即可；若独立仓库需要单独 LICENSE，可自行添加。
