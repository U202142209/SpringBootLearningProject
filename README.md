# 这是一个最简单的spring boot项目
## 1. 项目说明
由于有小伙伴们反馈新建spring boot工程的时候遇到了一点问题，因此出现了这个仓库

本仓库是一个最简单的spring boot工程，只有一个启动引导类和返回hello world的视图，适合作为spring boot的模板工程，如果您在新建工程的时候遇到了问题，可以直接clone这个仓库，直接在这份代码上面开启你的创作
## 2. 怎么把maven项目变成spring boot项目
1. 在 ```pom.xml``` 文件里面引入spring boot的依赖
```xml
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.7.1</version>
    </parent>
    
    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
    </dependencies>
```
2. 在src/main/java/com.zhao模块下编写spring boot的启动引导类（类的名字可以不相同）
```java
package com.zhao;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class HelloWorldSpringApplication {
    public static void main(String[] args) {
        SpringApplication.run(HelloWorldSpringApplication.class, args);

    }
}
```
3. 在启动引导类的同目录下创建controller的包，在controller包下面新建控制类，比如下面的代码可以返回hello world
```java
package com.zhao.Controller;

import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloWorldController {
    @RequestMapping("/hello")
    public String hello(String name){
        return "hello spring boot";
    }
}
```

## 3. 怎么启动项目
在IntelliJ IDEA 里面直接运行启动引导类即可
## 4. 获取帮助
```text
 @author: 我不是大佬 
 @contact: 2869210303@qq.com
 @wx; safeseaa
 @qq; 2869210303
 @time: 2023/9/30 16:45
```
也可以 [点击这里](https://www.bilibili.com/video/BV17h4y1T7Nx/) 查看超详细同步视频讲解