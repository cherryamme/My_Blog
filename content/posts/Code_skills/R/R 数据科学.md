---
title: R数据科学
description: Description
date: 2021-12-14T03:23:22+08:00
weight: 20
menu:
  sidebar:
    name: R数据科学
    identifier: R数据科学
    parent: 读书笔记
    weight: 20
---


# R数据科学

这本书是 Hadly 的著作,  学习 tidyverse 的首选参考书.





## ggplot2包

每个图层都可以设置自己的数据.

![1](/img_R_数据科学/image-20211210162952819.png)

111 


![2](/images/virus_PNG.png)

buxma

![image-20211210162952819](/img_R_数据科学/image-20211210162952819.png)

`geom_bar()` 有三种方式: "identity",  "fill",  "dodge"



### 配色方案

![image-20211210183521408](img_R_数据科学/image-20211210183521408.png)



## dplyr包

`select()`辅助函数:  `starts_with()`,  `contains()`,  `match()`,  `everthing()`等.

`rename()`:  修改列名





### 偏移函数

`lag()`,  `lead()`:  在`group_by()`中特别有用



### 排秩函数

`min_rank()`,  `row_number()`,  `dense_rank()`,  `percent_rank()`,  `cume_dist()`



`summarize()`摘要函数:  	`mean()`,  `median()`,  `min()`,  `max()`,  `first()`,  `last()`,  `nth(x,2)`,   `n_distinct()`,  



## forcats包

`fct_recode()`:  修改因子水平名称

![image-20211210172723259](img_R_数据科学/image-20211210172723259.png)

`fct_collapse()`:  合并不同因子水平

![image-20211210172625188](img_R_数据科学/image-20211210172625188.png)

## 管道使用

![image-20211210173053241](img_R_数据科学/image-20211210173053241.png)

### 编写适配管道的函数

![image-20211210173630001](img_R_数据科学/image-20211210173630001.png)





## 循环迭代

循环时最好提前定义好变量空间,用`[[]]`赋值,  在原子向量中也明确使用`[[]]`表示处理单个元素.

循环索引使用 `seq_along()`更好.

![image-20211210174457601](img_R_数据科学/image-20211210174457601.png)



### 使用 purrrr

`map()`



`map2()`

![image-20211210175709546](img_R_数据科学/image-20211210175709546.png)

`pmap()`

![image-20211210175802056](img_R_数据科学/image-20211210175802056.png)

`invoke_map()`

![image-20211210175830654](img_R_数据科学/image-20211210175830654.png)

#### 预测函数

`keep()`,  `discard()`,  `some()`,  `every()`

![image-20211210175907866](img_R_数据科学/image-20211210175907866.png)



## 使用列表列

创建列表列:  `nest()`,  `mutate()`,  `summarize()`

`mutate()`+`map_int()`可以创建为原子向量

`unnest()`可以将列表列还原为普通列, 每个普通列重复一次



## rmarkdown 代码段选项

常用选项:

- eval
- include
- echo
- results
- fig.show
- message
- warning

![image-20211210182743784](img_R_数据科学/image-20211210182743784.png)

简要图:

![image-20211210182815602](img_R_数据科学/image-20211210182815602.png)

### rmarkdown 设置缓存

避免运行花费太多时间

![image-20211210183257320](img_R_数据科学/image-20211210183257320.png)