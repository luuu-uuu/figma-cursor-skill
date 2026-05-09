# figma-mcp-skill

本仓库提供一个 **Cursor Skill**，用于在写代码前先和用户达成一致：**Figma** 不擅自增加稿外文案/图/功能；**涉及后端**时先把完整实现路径（含所有分支与数据源）说清楚，确认后再动手。

---

## 命名说明（克隆前必读）

| 名称 | 含义 |
|------|------|
| **仓库名** `figma-mcp-skill` | GitHub 上本仓库的名字；克隆后本地目录一般也叫这个名字（除非你改名）。 |
| **Skill 文件夹** `confirm-before-implement` | 位于 `.cursor/skills/` 下，须**整夹复制**到你的项目或全局目录；在 Cursor 里用 **`@confirm-before-implement`** 调用（由 `SKILL.md` 里的 `name` 决定）。 |

二者不必同名；安装时请以 **文件夹 `confirm-before-implement`** 为准。

Skill 正文路径：`.cursor/skills/confirm-before-implement/SKILL.md`。

---

## 他人如何获取本仓库

```bash
git clone https://github.com/<用户名>/figma-mcp-skill.git
cd figma-mcp-skill
```

将 `<用户名>` 换成仓库所有者（例如本仓库维护者的 GitHub 用户名）。若使用 SSH：`git clone git@github.com:<用户名>/figma-mcp-skill.git`。

也可在 GitHub 网页上下载 **ZIP**，解压后同样能得到下面的目录结构。

---

## 安装到某个项目（推荐从此仓库复制）

1. 在上一步得到的仓库目录里，找到文件夹：  
   **`figma-mcp-skill/.cursor/skills/confirm-before-implement/`**  
   （若你克隆时改成了别的顶层目录名，则为 `<你的克隆目录>/.cursor/skills/confirm-before-implement/`。）

2. 将 **`confirm-before-implement`** 这一整夹复制到你的目标项目：  
   **`<目标项目>/.cursor/skills/confirm-before-implement/`**  
   若不存在 `.cursor` / `skills`，请先新建。

3. 用 **Cursor 打开目标项目**，在对话中输入 **`@`**，选择 **`confirm-before-implement`** 即可。

---

## 安装为全局（所有仓库可用）

将 **`confirm-before-implement`** 整夹复制到本机：

```text
~/.cursor/skills/confirm-before-implement/
```

若 `~/.cursor/skills` 不存在，请先创建再粘贴。

---

## 仓库目录结构（复制时对准这一层）

```text
figma-mcp-skill/
└── .cursor/
    └── skills/
        └── confirm-before-implement/   ← 复制这一文件夹
            ├── SKILL.md
            └── README.md
```

---

## License

请在本仓库根目录自行添加 `LICENSE`（如 MIT）；未添加前请勿假定默认许可证。
