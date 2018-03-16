# ssm-project-frame
# 介绍
    针对于SpringMVC+Spring+Mybatis的一条线的梳理框架搭建到最后的调试通过，完事之后感觉还是很简单的，但是在过程中也遇到了一些小小的坎坷~
# 环境要求
    jdk1.8
    maven3.2.3
    当然可以在我的这个版本的基础上进行合理调整
# 框架介绍
e3-parent：父工程，打包方式pom，管理jar包的版本号。
    |           项目中所有工程都应该继承父工程。
    |--e3-common：通用的工具类通用的pojo。打包方式jar
    |--e3-manager：服务层工程。聚合工程。Pom工程
      |--e3-manager-dao：打包方式jar
      |--e3-manager-pojo：打包方式jar
      |--e3-manager-interface：打包方式jar
      |--e3-manager-service：打包方式：jar
      |--e3-manager-web：表现层工程。打包方式war
# 步骤
    1.将代码下载下来，导入自己的编译器中~
    2.将其中的e3mall.sql导入到mysql数据库中
    3.通过配置maven进行项目中依赖的jar，将其下载到自己的本地仓库
    4.配置一个tomcat将e3-manager-web配置到tomcat中进行启动就可以看到页面了
# 测试访问
    http://localhost:8080/item/123
    注：123是TbItem中随便一个主键id的值
# 遇到的坑
    这个框架没有加入日志，所以，在到service的实现层中调用的时候，可能因为数据库的账号密码错误导致没反应~
    本次版本已经加入日志，如果有问题会有相关日志输出
