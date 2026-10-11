# dsh-workmode
`nGitHub: https://github.com/broken-air/dsh-workmode`n`n## 安装`n`n```powershell`ndsh plugin --profile desktop add github:broken-air/dsh-workmode`n``` `n
Dsh Desktop 专用的“工作模式”插件。它的目标是减少仅因敏感词触发的误拒答，同时保留对明确现实伤害请求的必要边界。

## 行为

- 优先理解任务类型和用户上下文；
- 对敏感主题继续提供背景、分析、诊断、规划、代码审查和防御性建议；
- 需要限制时只限制具体高风险步骤，并继续回答安全部分；
- 不修改审批、沙箱、文件系统或网络权限；
- 配置可通过 Dsh 的 profile 覆盖，停用后不注入任何规则。

## 配置

```yaml
- insert:
    - id: dsh-workmode
      config:
        enabled: true
        mode: coding # balanced | research | coding
        extraInstructions: "你的项目约束"
```

本插件只适用于用户有权管理的 Dsh Desktop 实例。应用前建议保留 Dsh profile 备份。


