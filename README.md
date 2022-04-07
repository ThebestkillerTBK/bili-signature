# 哔哩哔哩自动更改个人简介

![GitHub stars](https://img.shields.io/github/stars/ThebestkillerTBK/bili-signature?style=flat)![GitHub stars](https://img.shields.io/github/forks/ThebestkillerTBK/bili-signature?style=flat)

[wuziqian211/bili-auto-change-sign](https://github.com/wuziqian211/bili-auto-change-sign)的Python版。

## ❓介绍

哔哩哔哩自动更改个人简介: 一个灵活的个人简介自动更改工具

本程序可以根据自己的哔哩哔哩账号的粉丝数, 自动更改您的个人简介。

## 🚀使用方法

首先**把 ``config.json.template`` 重命名为 ``config.json``.**

然后运行 ``python bili-signature.py``!

## ⚙配置文件

``SESSDATA`` 你的 SESSDATA.

``bili_jct`` 你的 bili_jct.

``freq`` **更新频率(秒). 太低会触发反爬虫系统.**

``signature`` 你的个人简介, %d是粉丝数.

``advancedMode`` 是否高级开启模式.

### ``advanced`` 用来判断条件

* ``criteria`` 条件，有 ``time``, ``date``, ``fans``

  * 对于fans:
    * ``RPN`` 逆波兰表达式, %d是粉丝数.
    * ``type`` 当结果>=,>,<=,<,=当前时间，根据条件更改简介.
    * ``value`` 与结果比较的值. 只支持整数. (RPN type value)
  
  * 对于time:
    * ``time`` 时间. (%H:%M)
    * ``type`` 当结果>=,>,<=,<,=比较的值时，根据条件更改简介.
  
  * 对于date:
    * ``date`` 日期. (%Y-%m-%d)
    * ``type`` 当结果>=,>,<=,<,=比较的值时，根据条件更改简介.
  
* ``ifTrue`` 返回真时的简介.

* ``ifFalse`` 返回假时的简介.

* ### 简介格式

  * 如果上两个参数里有 ``tw`` 则进行套娃, 其中是 ``advanced``,  有``data``就会启用随机简介, (数组)其余参数可省略.

* 参数和上面相同.

## 🚗运行

* 运行 ``pip install -r requirements.txt``.
* 编辑 ``config.json`` 来配置参数.
* 享受吧~

## ✔注意事项

🍪 **如何获取cookies: 打开你的浏览器获取(这不用说谁都知道吧).**

⭐ 如果喜欢的话请帮忙`star`支持一下！

🐛 有Bug可以开Issue或PR
