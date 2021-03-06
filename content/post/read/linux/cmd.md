---
title: "linux - 使用命令"
date: 2019-06-01T10:32:33+08:00
tags: [linux]
categories: [read]
hiddenFromHomePage: true
---

## 使用命令
- `type` 显示命令的类型
- `which` 显示一个可执行程序的位置
- `help` 得到 shell 内建命令的帮助文档
- `--help` 显示用法信息
- `apropos（man -k）` 显示适当的命令
- `whatis` 显示简洁的命令说明
- `info` 显示程序Info条目
- `alias` 创建自己的命令（多个命令`;`分开）
## man
>显示程序手册页
1. 用户命令
2. 程序接口内核系统调用
3. C 库函数程序接口
4. 特殊文件，比如说设备结点和驱动程序
5. 文件格式
6. 游戏娱乐，如屏幕保护程序
7. 其他方面
8. 系统管理员命令

## 重定向
- `>` 输出（`>>` 追加）到文件
- `2>` 错误输出到文件
- `&>` 重定向标准输出和错误到同一个文件（旧版本：`>file.txt 2>&1`）
- `/dev/null` 处理不需要的输出
- `cat` 连接文件
- `|` 管道线、过滤器
- `uniq` 报道或忽略重复行
- `wc` 打印行数、字数和字节数
- `grep` 打印匹配行(`-i`忽略大小写，`-v`不匹配)
- `head/tail` 打印文件开头部分/结尾部分(`-n`指定，默认10，`-f`实时浏览)
- `tee` 从 Stdin 读取数据，并同时输出到 Stdout 和文件

## 从shell眼中看世界
- `echo` 显示一行文本
- `echo *` 字符展开
- `echo D*` 路径名展开
- `echo ~` 波浪线展开
- `echo $((2 + 2))` 算术表达式展开（取幂**）
- `echo {Z..A}` 花括号展开
- `echo $USER` 参数展开（printenv|less查看变量列表）
- `file $(ls /usr/bin/- | grep zip)` 命令替换（旧版本：ls -l `which cp`）
- `echo this   a` 引用
- `ls -l "two words.txt"` `""`，`$`，`\`，`外的特殊字符失效
- `echo '$USER'` 禁止所有展开
- `echo \$5.00` 转义字符