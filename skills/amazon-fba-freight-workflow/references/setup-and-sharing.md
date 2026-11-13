# 新电脑安装与共享

这份Skill共享操作方法和清洁发票模板。每台电脑仍使用自己的紫鸟CLI配置、终端绑定和店铺登录；GitHub账号不能代替亚马逊／紫鸟授权。

## 安装Skill

推荐在员工电脑的Codex输入：

> 使用skill-installer，从 https://github.com/kkduck420-ops/kkduck/tree/main/skills/amazon-fba-freight-workflow 安装amazon-fba-freight-workflow。检查本机是否已经安装，避免重复安装同名Skill。安装后读取本文件，检查紫鸟CLI环境，先只读验收，不创建货件。

当前官方用户级Skill目录为`~/.agents/skills`，项目级为`.agents/skills`。本机若使用旧版`~/.codex/skills`或配置指定位置，按当前版本实际发现位置安装一份，不同时复制到两个扫描目录。以本机skill-installer的支持选项和Codex已加载列表为准。新Skill通常自动发现；未显示时重新打开Codex或新建一轮对话。

手工安装时，完整复制本Skill文件夹，保留`SKILL.md`、`agents`、`references`和`assets`；不要只复制SKILL.md。

## 紫鸟CLI依赖

- 先检查`ziniao-cli --version`、`node -v`及操作系统。当前机器已可正常运行时，不重复安装、初始化或换账号。
- 新机器缺CLI时，按[紫鸟官方安装指引](https://ziniao-open-prod.s3.cn-northwest-1.amazonaws.com.cn/ziniao-cli/SETUP.md)在本机安装正式版`@ziniao-open/cli`，再运行`ziniao-cli skills install --copy`。不要复制老板电脑的密钥配置，也不要把真实Key放入仓库、命令参数或聊天。
- 新机器的认证、启动及终端绑定按安装的`ziniao-shared`技能和该电脑现有权限模式处理；不把网页教程的权限要求当作绕过当前系统限制的许可。
- 执行`ziniao-cli doctor`。必须确认本机配置与API Key有效、终端已绑定、紫鸟客户端已登录、Bridge连通。服务端管理API的IP白名单失败若明确不影响本地浏览器，不据此阻断本地页面操作。
- 如果环境正常，使用`ziniao-store`／`ziniao-page`。不要为了恢复读取反复新建授权、重启客户端或打开重复店铺窗口。参数不明时查看本机`--help`，不要沿用其他设备的target-id。

## 第一次验收

只读列出可访问店铺，解析用户指定店铺；打开或复用正确店铺并确认Seller Central商家和美国站。报告CLI、Bridge、登录状态和实际可读页面。第一次验收不建真实货件、不改价格／广告、不回传追踪，不自动开启巡店。

之后可以说：

> 用amazon-fba-freight-workflow为红珊瑚建立这批FBA计划，使用自己的承运人、合到一个仓；做到显示收货仓和费用时暂停。装箱数据如下……

## 共享与更新

仓库：https://github.com/kkduck420-ops/kkduck

公开仓库只放Skill、清洁模板和合成示例。每票FBA号、PO、真实追踪号、产品实拍、客户数据和操作证据保存在本机业务资料目录，不提交GitHub。仓库不携带API Key、浏览器cookie、登录状态、自动任务或本机绝对路径。

更新时在每台电脑让Codex比较GitHub版本与已安装Skill，备份旧版本后仅替换本Skill目录。保留本机CLI配置和业务记录。安装或更新Skill不会自动执行发货，也不会自动同步其他机器的运行进度。

官方依据：[OpenAI Skill安装与目录说明](https://learn.chatgpt.com/docs/build-skills)。
