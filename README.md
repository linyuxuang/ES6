# ES6
ES6基础(新特新)

新特性

                let、const
                let 定义的变量不会被变量提升，const 定义的常量不能被修改，let 和 const 都是块级作用域


                ES6前，js 是没有块级作用域 {} 的概念的。（有函数作用域、全局作用域、eval作用域）
               
               ES6后，let 和 const 的出现，js 也有了块级作用域的概念，前端的知识是日新月异的~
               
               变量提升：在ES6以前，var关键字声明变量。无论声明在何处，都会被视为声明在函数的最顶部；
               不在函数内即在全局作用域的最顶部。

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

 const 定义的常量不能被修改
 
       
                var name = "bai";
                name = "ming";
                console.log(name); // ming


                const name = "bai";
                name = "ming"; // Assignment to constant variable.
                console.log(name);

        
 import、export
 import导入模块、export导出模块     
       
               // 全部导入
                import people from './example'

                // 将整个模块当作单一对象进行导入，该模块的所有导出都会作为对象的属性存在
                import * as example from "./example.js"
                console.log(example.name)
                console.log(example.getName())

                // 导入部分，引入非 default 时，使用花括号
                import {name, age} from './example'


                // 导出默认, 有且只有一个默认
                export default App

                // 部分导出
                export class App extend Component {};

class、extends、super


                 ES5中最令人头疼的的几个部分：原型、构造函数，继承，有了ES6我们不再烦恼！

                 ES6引入了Class（类）这个概念。

       
   例子1    
   
                  class Animal {
                    constructor() {
                        this.type = 'animal';
                    }
                    says(say) {
                        console.log(this.type + ' says ' + say);
                    }
                }

                let animal = new Animal();
                animal.says('hello'); //animal says hello

                class Cat extends Animal {
                    constructor() {
                        super();
                        this.type = 'cat';
                    }
                }

                let cat = new Cat();
                cat.says('hello'); //cat says hello


例子2

                    //  父类
                    class Father{
                      constructor(x,y){
                          this.x=x;
                          this.y=y;
                      }
                      mov(){
                          console.log(this.x+"----"+this.y)
                      }
                    }

                  //子继承父
                     class Son extends Father{
                         constructor(y) {
                             super();
                             this.x="ooooooooooop";
                             this.y=y;
                         }

                     }
                      var s=new Father("WWWW","LLLLL")
                        s.mov()    //WWWW----LLLLL

                      var x=new Son("ppppppppppppp")
                       x.mov()   //ooooooooooop----ppppppppppppp


                  上面代码首先用class定义了一个“类”，可以看到里面有一个constructor方法，这就是构造方法，
                  而this关键字则代表实例对象。简单地说，constructor内定义的方法和属性是实例对象自己的，
                  而constructor外定义的方法和属性则是所有实力对象可以共享的。

       
                 Class之间可以通过extends关键字实现继承，这比ES5的通过修改原型链实现继承，要清晰和方便很多。
                 上面定义了一个Cat类，该类通过extends关键字，继承了Animal类的所有属性和方法。
       
       
                 super关键字，它指代父类的实例（即父类的this对象）。
                 子类必须在constructor方法中调用super方法，否则新建实例时会报错。
                 这是因为子类没有自己的this对象，而是继承父类的this对象，
                 然后对其进行加工。如果不调用super方法，子类就得不到this对象。
       
       
                 ES6的继承机制，实质是先创造父类的实例对象this（所以必须先调用super方法），然后再用子类的构造函数修改this。
       
       
       
       
       
 
 
 
 





