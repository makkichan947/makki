# Makki - Compiler Frontend

Makki 是 Makki 编程语言的编译器前端项目，包含语言规范、示例代码和标准库定义。

## 特性

- **语言规范** - 完整的 Makki 编程语言语法和语义说明
- **示例代码** - 丰富的示例代码，展示语言特性
- **标准库** - Makki 标准库定义和头文件
- **快速开始** - 帮助开发者快速上手 Makki 编程

## 项目结构

```
makki/
├── examples/          # 示例代码
│   ├── hello/        # Hello World 示例
│   ├── concurrency/  # 协程和通道示例
│   └── generic_struct/ # 泛型结构体示例
├── .gitignore
└── .gitattributes
```

## 快速开始

### 安装编译器

首先需要安装 [mlang 编译器](https://github.com/makki-lang/mlang)。

```bash
cd mlang
make
```

### 编写第一个程序

创建 `hello.m4` 文件：

```makki
function main()
    println("Hello, Makki!");
end function;
```

### 编译运行

```bash
# 使用 mlang 编译器编译
mlang hello.m4 -o hello

# 运行程序
./hello
```

## 语言特性

### 基础语法

```makki
// 变量声明
var x: i32 = 42;
var y := 3.14;  // 类型推导

// 函数定义
function add(a: i32, b: i32) -> i32
    return a + b;
end function;
```

### 协程和通道

```makki
// 启动协程
go worker();

// 创建通道
var ch: chan i32 = make(chan i32);

// 发送和接收
ch <- 42;
var val := <-ch;
```

### 泛型结构体

```makki
struct List<T>
    var data: T*;
    var len: i32;
end struct;

function newList<T>() -> List<T>
    // ...
end function;
```

## 示例代码

更多示例请查看 [examples/](./examples/) 目录：

- [hello/](./examples/hello/) - Hello World 基础示例
- [concurrency/](./examples/concurrency/) - 协程和通道并发编程
- [generic_struct/](./examples/generic_struct/) - 泛型结构体使用

## 相关项目

- [mlang](https://github.com/makki-lang/mlang) - Makki 语言编译器本体
- [makki-vscode-extension](https://github.com/makki-lang/makki-vscode-extension) - VSCode 语言扩展

## 作者

Yaku Makki
