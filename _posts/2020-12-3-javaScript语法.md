---
layout: page
title:  "javaScript"
subtitle: "菜鸟教程"
date:   2020-12-05 21:21:21 +0530
categories: javaScript知识点
---

# js环境

  -  什么是JavaScript环境？


# js基本语法

  - 定义一个变量： var a = 0
  - 定义一个数组:  var a = []
  - 定义一个函数： var a = function(){}
  - 定义一个对象： var a = {}
  // 当对象中属性名为变量的时候用，取值的时候应用[]
# js 数组和对象
  - 相同点
    - 都是复合类型
    - 都是由键值对组成
    - 值都是任意数据类型
  - 不同点
    - 键的类型
      - 数组的键是0 1 2 3 4 5 ...有序的数字
      - 对象的键是无序的字符串
    - 表示的事物
      - 相同种类的事物用数组
      - 描述一个事物用对象
    - 是否有序
      - 数组因为键是有序的，所以可以表示有序的事物
      - 对象不存在顺序   
```javascript
  // 数组
  var arr = ["apple", "pear", "peach", "banana"]
  // 增
  arr[4] = "watermelon"
  // 删
  // 改
  arr[2] = "mango"
  // 查
  var temp = arr[2]
  console.log(temp)
  // 遍历
  for (var i = 0; i < arr.length; i++){
    console.log(arr[i])
  }

  // 对象
  var obj = {
    hair_color: "green",
    height: 150,
    weight: 200,
    three_size: [90,90,90]
    nickName: "煤气罐成精"
  }
  // 增
  obj.age = 20
  // 删
  delete obj.nickName;
  // 改
  obj.three_size = [80,60,90]
  // 查
  var temp = obj.height

  // 遍历(如果你的键是一个变量 那么 就要用[])
  for (var i in obj) {
    console.log(obj[i])
  }

```
# js对数组元素进行增删改移的函数
  - push() 在原来数组中的元素最后面添加元素  
  - unshift() 在原来数组中的元素最前面添加元素 
  - pop() 移除数组中最后面的一个元素
  - shift() 移除数组中最前面一个元素
  - concat() 拼接两个数组中的元素(哪个数组在前面，拼接后它的元素就在前面)
  - join("") 把数组转换为字符串(将数组中的元素通过特殊符号链接成字符串)

# JavaScript中var命令、let命令、const命令详解
  - var命令
    - var声明的是去全局变量，其作用域为所在的函数内
    - var命令可以在声明之前使用
  - let命令
    - let命令声明的变量是局部变量，该变量只会在最靠近{}内的范围有效
    - let命令声明的变量只在它所在的代码块有效
    - let命令不允许在相同作用域内，重复声明同一个变量
  - const命令
    - const声明一个只读的常量，一旦声明，常量的值就不能改变
    - const声明的常量，不可重复声明

# 变量的本质
  - 变量名的本质是地址
  - 内存的最小储存单位是字节
  - 一字节等于八个二进制位数字
    - 数据基础
       - 程序由数据构成
       - 数据存放于内存
       - 存放数据的内存起名叫变量名
       - 存放在内存中的数据叫做变量值
          - 数据有很多种类型，叫做数据类型
       - 两个加起来叫做变量

      - 变量存于栈内存
      - 常量存于数据段
      - 对象数组存于堆

# 原型链

- new的本质与封装
    - 声明一个空对象（obj）
    - 将该函数中的prototype属性浅复制到obj中，用以记录obj是哪个函数实例化来的 //prototype属性在函数中
    - 将该函数中的this指向要改为OBJ
    - 执行该函数
    - 返回obj

- 对象
    - 类似于PHP一样，JS的对象也是new出来的
    - 对象 - new - 类
    - 本质上就是存放地址

- this指向
    - 当前代码的运行环境【上下文】
    - this数据类型是永远是对象
    - 声明时已经奠定this指向位置,this指向是调用时才可知道的，谁调用的this那么就指向谁
    - 箭头函数(=>)为了统一this指向，就是调整this指向(例如：var that = this)

- 变量的存储
    - 定义一个变量，计算机会为这个变量分配一个地址存于内存中，如果存于内存中的是一个固定的值，就是值类型，如果存储的是一个地址那就是引用类型;简单概括就是变量中存的是值就是值类型，存的是地址就是引用类型
    - 值类型：
        - a = 10
            - 变量a实际上是个地址，计算机根据a的地址寻找到储存了10【值】的位置
    - 引用类型（对象、数组、函数）
        - a = {b : 10};  c = b; c.b + 1; console.log(a) a = 11; 
            - 计算机实际上是首先根据a的地址寻找到a的存放位置，在里面找到地址b，然后再通过b寻找到b对应的位置，取得值10
        - 浅复制
            - 地址之间的传递。
        - 深复制
            - 值的复制

  - 原型链是一种继承的方式
  
  - 继承的根本原因就是节约内存

