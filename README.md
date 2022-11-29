# report-health
gxnu-yiban-yzdx report health

> 使用者有责任和义务保证自己上传的打卡数据真实可靠。  
> 本项目仅供学习交流使用，严禁用于其他用途! For learning and communication only, other use is strictly prohibited！  
> 作者不承担任何法律责任！The author assumes no legal liability！  

## 使用GitHub Actions实现自动化签到

1. Fork 这个仓库

2. 在仓库的 Settings -> Security -> Secrets -> Actions 中新建两条 repository secret：

   - `USER_NAME`，易班的登录手机

   - `USER_PASS`，易班的密码  

3. 启用 GitHub Actions

- 进入仓库的 Actions 页面，点击绿色的「I understand my workflows, go ahead and enable them」按钮

   - 出于安全考虑，GitHub 会对 Fork 时存在 Workflow 文件的仓库禁用 Actions，需要用户手动确认安全才会启用。

   - 如果仓库没有 Actions 页面，请进入仓库的 Settings -> Code and automation -> Actions -> General -> Actions permissions 检查是否允许运行 Actions。

- 点击右侧enable workflow

默认每周一自动触发两次 Workflow （GitHub Actions 高负载时可能延迟）。如需修改为其他时间或条件下签到，可按照 GitHub [文档](https://docs.github.com/cn/actions/using-workflows/triggering-a-workflow)修改 `.github/workflows/deploy.yml`。

订阅 GitHub Actions 的 [Workflow 运行通知](https://docs.github.com/cn/actions/monitoring-and-troubleshooting-workflows/notifications-for-workflow-runs)，可在签到失败（Workflow 执行失败）时收到通知提醒。

## 参考项目

[gxnu-yzdx-autoreport](https://github.com/Universoar/gxnu-yzdx-autoreport)  

[TsinghuaDailyReport](https://github.com/naihaishy/TsinghuaDailyReport)

---

![GitHub all releases](https://img.shields.io/github/downloads/dx87c/report-health/total)
