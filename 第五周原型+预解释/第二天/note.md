### 1.1预解释无节操：
- 只对等号左边带var的，声明但不定义
- 自执行函数不会进行预解释，只有，执行到他的时候，声明+定义+调用同步完成
- 已经声明过的不会进行重复声明，但会重新赋值；
- return下面的语句虽然不会执行，但会进行预解释；
- 函数的声明早于变量的声明
- （在IE10及10以下浏览器下）在条件判断语句中，无论条件是否成立，都会进行预解释；
    + 不要在条件判断语句中写函数的定义阶段；否则，各大浏览器对其的兼容性不同
### 1.2 全局变量，都是window的全局属性； 全局函数，都是window的全局方法；
比如：
```
    setInterval()
    setTimeout()
    alert()
    confirm()
```
### 1.3关于this：
- 当一个元素身上的事件被触发的时候，会执行一个函数，函数中的this指向当前这个元素；
- 自执行函数中的this，永远都是window；
- 回调函数中的this，一般都是window； setInterval(函数名,1000)  ary.sort(function(){})
- 当函数被调用的时候，看前面是否有"."，"."前面是谁，this就是谁；
### 1.4带var和不带var的区别：
- 带var:1)会进行预解释 2）如果在全局作用域下，他就是window的全局属性
- 不带var：1）不会进行预解释 2）不带var在"赋值"的时候，相当于window添加全局属性














