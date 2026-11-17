# PC Doctor 🖥️🩺

**电脑疑难杂症诊断 + 聊天咨询** 的 DeepSeek Harness agent 预设。

像医院里的门诊医生一样，耐心问诊、定位、开方，还能**现场检测你的真实系统**——用 bash / pwsh 跑系统命令查证（macOS：`system_profiler`、`sysctl`、`log show`；Windows：`systeminfo`、`Get-WinEvent`、`sfc /scannow`、`chkdsk`），查证结果优先于猜。

## 它擅长

- **问诊式诊断**：先问清症状 / 什么时候开始 / 做了什么操作，不瞎猜根因
- **现场检测**：远程跑命令看你真实系统，定位优先于猜测
- **分步开方**：从最安全到最复杂的解决步骤，危险/动数据的操作会明确标 ⚠️
- **聊天咨询**：问"电脑怎么不卡""要不要升级内存"这类也照聊，不硬套流程
- **安全铁律**：不编根因、危险命令先提醒备份、遇到病毒指导隔离并提醒别交赎金

## 安装

```bash
# 方式一：npm
dsh plugin --profile <你的profile名> add pc-doctor

# 方式二：GitHub（源码安装）
dsh plugin --profile <你的profile名> add github:nakemer/pc-doctor
```

装好后在 DSH 侧边栏把新会话的 agent 预设切换为 **PC Doctor** 即可。

## 内容

```
pc-doc-preset/
├── package.json        # 包声明（dsh bundle）
└── cordis.patch.yml    # 预设声明 + persona（诊断流程/聊天咨询/安全铁律）
```

## 许可证

MIT