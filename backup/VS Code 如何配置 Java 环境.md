

## 一 下载并安装 JDK

1 打开 OpenJDK 官方网站
 https://jdk.java.net/

2 找到当前长期支持版本，通常为 JDK 17
 在页面中选择 Windows x64 的压缩包 zip

3 下载后将 zip 文件解压到任意位置
 推荐路径
 C:/Program Files/OpenJDK/jdk-17



------

## 二 配置系统环境变量

确保系统能正确找到 Java 编译器和运行环境

### 1 打开环境变量管理

Windows 搜索栏输入
 环境变量
 进入系统属性→环境变量

### 2 创建 JAVA_HOME

系统变量→新建
 变量名
 JAVA_HOME
 变量值
 C:/Program Files/OpenJDK/jdk-17 (此处为你的JDK路径)

### 3 修改 Path

系统变量中找到 Path → 编辑
 新增一行
 %JAVA_HOME%/bin

### 4 验证环境变量

打开终端输入
 java -version
 成功显示版本号说明配置完成

------

## 三 安装 VS Code 扩展

1 打开 VS Code
 2 进入扩展
 3 搜索 Extension Pack for Java
 4 点击安装
 它会自动安装 Java 开发所需组件
 （包括调试器、语言支持、项目管理等）

------

## 四 让 VS Code 使用 OpenJDK

若 VS Code 没自动识别 JAVA_HOME，可手动指定

1 按 Ctrl Shift P
 2 搜索 settings.json
 3 打开用户设置文件
 4 添加配置

"java.home": "C:/Program Files/OpenJDK/jdk-17" （此处为你的JDK路径）

保存后 VS Code 会重新加载 Java 环境

------

## 五 测试你的环境

1 新建文件夹作为项目
 2 创建 HelloWorld.java
 3 输入以下代码

```
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

4 点右上角运行
 看到输出 Hello Java 表示环境已完全搭建成功