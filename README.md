<div align="center">

# 🎮 EVIL-Endstone

**Endstone BDS 插件集合**

[![Author](https://img.shields.io/badge/Author-EVIL--ZIXIE-blueviolet?style=for-the-badge)](https://github.com/EVIL-ZIXIE)
[![Platform](https://img.shields.io/badge/Platform-Endstone_BDS-00599C?style=for-the-badge)](https://github.com/EndstoneMC/endstone)
[![License](https://img.shields.io/badge/License-Closed_Source-red?style=for-the-badge)]()

</div>

---

## 📋 简介

本仓库包含我开发的所有 **Endstone BDS** 服务器插件。

- 🔒 **闭源项目** - 仅提供编译后的插件文件
- 🌐 **中英双语** - 所有插件支持中英文切换
- 🔌 **开发者友好** - 提供 C++ / Python API 接口

---

## 📦 插件列表

### 💰 MoneyCore 经济核心

功能完善的服务器经济系统。

| 特性 | 说明 |
|------|------|
| 💱 双经济模式 | 支持插件经济 / 计分板经济 |
| 🌐 双语支持 | 中文 / 英文自由切换 |
| 💸 玩家功能 | 转账、排行榜、交易记录 |
| 👨‍💼 管理功能 | 增减余额、批量操作、数据迁移 |
| 🔌 开发者API | 提供 C++ / Python 接口 |

**下载**: [endstone_money_core.dll]()

---

### 🎮 GameRuleManager 游戏规则管理器

可视化的游戏规则管理器。

| 特性 | 说明 |
|------|------|
| 📋 可视化界面 | GUI 表单操作，无需命令 |
| 🔧 完整支持 | 支持所有原版游戏规则 |
| 🔐 权限控制 | 管理员权限保护 |

**下载**: [endstone_gamerule_manager.dll]()

---

### 🏪 ShopSystem 商店系统 `开发中`

服务器商店系统，对接 MoneyCore 经济。

---

## 🔌 开发者 API

为其他插件开发者提供经济系统接口。

### C++ 接入

```cpp
#include "money_api.h"

auto service = getServer().getServiceManager().load<IMoneyService>("MoneyService");
if (service) {
    double bal = service->getMoney("PlayerName");
    service->trySubMoney("PlayerName", 100, "购买物品");
}
```

### Python 接入

```python
from money_api import MoneyAPI

money = MoneyAPI(self)
bal = money.get_money("PlayerName")
money.try_sub_money("PlayerName", 100, "购买物品")
```

### API 文件下载

| 文件 | 语言 |
|------|------|
| [money_api.h]() | C++ |
| [money_api.py]() | Python |

---

## 💻 系统要求

- **Endstone BDS**: v0.10+
- **操作系统**: Windows / Linux

---

## 📥 安装方法

1. 下载对应的 `.dll` 文件
2. 放入服务器 `plugins/` 目录
3. 重启服务器

---

## 📫 问题反馈

如有问题或建议，请提交 Issue：

[![GitHub Issues](https://img.shields.io/badge/GitHub-提交Issue-181717?style=for-the-badge&logo=github)](https://github.com/EVIL-ZIXIE/EVIL-Endstone/issues)

---

<div align="center">

**Made with ❤️ by [EVIL-ZIXIE](https://github.com/EVIL-ZIXIE)**

</div>
