## 浏览器内核
### webkit内核
- Apple的Safari, Google的Chrome, Nokia S60平台的默认浏览器，Apple手机的默认浏览器，Android手机的默认浏览器均采用的Webkit作为器浏览器内核

### GEcko内核
- 主要是Firefox浏览器使用的内核

### Trident内核
- 微软的IE系列使用的内核

>搜狗浏览器是双核的，双核并不是指一个页面由2个内核同时处理,而是所有网页（通常是标准通用标记语言的应用超文本标记语言）由webkit内核处理,只有银行网站用IE内核

## js中的内置函数和内置对象
### js中的内置函数 -- 数据封装类对象
- Object
- Array
- Boolean
- Number
- String
- Function
- Date
- RegExp
- Error

### js中的内置对象
- Math
- JSON

## 函数
### 函数传参
```JavaScript
function square(num){
    total=200;    
    return total;  
}   
   var total=50;  
   var number=square(20);   
   console.log(total);//输出是200，此时函数内部的total的确覆盖了全局变量。

function square(total){
    total=200;    
    return total;  
}   
   var total=50;  
   var number=square(20);   
   console.log(total);//输出是50，此时total并不作为全局变量。而它与上面的例子唯一的不同只在于它的传参名叫total。

function square(num){
    var total = 20;
    total=200;    
    return total;  
}   
   var total=50;  
   var number=square(20);   
   console.log(total);//输出50，它与第一个例子的唯一不同在于声明了一句var total ＝ 20；结合第二个例子，说明传参时实际就等于声明了一次，此时就变为新的局部的变量。
```
