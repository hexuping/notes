* 父工程依赖管理

```java
	<dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>org.springframework.cloud</groupId>
                <artifactId>spring-cloud-dependencies</artifactId>
                <version>Greenwich.SR3</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
            <dependency>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-dependencies</artifactId>
                <version>2.1.9.RELEASE</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
            <dependency>
                <groupId>com.alibaba.cloud</groupId>
                <artifactId>spring-cloud-alibaba-dependencies</artifactId>
                <version>2.1.2.RELEASE</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
        </dependencies>
    </dependencyManagement>
```

```java
<!--引入依赖，将外部依赖引入项目进行管理，后续使用相关依赖可不填写版本信息，默认使用引入的依赖版本-->
<type>pom</type>

<scope>import</scope>
```

```java
<!--依赖传递 默认依赖传递 true-依赖不传递-->
<optional>true</optional>
```

```java
<!--指定依赖作用范围 test-只在测试文件夹下有效-->
<scope>test</scope>
```



继承依赖

子模块继承父模块的依赖,使用父模块依赖管理中的依赖不用指定版本，默认使用依赖管理中的版本