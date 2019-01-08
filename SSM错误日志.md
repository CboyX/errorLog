1. ## 启动SSM项目时，mybatis的sql映射文件出现相同id导致如下错误：（本次错误是因为EmployeeMapper.XML文件中 的id = BaseResultMap出现了重复）

```java
Caused by: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'sqlSessionFactory' defined in class path resource [applicationContext.xml]: Invocation of init method failed; nested exception is org.springframework.core.NestedIOException: Failed to parse mapping resource: 'file [D:\workSpace\test\target\classes\mapper\EmployeeMapper.xml]'; nested exception is org.apache.ibatis.builder.BuilderException: Error parsing Mapper XML. Cause: java.lang.IllegalArgumentException: Result Maps collection already contains value for com.hand.ssm.dao.EmployeeMapper.BaseResultMap

```

## 解决办法:

去EmployeeMapper.XML文件中将多余的id=BaseResultMap的resultMap去掉即可。

