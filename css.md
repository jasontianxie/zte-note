1、
white-space: pre-wrap;设置换行
    word-wrap: break-word;设置长数字和字母换行

2、
父元素的高度必须明确指定，子元素设置height：100%才有效。父元素设置min-height，max-height，子元素的100%都不会生效。

3、设置placeholder的样式（在输入框得到焦点或hover时）
.search-box-input:focus::-webkit-input-placeholder{
    color: #22bdf6;
}
.search-box-input:focus:-moz-placeholder{
    color: #22bdf6;
}
.search-box-input:focus::-moz-placeholder{
    color: #22bdf6;
}
.search-box-input:focus:-ms-input-placeholder{
    color: #22bdf6;
}
.search-box-input:hover::-webkit-input-placeholder{
    color: #22bdf6;
}
.search-box-input:hover:-moz-placeholder{
    color: #22bdf6;
}
.search-box-input:hover::-moz-placeholder{
    color: #22bdf6;
}
.search-box-input:hover:-ms-input-placeholder{
    color: #22bdf6;
}


4、input的type属性为number时，如何去掉右边的上下箭头

网页在有些情况下，会需要input的输入的为单纯数字的文本框，此时type=number，但使用type=number时，输入框后面会有一个上下箭头，那么如何去掉上下箭头呢？

1)chrome浏览器移除
input[type="number"]::-webkit-outer-spin-button,input[type="number"]::-webkit-inner-spin-button{
        -webkit-appearance:textfield;
}
使用none替代textfield，也可以实现去除箭头的效果

2)firefox浏览器下移除
input[type="number"]{
        -moz-appearance:textfield;
}
 在firefox浏览器下使用none替代textfield没有效果。

3)用type="tel"代替
　　input[type="tel"]的value值亦是number，且其没有type="number"时的上下箭头，故我们可以用[type="tel"]代替[type="number"]，达到一样的效果（实际使用中发现tel属性没起作用？），并通过设置maxlength = "m"限定value值得长度。如果有其他的要求，可以通过正则来判断。


5、css grid layout
http://www.w3cplus.com/css3/css-grid-layout-quick-start-guide.html

6、[css]如何让一个元素div1的宽度由子元素的宽度决定，并超出父元素div0
http://blog.csdn.net/misssprite/article/details/20308229
