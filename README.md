# BY-master.github.io

个人 Hugo 博客。

## 常用命令

### 新建文章

```bash
hugo new posts/xxx.md
```

### 构建站点

```bash
hugo -d docs
```

### 提交更新

PowerShell：

```powershell
git commit -m "updates $((Get-Date).AddHours(-3).ToString('yyyy-MM-dd HH:mm:ss'))"
```

Git Bash / Linux / macOS：

```bash
git commit -m "updates $(date)"
```