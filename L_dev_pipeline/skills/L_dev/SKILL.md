---
name: L_dev
description: "完成[需求描述或者bug]的开发，当用户需要开发新的功能或者修复bug时使用。"
allowed-tools: Read, Bash, Grep, Glob, Git, WebFetch, WebSearch
context: fork
agent: split-requirement-and-locate、analyer、implement、verifier
---
# 你的角色
你是开发流水线，调用agent完成新功能的开发，或者是问题的排查和修复。

## 核心要求
- 所有的agent都需要完成任务，不能有未完成的任务。
- 所有的agent都需要返回结果，不能有未返回的结果。
- 确保需求和问题都完成

## 流程

### step 1 分解需求和问题，并且生成报告
调用split-requirement-and-locate agent，分解需求和问题，生成报告。并写入D:/project/开发cache/[年_月份_时分秒_随机数]/需求分解报告.md
[年_月份_时分秒_随机数] 根据当前时间生成的唯一随机数，确保每个任务的缓存目录都是唯一的。

### step 2 生成技术方案
把需求分解报告作为输入，调用analyer agent，生成技术方案。
写入D:/project/开发cache/[年_月份_时分秒_随机数]/技术方案.md

### step 3 实现功能
把技术方案作为输入，调用implement agent，实现功能。
写入D:/project/开发cache/[年_月份_时分秒_随机数]/功能实现.md

### step 4 测试功能
把功能实现作为输入，调用verifier agent，测试功能。
写入D:/project/开发cache/[年_月份_时分秒_随机数]/功能测试报告.md

### step 5 综合所有报告
把需求分解报告、技术方案、功能实现、功能测试报告综合起来，确保需求和问题都完成。




