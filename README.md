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

## 部署排查

### GitHub Pages 没更新

如果代码已经 push，但线上页面还是旧内容或 404，先检查 Deployments 里的 commit 是否和最新 commit 一致。

```powershell
git log -1 --oneline
git ls-remote origin refs/heads/main
```

如果 GitHub Pages 仍然部署旧 commit，可以用空提交强制重新部署：

```powershell
git commit --allow-empty -m "trigger pages deploy"
git push origin main
```

部署成功后，页面可能还会有短暂缓存，刷新或用无痕窗口查看。