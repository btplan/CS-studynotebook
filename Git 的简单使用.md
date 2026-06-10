## 一、仓库管理（Repository）

|操作|命令|
|---|---|
|初始化仓库|`git init`|
|查看仓库状态|`git status`|
|查看远程仓库|`git remote -v`|
|绑定远程仓库|`git remote add origin URL`|
|修改远程仓库|`git remote set-url origin URL`|
|删除远程仓库|`git remote remove origin`|

---

## 二、日常开发（每天都会用）

|操作|命令|
|---|---|
|查看状态|`git status`|
|查看修改内容|`git diff`|
|添加所有修改|`git add .`|
|添加单个文件|`git add 文件名`|
|提交到本地|`git commit -m "feat: add xxx"`|
|上传到 GitHub|`git push`|
|拉取最新代码|`git pull`|

> 推荐流程：

```bash
git status
git add .
git commit -m "feat: add quality evaluation"
git push
```

---

## 三、Commit（版本快照）

|操作|命令|
|---|---|
|查看历史|`git log --oneline`|
|查看详细历史|`git log`|
|图形化查看历史|`git log --oneline --graph --decorate --all`|

推荐 Commit Message：

```
feat: 新功能
fix: 修复Bug
docs: 更新文档
refactor: 重构
test: 测试
chore: 杂项维护
```

例如：

```
feat: add graph construction
fix: resolve coordinate mapping
docs: update README
```

---

## 四、Tag（版本发布）

| 操作        | 命令                                       |
| --------- | ---------------------------------------- |
| 查看所有Tag   | `git tag`                                |
| 创建Tag（推荐） | `git tag -a v1.0.0 -m "Initial release"` |
| 查看Tag详情   | `git show v1.0.0`                        |
| 上传所有Tag   | `git push --tags`                        |
| 上传单个Tag   | `git push origin v1.0.0`                 |
| 删除本地Tag   | `git tag -d v1.0.0`                      |

推荐版本：

```
v1.0.0  初始版本
v1.1.0  新功能
v1.2.0  Bug修复
v2.0.0  大版本更新
```

---

## 五、Branch（分支）

|操作|命令|
|---|---|
|查看所有分支|`git branch`|
|查看远程分支|`git branch -r`|
|查看所有分支（本地+远程）|`git branch -a`|
|创建并切换分支|`git checkout -b experiment`|
|切换分支|`git checkout main`|
|重命名当前分支|`git branch -M main`|
|删除分支|`git branch -D experiment`|

> 个人科研项目推荐：
> 长期只维护一个 `main` 分支，重要版本使用 Tag，不建议创建大量 Branch。

---

## 六、回滚与恢复

|操作|命令|
|---|---|
|查看旧版本|`git checkout commit_id`|
|回滚到某个Commit|`git reset --hard commit_id`|
|回滚到上一个Commit|`git reset --hard HEAD~1`|
|恢复未提交修改|`git restore 文件名`|
|删除未跟踪文件|`git clean -fd`|

---

## 七、GitHub 第一次上传

```bash
git init

git remote add origin https://github.com/用户名/仓库名.git

git add .

git commit -m "feat: initial project"

git branch -M main

git push -u origin main
```

以后：

```bash
git add .

git commit -m "feat: add xxx"

git push
```

---

## 八、发布一个版本（推荐流程）

```bash
# 修改代码

git add .

git commit -m "feat: add quality evaluation"

# 更新 CHANGELOG（可选）

git add CHANGELOG.md

git commit -m "docs: update changelog"

# 创建版本

git tag -a v1.1.0 -m "Quality evaluation release"

# 上传代码

git push

# 上传Tag

git push --tags
```

---

## 九、项目文档建议

```
README.md        项目介绍
CHANGELOG.md     更新日志
LICENSE          开源协议
.gitignore       Git忽略文件
```

---

# 十、个人科研项目推荐工作流

```
修改代码
        │
git status
        │
git add .
        │
git commit -m "feat: xxx"
        │
git push
        │
───────────────
重大更新
        │
更新CHANGELOG
        │
git commit
        │
git tag -a v1.1.0 -m "Release"
        │
git push
        │
git push --tags
```

> 推荐：**一个 `main` 分支 + 清晰的 Commit + Tag + CHANGELOG**，足够满足绝大多数个人科研项目和 GitHub 开源维护需求。