# 获取DOM元素
  - getElementById('id名称')
    - 查找一个元素，返回 id 匹配的元素(一个)

  - getElementsByTagName('标签名')
    - 获取标签名匹配的元素，返回一个数组(数组的常用方法用不了)

  - getElementsByClassName('类名')
    - 获取类名匹配的元素，返回一个数组(数组的常用方法用不了)

  - getElementsByName('元素name属性的值')
    - 获取元素的 name 属性的值匹配的元素，返回一个数组(数组的常用方法用不了)

  - querySelector('选择器')
    - 获取选择器所匹配的第一个元素，返回选择器匹配的元素(一个)

  - querySelectorAll('选择器')
    - 获取选择器所匹配的所有元素，返回一个数组(数组的常用方法用不了)
    
#  DOM节点分类
  - document(根节点)
    - 一个页面中最大的节点，不属于元素
  - html(根元素节点)
    - 一个页面中最大的元素节点
  - 元素节点
    - 就是页面的标签，例如：head/body/div....等
  - 文本节点
    - 页面中每一个文本内容(包含换行、空格)
    - 一般作为元素节点的子节点存在
  - 属性节点
    - 属性节点不作为独立节点出现，必须依赖元素
# DOM节点操作

  ## DOM获取节点

  - childNodes
    - 返回元素的所有子节点，数组(常用方法不可用)

  - children
    - 返回元素的所有子元素节点，数组(常用方法不可用)

  - firstChild
    - 返回元素的第一个子节点

  - firstElementChild
    - 返回元素的第一个子元素节点

  - lastChild
    - 返回元素的最后一个子节点

  - lastElementChild
    - 返回元素的最后一个子元素节点

  - previousSibling
    - 返回元素的上一个兄弟节点

  - previousElementSibling
    - 返回元素的上一个兄弟元素节点

  - nextSibling
    - 返回元素的下一个兄弟节点

  - nextElementSibling
    - 返回元素的下一个兄弟元素节点
    
  - parentNode
    - 返回元素的父节点

  - parentElement
    - 返回元素的父元素节点

  - attributes
    - 返回元素的所有属性节点 

  ## DOM节点的创建(增)
  - createElement('标签名')
    - 返回一个元素节点

  - createTextNode('文本内容')
    - 返回一个文本节点, 不是字符串

  - createAttribute('属性名')
    - 返回一个属性节点

  ## DOM节点的插入和替换
  - appendChild()
    - 使用：父节点.appendChild(子节点)
    - 把子节点插入到父节点里面, 放在最后一个节点的位置

  - insertBefore()
    - 使用: 父节点.innserBefore(要插入的子节点, 哪一个子节点前面)
    - 把子节点插入到指定父节点的指定子节点前面

  - replaceChild()
    - 使用: 父节点.replaceChild(新节点, 旧节点)
    - 在父节点下, 用新节点替换旧节点
    
  ## DOM节点的删除
  - removeChild()
    - 使用: 父节点.removeChild(子节点)
    - 把子节点从父节点里面移出

  - remove()
    - 使用: 节点.remove()
    - 把自己移出父节点

# 错误error
- 常见的内置错误
  - 未捕获error的话，错误后面代码不执行
  - Error: 所有错误的父类型
  - RenferenceError：引用的变量不存在

    - 例如：console.log(a)  ReferenceError: a is not defined

  - TypeError: 数据类型不正确的错误

    - 例如： let b; console.log(b.abc)  TypeError: Cannot read property "abc" of undifined
    - 例如：let b = {}; console.log(b.abc()) TypeError: b.abc is not a function

  - RangeError: 数据值不在其范围所允许的范围内

    - 例如：function fun() { fun() } fun() RangeError: Maximun call stack size exceeded

  - SyntaxError: 语法错误
    - 例如：const c = " SynatxError: Unexpected string

- 错误处理
  - 捕获错误： try{  }catch(error){}
    - 错误对象error：形参error是一个对象，里面有两个属性 message 和 stack
    - message属性：错误相关信息
    - stack属性： 函数调用栈记录信息
  - 抛出错误： throw new Error("错误")

# Promise技术
  - 抽象表达Promise是什么
    - Promise是 JS 中进行异步编程的新的解决方案
  - 具体表达Promise是什么
    - 语法上： 是一个构造函数(被实例化的函数)
    - 功能上： promise队形用来封装异步操作并可以获取其结果

  - Promise的状态及其变化
    - pending 未判定的
    - resolved 成功的
    - rejected 拒绝的
    - 说明： 只有这三种状态，初始状态是pending，所以Promise只有两种变化，且一个Promise对象只能改变一次，且都会返回结果数据
  - Promise的基本使用
    ```
      var a = new Promise((resolve, reject) => {
        
        const time = date()
        setTimeout(() => {
          if (time%2 === 0) {
            resolve("成功的数据,time =" + time)
          }else {
            reject("失败的数据,time =" +time)
          }
        },1000);
      })

      a.then( value => {console.log("成功的回调", value)},reason => {console.log("失败的回调", reason)})
    ```
  - Promise的优势
    - 指定回调函数的方式更为灵活
    - 支持链式调用，可以解决回调地狱(回调嵌套，后一个回调函数的条件为前一个回调函数的结果，不便于维护、阅读和异常处理，且代码较臃肿)；解决方案：Promise的链式调用，终极解决方案：async/await