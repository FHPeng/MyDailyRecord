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
# 2. Maven相关
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