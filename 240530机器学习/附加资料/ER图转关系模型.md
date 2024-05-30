## 1:1联系的转换方法

<img src="https://img-blog.csdnimg.cn/20210411145828729.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNzA2MzMx,size_16,color_FFFFFF,t_70" alt="img" style="zoom:33%;" />

方法一：

将1:1联系转换为一个独立的关系：与该联系相连的各实体的码以及联系本身的属性均转换为关系的属性，且每个实体的码均是该关系的候选码。

       联系形成的关系独立存在：    
    
       职工（职工号，姓名，年龄）
    
       产品（产品号，产品名，价格）   
    
       负责（职工号，产品号）

方法二：

将1:1联系与某一端实体集所对应的关系合并，则需要在被合并关系中增加属性，其新增的属性为联系本身的属性和与联系相关的另一个实体集的码。

      “负责”与“职工”两关系合并：
    
       职工（职工号，姓名，年龄，产品号）
    
       产品（产品号，产品名，价格）

 




       也可以“负责”与“产品”两关系合并：
    
       职工（职工号，姓名，年龄）
    
      产品（产品号，产品名，价格，职工号
##  1:n联系的转换方法

<img src="https://img-blog.csdnimg.cn/20210411150025201.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNzA2MzMx,size_16,color_FFFFFF,t_70" alt="img" style="zoom:33%;" />

方法一：

一种方法是将联系转换为一个独立的关系，其关系的属性由与该联系相连的各实体集的码以及联系本身的属性组成，而该关系的码为n端实体集的码。

          联系形成的关系独立存在：
    
          仓库（仓库号，地点，面积）
    
          产品（产品号，产品名，价格）
    
          仓储（产品号，仓库号，数量）


       方法二：

在n端实体集中增加新属性，新属性由联系对应的1端实体集的码和联系自身的属性构成，新增属性后原关系的码不变。

          仓库（仓库号，地点，面积）      
    
          产品（产品号，产品名，价格，仓库号，数量）
## m:n联系的转换方法

<img src="https://img-blog.csdnimg.cn/20210411150311547.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNzA2MzMx,size_16,color_FFFFFF,t_70" alt="img" style="zoom:33%;" />

转换方法为：

与该联系相连的各实体集的码以及联系本身的属性均转换为关系的属性，新关系的码为两个相连实体码的组合（该码为多属性构成的组合码）。

          转换的关系模型为：
    
          学生（学号，姓名，年龄，性别）
    
          课程（课程号，课程名，学时数）
    
          选修（学号，课程号，成绩）
## 三个或三个以上实体集间的多元联系的转换方法

1. **对于一对多的联系**

<img src="https://img-blog.csdnimg.cn/20210411150422387.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNzA2MzMx,size_16,color_FFFFFF,t_70" alt="img" style="zoom:33%;" />

课程（课程号，课程名，学分，学时）

教师（教师号，教师名，性别，职称，课程号）

参考书（书号，书名，出版社，主编，课程号）

2. **对于多对多的联系**

<img src="https://img-blog.csdnimg.cn/20210411150554866.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQxNzA2MzMx,size_16,color_FFFFFF,t_70" alt="img" style="zoom:33%;" />

供应商（供应商号，供应商名，地址）

零件（零件号，零件名，单价）

产品（产品号，产品名，型号）

供应（供应商号，零件号，产品号，数量）




