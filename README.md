# ES6
ES6基础(新特新)

新特性

                let、const
                let 定义的变量不会被变量提升，const 定义的常量不能被修改，let 和 const 都是块级作用域


ES6前，js 是没有块级作用域 {} 的概念的。（有函数作用域、全局作用域、eval作用域）
ES6后，let 和 const 的出现，js 也有了块级作用域的概念，前端的知识是日新月异的~
变量提升：在ES6以前，var关键字声明变量。无论声明在何处，都会被视为声明在函数的最顶部；不在函数内即在全局作用域的最顶部。

 例如：
 
                 console.log(a);  // undefined
                  var a = 'hello';

                  # 上面的代码相当于
                  var a;
                  console.log(a);
                  a = 'hello';

                  # 而 let 就不会被变量提升
                  console.log(a); // a is not defined
                  let a = 'hello';

 
 
 
 
 





