# MyDailyRecord
# 1. log4j 2
* [log4j的引入](https://logging.apache.org/log4j/2.x/maven-artifacts.html)   
  * Maven引入
```<dependencies>
  <dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-api</artifactId>
    <version>2.5</version>
  </dependency>
  <dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-core</artifactId>
    <version>2.5</version>
  </dependency>
</dependencies>
```
* [logj的配置](https://logging.apache.org/log4j/2.x/manual/configuration.html)
  * 配置中的pattern
  ![](/Image/log4j-pattern.png)

#  2. Maven相关
* 1. 创建Maven下的Java控制台输出程序的
* 2. 创建Maven下的Scala控制台输出程序
> 第一步：创建空的maven项目
> 第二步：修改pom文件
```<dependencies>
           <dependency>
               <groupId>org.scala-lang</groupId>
               <artifactId>scala-library</artifactId>
               <version>2.11.7</version>
           </dependency>
       </dependencies>
       <build>
           <finalName>${artifactId}</finalName>
           <plugins>
               <plugin>
                   <artifactId>maven-compiler-plugin</artifactId>
                   <configuration>
                       <source>1.8</source>
                       <target>1.8</target>
                   </configuration>
               </plugin>
               <plugin>
                   <groupId>org.scala-tools</groupId>
                   <artifactId>maven-scala-plugin</artifactId>
                   <executions>
                       <execution>
                           <goals>
                               <goal>compile</goal>
                               <goal>testCompile</goal>
                           </goals>
                       </execution>
                   </executions>

               </plugin>
           </plugins>
       </build>
```
# 3. Mysql相关
可更改my-default.imi文件 或者复制一个更改里面的内容后放到bin目录下，
如果出现```Fatal error: Can't open and lock privilege tables: Table 'mysql.user' doesn't exist``` 错误：
先删除datadir中的文件
执行``mysqld --initialize --user=mysql --console``` 即可。

如果出现登陆失败，请查看服务是否启动
如未启动：请```mysqld-nt -install```（安装服务） （mysqld-nt -remove ）
启动服务：```net start mysql```

首次使用前需修改密码：````SET PASSWORD = PASSWORD('123456');````
查看mysql字符集 ```show variables like 'char%';```

# 4. android源码下载
[android源码下载](https://source.android.com/source/downloading.html)

# 5. Ubuntu相关
![](/Image/ubuntu常用快捷键.png)
# 6. IDEA注册地址
[IDEA注册地址](http://idea.lanyus.com/)

# 7. jProfiler
JProfiler是一个商业授权的Java剖析工具，由EJ技术有限公司，针对Java EE和Java SE应用程序开发的。
它允许两个内存剖面评估内存使用情况和动态分配泄漏和CPU剖析，以评估线程冲突。
JProfiler直觉式的GUI让你可以找到性能瓶颈、抓出内存漏失(memory leaks)、并解决执行绪的问题。[from 百度百科]
简而言之，它能通过评估CPU、内存以及线程来避免内存漏失，是一个性能监测工具。

[jProfiler主页](http://www.ej-technologies.com/index.html)

L-Larry_Lau@163.com#36573-fdkscp15axjj6#25257
L-Larry_Lau@163.com#7009-14frku31ynzpfr#20176
L-Larry_Lau@163.com#49604-1jfe58we9gyb6#5814
L-Larry_Lau@163.com#25531-1qcev4yintqkj#23927
L-Larry_Lau@163.com#96496-1qsu1lb1jz7g8w#23479
L-Larry_Lau@163.com#20948-11amlvg181cw0p#171159
