## -webkit-，-moz-，-ms-，-o-具体指什么？
### -webkit-，-moz-，-ms-，-o-是指浏览器私有前缀名。

 - 那为什么要有私有前缀呢?  
 - 因为制定HTML和CSS标准的组织W3C动作是很慢的。  
 - 通常，有w3c组织成员提出一个新属性，比如说圆角border-radius，大家都觉得好，但是w3c不会为这个属性制定标准，而是要走很复杂的程序，经过很多审查。  
 - 而浏览器商不愿意等那么久，他们觉得一个属性已经够成熟了，就会在浏览器中加入支持。  
 - 但是避免日后w3c公布标准时有所变更，就会加入一个私有前缀，比如-webkit-border-radius。  

### -webkit-，-moz-，-ms-，-o-具体代表的浏览器如下：
- -webkit-代表chrome、safari私有属性
- -moz-代表firefox浏览器私有属性
- -ms-代表IE浏览器私有属性
- -o-代表Operai私有属性

***

## 清浮动的三种方法
- 父元素设置属性
```
overflow:hidden;
```
- 伪元素清除
```
.clearfix:after{
    content:'';
    display:block;
    height:0;
    clear:both;
    visibility:hidden;
}

.clearfix{
    *zoom:1;
}
```
- 双伪元素清除
```
.clearfix:before,
.clearfix:after{
    content:'';
    display:table;
}
.clearfix:after{
    clear:both;
}
.clearfix{
    *zoom:1;
}
```

***

## 页面设置全灰的属性
```
filter: grayscale(100%);
```
