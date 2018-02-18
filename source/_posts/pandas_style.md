---
title: pandas中style输出格式
date: 2017-10-14
categories: 编程开发
tags: [pandas, python]
---

### 1.具体见

[官方手册](http://pandas.pydata.org/pandas-docs/stable/style.html)
http://pandas.pydata.org/pandas-docs/stable/style.html

### 2.(以下数据效果只能在Notebook中显示)

对于DataFrame数据df

A  | B | C
---|---|---
1 | 12.5 | 0.369448
2 | 0.6958 | 0.896
3 | 150.36 | 0.00256

如果对全部数据统一使用格式

```python
df.style.format("{:0.2f}")
```

那么输出的是

A | B | C
---|---|---
1.00|12.50|0.37
2.00|0.70|0.90
3.00|150.36|0.00

如果对某列数据进行格式化

```python
style = {'B': "{:0.2%}",
         'C': '{:+.2f}'}
df.style.format("{:0.2f}")
```

输出效果是

A | B | C
---|---|---
1|12.50|0.37
2|0.70|0.90
3|150.36|0.00