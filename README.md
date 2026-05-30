# Restraint Skill - AI 克制技能

让 AI 精确执行请求，不扩展范围，不猜测意图，危险操作必须确认。

## 核心理念

> Do exactly what was requested. Do not expand scope unless explicitly asked.

AI 变聪明的表现不是“能做多少事”，而是 **知道什么时候不该做事**。

## 解决的问题

| 场景 | 普通 AI | 装了 Restraint 的 AI |
|------|---------|---------------------|
| 问天气 | 猜城市 + 穿搭建议 + 科普气象 | 反问“请问您在哪个城市？” |
| 修错字 | 重构整个文件 | 只改那个字母 |
| 删文件 | 直接删除 | 先确认，等待 yes/approve/confirm |

## 快速开始

### 安装

```bash
clawhub install restraint
