# Overview

# 术语

JDK：Java Development kit，java开发组件，包括编译和运行java程序

JRE：Java Runtime Environment，java运行环境，只包括运行java的环境

javac：java程序编译器，用于将java源代码编译成程序

java：java运行时命令，用于运行编译后的java程序

javadoc：用于生成java的文档

jar：Java Archive。用于创建和管理jar。JAVA归档，表示把多个Java相关文件（.class 图像 声音等等）打包合成一个文件。内部会自动生成一个manifest文件存储详情单信息。可以需要的库和和部署资源打包，直接在编译器和JVM上使用。

JVM：JAVA Virtual Machine。使用java编译器编译java程序时，生成的是字节码（test.class 类文件，或字节码文件，包含JVM指令集、符号表及补充信息），可以在虚拟机上执行。class文件不会与机器的操作系统相对应，而是与虚拟机JVM对应，虚拟机解释给本地的操作系统执行。

# 安装

```bash
sudo apt install openjdk-11-jdk
# 或
sudo apt install openjdk-11-jre
```

# 环境变量

```bash
JAVA_HOME：jdk/jre的安装目录，例如：/usr/lib/jvm/java-11-openjdk-amd64
PATH：用于指出java和javac程序所在
CLASSPATH：指定了Java类文件和库的搜索路径，通常情况下不需要设置全局的CLASSPATH，而是再运行java程序的时候通过命令行参数-cp/-classpath指定
```

# example

```java
# HelloWorld.java

public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

```bash
javac HekkoWorld.java # 改命令会在源码同目录下，生成HelloWorld.class文件

# 设置CLASSPATH
export CLASSPATH=$(pwd)

# 默认会在当前路径查找。如果不设置CLASSPATH，则可能找不到非当前路径的java程序
java HelloWorld
```

# JAR example
