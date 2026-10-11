# 伊卡洛斯杯 · HEAT 海上竞速

Foundry VTT **v12** 测试模组。一个共享玩家席位与Legends自动对手在120格十门单程海路上竞速，默认1玩家＋3自动船。

## 安装

在Foundry Setup → Add-on Modules → Install Module中粘贴：

```text
https://raw.githubusercontent.com/litchicalpis/icarian-cup-heat/main/module.json
```

也可以从[Release v0.1.1](https://github.com/litchicalpis/icarian-cup-heat/releases/tag/v0.1.1)下载`icarian-cup-heat-0.1.1.zip`，解压到用户数据`Data/modules/`，确认存在`Data/modules/icarian-cup-heat/module.json`。

**不要使用GitHub自动生成的Source code ZIP。** 本仓库默认分支只保存README与稳定清单；完整运行代码、规则数据、素材、安装说明及来源记录位于Release安装ZIP。每次发行提供`module.json`、安装ZIP与`SHA256SUMS.txt`。

## 内容

- HEAT基础玩家流程；Legends全部1—6档，2—6档启用Stars；无天气、宿敌、车库、锦标赛或其他赛道。
- 默认1＋3，可配置1—5艘自动船；多人账号可共同操作同一人类席位。
- 上方连续高程海图只标海峡，内部船棋子沿航路转向；不创建原生Foundry Token。
- 下方120进度×2船位，默认两段2×60，可展开为单条。
- GM管理／授权并在线自动裁决；玩家提交决策，AI自动行动；逐步保存、导出及恢复。

进入World后默认不自动弹窗，按`Shift+I`、左侧工具栏的伊卡洛斯杯按钮或模组设置中的“打开竞速面板”手动打开。客户端设置“进入世界时打开伊卡洛斯杯”仍可开启；0.1.1不会覆盖已保存的开启或关闭偏好，后台初始化、同步与自动裁决不受影响。

GM先取得裁决权、授权玩家，再创建比赛。GM可以关闭模组窗口，但必须保持该浏览器会话在线；GM断线时暂停结算。

## 测试状态与限制

0.1.1继续标记为 **Pre-release**。131项Node测试通过，包含48场完整策略模拟，以及默认静默、已保存开启／关闭偏好、启动错误和版本一致性回归；启动测试执行真实Runtime初始化。0.1.1已重新通过Edge浏览器模拟检查，涵盖双端同步、完整人类回合与自动对手、六档难度、存档及布局，但模拟Foundry接口不等于实机验收；**未完成真实FVTT v12服务器双端联机验收**。建议使用备份后的测试World，发布本身不会修改任何服务器或World。

随包牌库忠实转录固定公开社区来源，并通过完整性及逐字段比较；不是官方数字版。C-01：第10组绿色船在绿组的速度18，以及黄／红组速度19但无星，尚待清晰实体牌确认。本版保留来源值、不凭模式擅改；详见ZIP内`DATA-SOURCES.md`。

## 素材与权利

地图基于用户已有连续高程场；5张船图和海图内嵌海面、羊皮纸纹理来自用户已有的Nantucket素材。HEAT、Legends、Nantucket及素材权利归原权利人，本项目非官方、无关联或背书。

本测试发布不声称取得第三方素材授权，也不授予第三方素材的再分发许可。原始素材提取目录、用户存档、密钥、浏览器数据与工程私有资料不随本仓库或Release上传。
