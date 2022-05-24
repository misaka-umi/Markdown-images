# 良好的编程实践

- 变量命名
  
  - meaningful
  
  - consistent

- 编写自文档
  
  - 理解容易、无歧义
  
  - prologue comments 序言性注释
    
    - 组件名字
    
    - 代码作者
    
    - 代码功能描述
    
    - 组件描述
  
  - 行内注释
    
    - 代码难以理解时使用
    
    - 过多行内注释会影响简洁性、可理解性

- 很少有真正的常量
  
  - 因此最好使用变量代替常量

- 增加可读性的代码编排layout
  
  - 缩进
  
  - 空行
  
  - e.g. if嵌套的使用
    
    - if-if 与 if-else-if通常是难以阅读的
      
      - if-if简化为 ```if(a&&b)```
    
    - if嵌套应当避免超过三层

- 编码标准programming standards
  
  - 要灵活运用，不然可能有负面效果

# 代码集成

## 一次性集成

- drivers驱动模块和stubs存根模块
  
  - ![Screen Shot 2022-05-23 at 14.44.01.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/4.1.png)
  
  - 一次性集成的两个问题
    
    - 为测试某个模块，必须额外编写它的驱动模块和存根模块
    
    - 缺乏错误隔离
      
      - 错误可能存在于任何组件或接口中

## 系统集成

- 自顶向下集成
  
  - 可以有不同顺序
    
    - 广度优先
      
      ![Screen Shot 2022-05-23 at 14.48.04.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/4.2.png)
    
    - 深度优先
      
      ![Screen Shot 2022-05-23 at 14.48.19.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/4.3.png)
  
  - 优势
    
    - 错误隔离
      
      - 错误往往存在于刚刚被集成的模块，提高维护效率
    
    - 存根模块不被浪费
      
      - 新集成进的模块往往是前一模块的存根模块，不再需要额外设计存根模块
    
    - 较早发现设计方面错误
  
  - 问题
    
    - 较低层次的组件测试时间靠后
    
    - 较低层次的组件使用频率很高，但测试次数偏少

- 自底向上
  
  - 广度优先
    
    ![4.4.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/4.4.png)
  
  - 深度优先
    
    ![4.5.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/4.5.png)
  
  - 优势
    
    - 充分测试底层操作组件
    
    - 操作组件被驱动模块测试（因此不需要额外编写
    
    - 错误隔离
  
  - 问题
    
    - 主要的设计错误较晚被发现
  
  - solution
    
    - 结合自顶向下和自底向上->三明治集成

## 三明治集成

- 逻辑组件top-down

- 操作组件bottom-up

- 最后对两个组的接口进行集成和测试

![4.6.png](https://github.com/misaka-umi/Markdown-images/blob/main/software%20engineering/4.6.png)

- 优势
  
  - 主要设计错误能尽早发现
  
  - 操作组件充分被测试，且能保证测试质量
  
  - 错误隔离

## 面向对象集成

- 对象bottom-up

- 其他组件top-down

- 基本采用三明治集成

## 集成测试的管理

SQA团队负责，且对项目的过失负主要责任

# 4.3 4.4 4.5有pdf无视频课
