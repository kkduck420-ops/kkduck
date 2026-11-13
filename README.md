# 亚马逊FBA发货Skill

把已验证的FBA发货操作流程提供给另一台电脑的Codex使用。包含自选承运人单仓建货件、仓库与货代确认、10×10cm箱标偏好、发票模板、PO核对及按渠道验证的箱号追踪关联。

## 在小马电脑安装

把下面这段发送给小马电脑的Codex：

> 使用skill-installer，从 https://github.com/kkduck420-ops/kkduck/tree/main/skills/amazon-fba-freight-workflow 安装amazon-fba-freight-workflow。检查已安装目录，避免重复安装。读取其中references/setup-and-sharing.md，在本机检查并配置紫鸟CLI、授权、终端绑定和店铺登录。运行doctor，再只读确认指定亚马逊店铺与美国站；先不要创建真实货件。

安装后可以直接说：

> 用amazon-fba-freight-workflow为这批货做FBA计划，使用自己的承运人、单仓合仓，显示收货仓和费用时暂停。以下是装箱资料……

Skill不会搬走其他电脑的登录态。每台机器的紫鸟授权独立配置；用户已在当前任务授权继续时直接执行，不把安装Skill等同于获准发起真实发货。

## 流程

1. 核对每箱SKU、件数、尺寸和毛重。
2. 建立FBA计划，自选承运人、单仓；核实实际SPD／LTL。
3. 显示仓库、地址和配置费，附可转发货代的话术，按用户指定节点暂停。
4. 确认船期和时效口径，估计到仓周，再按授权生成货件。
5. 核对货件号、PO及逐箱箱号，下载并检查正确箱标；打印按100×100mm偏好处理。
6. 使用清洁模板填发票，其他未知申报字段留货代填写，不沿用示例默认值。
7. 支持箱号关联的既有渠道可逐箱填对应箱号，保存刷新核对真实物流关联；其他渠道按实际追踪号。
8. 验收所有箱已确认、后台步骤完成，分别记录交货代、开船和亚马逊接收状态。

## 文件

- `skills/amazon-fba-freight-workflow/SKILL.md`：Skill入口。
- `skills/amazon-fba-freight-workflow/references/`：分步操作、模板字段和新电脑安装说明。
- `skills/amazon-fba-freight-workflow/assets/fba-invoice-template.xlsx`：脱敏空白模板。

本仓库不包含真实订单号、PO、物流号、联系人、密钥或浏览器数据。模板中的公共仓库地址库会变化，每票仍须与当前亚马逊地址核对。

参考：[OpenAI Skills](https://learn.chatgpt.com/docs/build-skills)、[紫鸟CLI官方安装指引](https://ziniao-open-prod.s3.cn-northwest-1.amazonaws.com.cn/ziniao-cli/SETUP.md)。
