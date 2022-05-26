



# 详细设计及设计工具

## 结构化详细系统设计

- 目的
  
  - 确定模块内所用算法和数据结构
  
  - 决定外部和用户接口
  
  - 给出被选中表达的清晰描述

## 盒图（N-S图）

![](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/3%60508%603QL%7D8JXZFGVZ%24%246J8.png)

- 特点
  
  - 表达功能域明确
  
  - 无箭头，不允许随意转移控制
  
  - 很容易确定局部和全程数据的作用域
  
  - 看起来像大盒子套小盒子，容易表示嵌套和层次结构

- 实例![][Markdown-images/7T$]R_H}22LX8A79AQKSV)D.png at main · misaka-umi/Markdown-images · GitHub](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/7T%24%5DR_H%7D22LX8A79AQKSV)

## PAD图

- 问题分析图
  
  - 二维树形结构
  
  - 表示程序的数据流或业务流程模式

- 表达

![](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/OP5OBRZJK%252ZM1X%5BL)

- b
  
  - if P then A else B

- c
  
  - While P do S

- d
  
  - Repeat P until S

- e
  
  - Case P？ do A？

- f
  
  - 语句标号

- g
  
  - 定义

![](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/NYW0312%40TD1W(_DSH9OU0UH.png)

- 优势
  
  - ....

- 例子

- ![](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/SVW4%40G54LTU46U84IL9U(V1.png)

- ![](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/O(A49535ZT18Q6%7DKYOOA%24TL.png)

## decision table 判定表



![3.3.1.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/3.3.3.1.png)

![3.3.3.2.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/3.3.3.2.png)

- 优势、劣势

## decision tree 判定树

- 判定表所表示含义不明显不直观
  
  - 引入判定树

- 步骤
  
  - 分出判定条件、判定决策
  
  - 找出条件的从属、并列、选择关系
  
  - 构造判定树
    
    ![3.3.4.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/3.3.4.png)

## 层次图与IPO图

- 层次图
  
  - 用树形结构来描述软件层次结构
  
  - ![3.3.5.1.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/3.3.5.1.png)
    
    

- IPO图
  
  - 描述输入数据、数据处理和输出数据的关系
  
  - ![3.3.5.2.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/3.3.5.2.png)
    
    

- HIPO图
  
  - 描述系统层次结构和模块内部处理
    
    ![3.3.5.3.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/3.3.5.3.png)
    
    ![3.3.5.4.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/3.3.5.4.png)

# 面向对象的建模

## 面向对象的分析建模

- 需求建模

- 分析建模

- 设计建模

- OOA->OOD 多次反复 逐步迭代

- 步骤
  
  - 细化用例
  
  - 识别与确定分析类
    
    - 实体类
      
      - 持久性
    
    - 边界类
      
      - 用户界面
      
      - 系统接口
      
      - 硬件接口
    
    - 控制类
      
      - 独立环境
      
      - 确定用户中的控制逻辑与事务
      
      - ....
