## css reset 是什么？css 预编译器是什么？ 后编译器(post css)是什么

1. HTML标签在浏览器中都有默认的样式，不同的浏览器的默认样式之间存在差别,  
开发时浏览器的默认样式可能会给我们带来多浏览器兼容性问题，影响开发效率,因此一开始就将浏览器的默认样式全部覆盖掉，这就是css reset.      
 
2. CSS 预编译器基于 CSS 扩展了一套属于自己的 DSL，来解决书写 CSS 时难以解决的问题：    
   (1)语法不够强大，比如无法嵌套书写导致模块化开发中需要书写很多重复的选择器；   
   (2)没有变量和合理的样式复用机制，使得逻辑上相关的属性值必须以字面量的形式重复输出，导致难以维护。   
   所以这就决定了 CSS 预处理器的主要目标：提供 CSS 缺失的样式层复用机制、减少冗余代码，提高样式代码的可维护性。  
   
慕课： https://www.imooc.com/code/5993
CSS 预编译器定义了一种新的语言，其基本思想是，用一种专门的编程语言，为 CSS 增加了一些编程的特性，将 CSS 作为目标生成文件，然后开发者就只要使用这种语言进行编码工作。   
通俗的说，“CSS 预处理器用一种专门的编程语言，进行 Web 页面样式设计，然后再编译成正常的 CSS 文件，以供项目使用。CSS 预处理器为 CSS 增加一些编程的特性，无需考虑浏览器的兼容性问题”，   
例如你可以在 CSS 中使用变量、简单的逻辑程序、函数（如右侧代码编辑器中就使用了变量$color）等等在编程语言中的一些基本特性，可以让你的 CSS 更加简洁、适应性更强、可读性更佳，更易于代码的维护等诸多好处。   
   CSS 预处理器语言，比如说：
   Sass（SCSS）  
   LESS   
   Stylus   
   Turbine   
   Swithch CSS  
   CSS Cacheer  
   DT CSS  
3. 后编译器     
CSS 后编译器 是对 CSS 进行处理，并最终生成 CSS 的 预处理器，它属于广义上的 CSS 预处理器。   
后编译器通常被视为在完成的样式表中根据CSS规范处理CSS，让其更有效；目前最常做的是给CSS属性添加浏览器私有前缀，实现跨浏览器兼容性的问题。  
 
 



