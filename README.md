# 🪄 GitHub Auto Star Bot ✨

> 一个可爱又聪明的 GitHub Action，每小时自动帮你 Star 某个项目喵♡～
> 前 1 小时保持 Star，最后 1 小时保持取消 Star，然后重新开始循环喵～  
> 灵感来源于活动打卡、排行榜维持热度等场景 ✨

# 🚧 注意：频繁 `star` 操作可能会被封号。
> 目前本仓库是给 `AstrBotDevs` 的 [AstrBot](https://github.com/AstrBotDevs/AstrBot) 仓库点 `star`
>

> [!WARNING]
>
> 请不要用于非法用途，本仓库仅仅作为学习交流使用。

## 🐾 项目用途

使用 GitHub Actions 自动定时对指定仓库进行 Star / Unstar 操作，从而制造“刚刚 Star” 的效果，提高项目曝光度喵～

适合：
- 技术活动打卡或挑战
- 希望项目持续出现在 Star 动态中
- 为自己或朋友的项目打气（喵！）

## ✨ 功能逻辑

- 每小时执行一次（通过 `schedule` 触发）
- 前 1 小时会持续保持 Star 状态
- 到第 2 小时自动取消 Star
- 然后重新开始计数循环

## ⚙️ 使用方式

### 1. Fork 本仓库或将 `.github/workflows/star-cycle-2.yml` 放入你的项目中

### 2. 添加 Secrets（Settings → Secrets and variables → Actions）

| 名称             | 描述                       |
|------------------|----------------------------|
| `PERSONAL_TOKEN` | 你的 GitHub Classic Token（需要 repo 权限） |

> 💡 建议使用 [Classic Token](https://github.com/settings/tokens?type=beta)，并勾选 `public_repo` 权限即可。

### 3. 修改目标仓库

编辑 `main.yml` 中的这部分，替换为你要操作的目标仓库：

```yaml
      TARGET_OWNER: # 加star对象的用户名
      TARGET_REPO: #加star对象的仓库名
```
