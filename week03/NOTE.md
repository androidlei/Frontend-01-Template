# 每周总结可以写在这里

Skip to content
 
Search or jump to…

Pull requests
Issues
Marketplace
Explore
 
@androidlei 
yangdengcheng
/
Frontend-01-Template
forked from GeekUniversity/Frontend-01-Template
0
0 871
 Code
 Pull requests 0  Actions
 Projects 0
 Wiki
 Security 0
 Insights
Frontend-01-Template/week03/NOTE.md 
Newer           Older
 100644  205 lines (145 sloc)  6.33 KB
### Javascript语句

- Atom
- Expression
- Statement
- Structure
- Program/Module

#### Grammar
##### 简单语句
- Expression Statement 表达式语句
    - a = 1 + 2;

- Empty Statement 空语句
    - ;
- Debugger Statement debugger语句，运行时不产生作用
    - debugger;

- ThrowStatement
    - throw a;
- Continue Statement(与循环相互匹配)
    - continue label1;
- Break Statement(与循环匹配)
    - break label2;
- Return Statement
    - return; / return 1;

##### 组合语句
- Block Statement
```
{
...
...
}
```
- Iteration
```
while()
do...while
for
for...in...
for...of...
```
##### 声明
- FunctionDeclaration
- GeneratorDeclaration
- AsyncFunctionDeclaration
- AsyncGeneratorDeclaration
- VariableStatemeny
- ClassDeclaration
- LexicalDeclaration


##### 标签、循环、break、continue
- LabelledStatement
- IterationStatement
- ContinueStatement
- BreakStatement
- SwitchStatement

#### Runtime：
- Complection Record
    - [[type]]: normal, break, continue, return, throw
    - [[value]]: Types
    - [[target]]: label
- Lexical Enviorment

### Javascript对象机制

#### Object

- 任何一个对象都是唯一的，这与它本身的状态无关。

- 即使状态完全一致的两个对象。也并不相等。

- 我们用状态来描述对象。

- 状态的改变即是行为。

- 标示性（Identifier）指针（state）行为（behavior）

#### 基于类的面向对象

- 类是一种常见的描述对象的方式。而“归类”和“分类”则是两个主要的流派。

- 对于“归类”方法而言，多继承是非常自然的事情。如C++。

- 而采用分类思想的计算机语言，则是单继承结构。并且会有一个基类Object。

- 原型是一种更接近人类原始认知的描述对象的方法。

- 我们并不试图做严谨的分类，而是采用“相似”这样的方式去描述对象。

- 任何对象仅仅需要描述它自己与原型的区别即可。

#### Object in Javascript

- 在Javascript运行时，原生对象的描述方式非常简单。我们只需要关心原型和属性两个部分。

- 它的原型实际上就是一个KV对。

- Javascript用属性来统一抽象对象状态和行为。

- 一般来说，数据属性用于描述状态，访问器属性则用于描述行为。

- 数据属性中如果存储函数，也可以用于描述行为。



### Javascript中的对象

#### 基本对象

基本对象是定义或使用其他对象的基础。基本对象包括一般对象、函数对象和错误对象。

##### 一般对象、函数对象

- Object
- Function
- Boolean
- Symbol

##### 错误对象

错误对象是一种特殊的基本对象。它们拥有基本的 Error 类型，同时也有多种具体的错误类型。

- Error（通过Error的构造器可以创建一个错误对象。当运行时错误产生时，Error的实例对象会被抛出。Error对象也可用于用户自定义的异常的基础对象。）

```
new Error([message[, fileName[,lineNumber]]])
```

- AggregateError
- EvalError
- RangeError(标明一个错误，当一个值不在其所允许的范围或者集合中。)
- ReferenceError(代表当一个不存在的变量被引用时发生的错误。)
- SyntaxError(对象代表尝试解析语法上不合法的代码的错误。)
- TypeError(对象用来表示值的类型非预期类型时发生的错误。

语法)
- URLError(URIError 对象用来表示以一种错误的方式使用全局URI处理函数而产生的错误。)

#### 数字和日期对象

用来表示数字、日期和执行数学计算的对象。

- Number
- BigInt(它提供了一种方法来表示大于 253 - 1 的整数。这原本是 Javascript中可以用 Number 表示的最大数字。BigInt 可以表示任意大的整数。)
- Math
- Date

#### 字符串

用来表示和操作字符串的对象。

- String
- RegExp

#### 可索引的集合对象

表示按照索引值来排序的数据集合，包括数组和类型数组，以及类数组结构的对象。

- Array
- Int8Array(表示二进制补码8位有符号整数的数组。内容初始化为0。 一旦建立，你可以使用对象的方法引用数组中的元素，或使用标准数组索引语法( 即，使用括号注释)。)
- Uint8Array(表示一个8位无符号整型数组，创建时内容被初始化为0。创建完后，可以以对象的方式或使用数组下标索引的方式引用数组中的元素。)
- Uint8ClampedArray(（8位无符号整型固定数组） 类型化数组表示一个由值固定在0-255区间的8位无符号整型组成的数组；如果你指定一个在 [0,255] 区间外的值，它将被替换为0或255；如果你指定一个非整数，那么它将被设置为最接近它的整数。（数组）内容被初始化为0。一旦（数组）被创建，你可以使用对象的方法引用数组里的元素，或使用标准的数组索引语法（即使用方括号标记）。)
- Int16Array
- Uint16Array
- Int32Array
- Uint32Array
- Float32Array
- Float64Array
- BigInt64Array
- BigUint64Array

#### 使用键的集合对象

这些集合对象在存储数据时会使用到键，包括可迭代的Map 和 Set，支持按照插入顺序来迭代元素。

- Map
- Set
- WeakMap（一组键/值对的集合，其中的键是弱引用的。）
- WeakSet（对象允许你将弱保持对象存储在一个集合中。）

#### 结构化语句

这些对象用来表示和操作结构化的缓冲区数据，或使用 JSON （JavaScript Object Notation）编码的数据。

- ArrayBuffer（表示通用的、固定长度的原始二进制数据缓冲区。它是一个字节数组，你不能直接操作 ArrayBuffer 的内容，而是要通过类型数组对象或 DataView 对象来操作，它们会将缓冲区中的数据表示为特定的格式，并通过这些格式来读写缓冲区的内容。）
- DataView（视图是一个可以从 二进制ArrayBuffer 对象中读写多种数值类型的底层接口，使用它时，不用考虑不同平台的字节序问题。）
- JSON

#### 控制抽象对象

- Promise
- Generator
- GeneratorFunction
- AsyncFunction
- Iterator
- AsyncIterator

#### 反射

- Reflect（它提供拦截 JavaScript 操作的方法。这些方法与proxy handlers的方法相同。Reflect不是一个函数对象，因此它是不可构造的。）
- Proxy（用于定义基本操作的自定义行为（如属性查找、赋值、枚举、函数调用等））

