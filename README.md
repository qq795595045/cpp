# 📘 C++ 核心编程与工程实践笔记库

> 专注于现代 C++、STL 标准模板库与多线程并发编程的高密速查手册与系统化知识库。

---

## 🚀 知识库导航 · 在线极速直达 (点击直接阅读)

由于 GitHub 仓库直接点击 `.html` 文件默认展示 HTML 源码，推荐通过以下两种方式**直接在浏览器中免下载交互阅读**：

| 文档名称 | 🌐 在线交互阅读 (推荐·免配置) | ⚡ GitHub Pages 在线阅读 (需开启) | 📄 仓库源码 |
| :--- | :--- | :--- | :--- |
| **C++ 提高编程 · 模板与常用容器语法全貌手册** | [👉 点击直接阅读手册](https://htmlpreview.github.io/?https://github.com/qq795595045/cpp/blob/main/cpp_advanced_programming.html) | [⚡ Pages 站点阅读](https://qq795595045.github.io/cpp/cpp_advanced_programming.html) | [查看源文件](./cpp_advanced_programming.html) |
| **C++ 现代多线程与并发编程笔记** | [👉 点击直接阅读笔记](https://htmlpreview.github.io/?https://github.com/qq795595045/cpp/blob/main/cpp_multithreading_guide.html) | [⚡ Pages 站点阅读](https://qq795595045.github.io/cpp/cpp_multithreading_guide.html) | [查看源文件](./cpp_multithreading_guide.html) |

---

## 📑 核心知识点全景索引目录

### 📂 模块一：C++ 提高编程 · 模板机制与常用容器速查
> 对应文件：[`cpp_advanced_programming.html`](./cpp_advanced_programming.html)
> 在线直达：[点击免下载直接阅读](https://htmlpreview.github.io/?https://github.com/qq795595045/cpp/blob/main/cpp_advanced_programming.html)

#### 1 模板机制 (Templates)
* **1.2 函数模板**
  * `1.2.1` **函数模板语法**：通用类型参数化 `template <typename T>`、显式指定与自动推导
  * `1.2.2` **函数模板注意事项**：一致推导要求、T 类型必须显式或隐式确定
  * `1.2.3` **函数模板案例**：通用选择排序 `mySort` 与数组打印 `printArray`
  * `1.2.4` **普通函数与模板区别**：隐式类型转换发生机制
  * `1.2.5` **调用规则与优先级**：普通函数优先、空模板参数列表 `<>` 强制调用模板、重载规则
  * `1.2.6` **模板局限性与全特化**：自定义类 `Person` 的具体化全特化重载 `template <>`
* **1.3 类模板**
  * `1.3.1` **类模板语法**：`template <class NameType, class AgeType>`
  * `1.3.2` **区别与默认参数**：类模板无自动类型推导、支持默认模板参数
  * `1.3.3` **成员函数创建时机**：调用阶段延迟二次实例化
  * `1.3.4` **对象做函数形参**：3 种方式（指定传入类型、参数模板化、整个类模板化）
  * `1.3.5` **类模板与继承**：基类显式指定类型 vs 派生类也为模板类
  * `1.3.6` **成员函数类外实现**：类外作用域解析与模板参数列表标准书写
  * `1.3.7` **分文件编写规范**：`.cpp` 与 `.hpp` 头文件解决方案深度解析
  * `1.3.8` **类模板与友元**：全局友元函数类内实现 vs 类外实现（提前声明与 `<>`）

#### 2 STL 初识
* **2.5 容器算法迭代器遍历**
  * `2.5.1` **内置数据类型**：标准迭代器 `begin()/end()` 与 C++11 基于范围 `for` 遍历
  * `2.5.2` **自定义数据类型**：对象实体遍历与对象指针解引用访问
  * `2.5.3` **嵌套容器遍历**：双层 vector 嵌套双重迭代器遍历

#### 3 STL 常用容器全量单行语法速查 (40+ 细分小节)
* **3.1 `std::string` 字符串容器**
  * `3.1.2` **构造函数**：默认构造、字符数组初始化、拷贝构造、重复字符初始化
  * `3.1.3` **赋值操作**：`operator=`、`assign()` 多种赋值方式
  * `3.1.4` **字符串拼接**：`operator+=`、`append()` 追加
  * `3.1.5` **查找与替换**：`find()`、`rfind()`、`replace()`
  * `3.1.6` **字符串比较**：`compare()` 基于 ASCII 逐字符比对
  * `3.1.7` **字符存取**：`operator[]`、`at()` 安全边界访问
  * `3.1.8` **插入与删除**：`insert()`、`erase()`
  * `3.1.9` **子串与底层接口**：`substr()`、兼容底层 C 接口 `c_str()`
* **3.2 `std::vector` 动态数组容器**
  * `3.2.2` **构造函数**：区间构造、指定大小初始化、拷贝构造
  * `3.2.3` **赋值操作**：等号重载、`assign()`
  * `3.2.4` **容量和大小**：`empty()`、`capacity()`、`size()`、`resize()` 动态伸缩
  * `3.2.5` **插入和删除**：尾部增删 `push_back`/`pop_back`、迭代器插入与删除 `insert`/`erase`、`clear()`
  * `3.2.6` **数据存取**：`at()`、`operator[]`、首尾元素 `front()`/`back()`
  * `3.2.7` **互换容器**：`swap()` 及匿名对象 `vector<T>(v).swap(v)` 强制收缩内存经典语法
  * `3.2.8` **预留空间**：`reserve()` 杜绝频繁动态扩容
* **3.3 `std::deque` 双端队列容器**
  * 中控器与分段连续缓冲区原理、双端增删 `push_front`/`pop_front`、支持随机访问、全局 `std::sort` 排序
* **3.4 `std::stack` 栈适配器 (LIFO)**
  * 后进先出特性、`push()`、`pop()`、`top()`、无迭代器
* **3.5 `std::queue` 队列适配器 (FIFO)**
  * 先进先出特性、`push()`、`pop()`、`front()`、`back()`、无迭代器
* **3.6 `std::list` 双向链表容器**
  * 双向循环链表、常数时间任意节点插入删除、`remove()` 按值移除、`reverse()`、成员函数专用归并排序 `sort()` 与谓词比较器
* **3.7 `std::set` / `std::multiset` 集合容器**
  * 底层红黑树自平衡二叉树、`insert` 判定元组 `pair<iterator, bool>`、二分查找 $O(\log n)$、仿函数自定义降序比较器
* **3.8 `std::pair` 对组工具函数**
  * 构造函数创建、`std::make_pair()` 模板自动推导、公有成员 `first`/`second`
* **3.9 `std::map` / `std::multimap` 映射容器**
  * 键值对红黑树、4 种插入语法、`operator[]` 自动默认值陷阱防范与安全 `find()`、自定义键排序仿函数

#### 4 容器全景对比与选型指南
* 8 大常用容器的时间复杂度（增删查改）、底层数据结构、迭代器支持等级全景对照表

---

### 📂 模块二：C++ 现代多线程与并发编程
> 对应文件：[`cpp_multithreading_guide.html`](./cpp_multithreading_guide.html)
> 在线直达：[点击免下载直接阅读](https://htmlpreview.github.io/?https://github.com/qq795595045/cpp/blob/main/cpp_multithreading_guide.html)

* **一、多线程核心概念与生命周期**
  * 线程与进程的区别、并发与并行
  * `std::thread` 构造与参数传递机制（值传递、`std::ref` 引用传递、移动语义）
  * `join()` 阻塞主线程等待 vs `detach()` 后台守护线程
* **二、面向对象与 ROS2 节点类内多线程**
  * 类成员函数作为线程入口函数的规范写法
  * Lambda 表达式捕获 `[this]` 优雅实现异步并发
  * 线程对象的生命周期与 RAII 资源回收
* **三、工程实战：机器人速度差监控与异常检测**
  * 队列缓存与时序差值计算
  * `checkSpeedChange(current, previous)` 工作线程异步封装
  * 线程等待与安全合并实战

---

## ⚡ 30 秒开启 GitHub Pages (建议开通)

若想拥有专属的在线网站域名（例如 `https://qq795595045.github.io/cpp/`），只需在 GitHub 上点两下：

1. 进入仓库页面：[https://github.com/qq795595045/cpp](https://github.com/qq795595045/cpp)
2. 点击顶部导航的 **Settings**（设置）
3. 在左侧菜单中找到并点击 **Pages**
4. 在 **Build and deployment** 下方的 **Branch** 下拉框中：
   - 选择 **`main`** 分支，目录保持 **`/ (root)`**
   - 点击 **Save**（保存）
5. 等待 30 秒刷新，即可获得永久官方在线阅读站点！
