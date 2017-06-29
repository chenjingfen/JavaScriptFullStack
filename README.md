# JavaScriptFullStack
整理javaScript，学习node
ECMAScript==>javaScript


要特别注意相等运算符==。JavaScript在设计时，有两种比较运算符：

第一种是==比较，它会自动转换数据类型再比较，很多时候，会得到非常诡异的结果；

第二种是===比较，它不会自动转换数据类型，如果数据类型不一致，返回false，如果一致，再比较。

由于JavaScript这个设计缺陷，不要使用==比较，始终坚持使用===比较。

另一个例外是NaN这个特殊的Number与所有其他值都不相等，包括它自己：

NaN === NaN; // false
唯一能判断NaN的方法是通过isNaN()函数：

isNaN(NaN); // true


不要使用 new Number()、new Boolean()、new String()创建包装对象；
用parseInt()或parseFloat()来转换任意类型到number；
用户String()来转换任意类型到string，或者直接调用某个对象的toString()方法。
通常不必把任意类型转换为boolean再判断，因为可以直接写if(myVar){...};
typeof操作符可以判断出number、boolean、string、function和undefined;
判断Array要使用Array.isArray(arr);
判断null请使用myVar===null;
判断某个全局变量是否存在用typeof window.myVar==='undefined';
函数内部判断某个变量是否存在用typeof myVar==='undefined'



JavaScript不区分类和实例的概念，而是通过原型来实现面向对象编程。

JavaScript的原型链和Java的Class区别就在，它没有“class”的概念，所有对象都是实例，
所谓继承关系不过是把一个对象的原型指向另一个对象而已。

