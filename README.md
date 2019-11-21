# JavaFirstLearning

1)建立Spring Boot 的專案

使用URL： https://start.spring.io/ 

建立完成使用VS Code開啟

PS.記得使用Maven專案

2)Maven的基本命令

```maven
mvn clean
mvn compile
mvn package
mvn spring-boot:run
```

3)VS中的基本快速鍵

```visaul studio
CTRL + E 找檔案
CTRL + SHIFT + . 開啟該檔案的Method 列表
CTRL + C 停止
```

4)撰寫第一個Controller

E:\Learn\Java\JavaFirstLearning\src\main\java\com\Danny\web\HelloController.java

```java
  
 package com.Danny.web;

import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

/**
 * HelloController
 */
@RestController
public class HelloController {

    @RequestMapping("/hello")
    public String index(){
        return "Hello World";
    }
    
}
```

Controller 和初始的main Method不同Package時需要設定如下 ComponentScan

```java
@SpringBootApplication
@ComponentScan("com.Danny.web")
public class Chapter1Application {

	public static void main(String[] args) {
		SpringApplication.run(Chapter1Application.class, args);
	}

}
```

pom.xml

```xml
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>		

```





