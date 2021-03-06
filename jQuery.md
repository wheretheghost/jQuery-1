##  1.jQuery 如何获取元素

jQuery主要是：选择某一个网页元素，然后对其进行某种操作。

将一个选择表达式，放进构造函数jQuery(),然后得到被选中的元素。


##  2.jQuery 的链式操作是怎样的


选中最终的网页元素以后，对其进行一系列的操作，这一系列的操作可以以链条的形式写在一起。

如：
`
$('div').find('h3').eq(2).html('Hello');
`
即找到div元素，选择其中的h3元素，选择第3个h3元素，将他的内容改为Hello。


##  3.jQuery 如何创建元素


创建新元素的方法非常简单，只要把新元素直接传入jQuery的构造函数就行了：

```　　
$('<p>Hello</p>');

$('<li class="new">new list item</li>');

$('ul').append('<li>list item</li>');

```

##  4.jQuery 如何移动元素

jQuery有两种方法来操作元素在网页中的移动，一个是直接移动该元素，一个是启动其他元素，使得目标元素到达一定位置。


1.使用.insertAfter()，把div元素移动到p元素后面：

`
$('div').insertAfter($('p'));
`
2.使用.after()，把p元素移动到div元素前面：
`
$('p').after($('div'));
`
使用这种模式的操作方法，一共有四对：

　　.insertAfter()和.after()：在现存元素的外部，从后面插入元素

　　.insertBefore()和.before()：在现存元素的外部，从前面插入元素

　　.appendTo()和.append()：在现存元素的内部，从后面插入元素

　　.prependTo()和.prepend()：在现存元素的内部，从前面插入元素

##  5.jQuery 如何修改元素的属性

修改元素，即取值或赋值。

使用同一个函数，来完成取值和赋值，即取值器和赋值器合二为一，到底进行取还是赋，由函数的参数决定。


如：
`
$('h1').html();
`
没有参数，表示取出h1的值。
`
$('h1').html('Hello');
`
有参数Hello，表示对h1进行赋值。

常见的取值和赋值函数如下：

　　.html() 取出或设置html内容

　　.text() 取出或设置text内容

　　.attr() 取出或设置某个属性的值

　　.width() 取出或设置某个元素的宽度

　　.height() 取出或设置某个元素的高度

　　.val() 取出某个表单元素的值
