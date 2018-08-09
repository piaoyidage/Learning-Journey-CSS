# LESS 

使用 Sublime Text 3，安装 Less2Css 插件，自动将 less 文件转成 css 文件。

## demo_01 注释

less 里面提供两种注释方式，一种是 //, 另一种是 /****/, 编译成 css 文件后，前一种注释将会被忽略，不会被编译。


## demo_02 变量

使用 @变量名: 属性值，可以定义一个变量：

```less
// 变量
@width: 100px;
@height: 200px;

.box {
	width: @width;
	height: @height;
}
```

## demo_03 运算

```less
// 运算
@width: 100px;
@height: @width + 100px;
@color: #ccc;

.box {
	width: @width;
	height: @height;
	color: @color + 10;
}
```

## demo_04 混合(mixin)

简单的混合：

```less
.border {
	border: solid 1px red;
}

// 混合
.box {
	.border;
	background-color: #f0f;
}
```


## demo_05 匹配模式

```less
.pos(a) {
	position: absolute;
}

.pos(r) {
	position: relative;
}

.pos(f) {
	position: fixed;
}


// 匹配 布局定位
.box {
	.pos(f);
}
```


## demo_06 嵌套

嵌套减少了很多代码量，非常方便，此外 & 代表当前父亲选择器。

```less
.wrap {
	background-color: red;

	a {
		font-size: 13px;
		&:hover {
			color: #ff0;
		}
	}

	span {
		color: black;
	}

	& > span {
		color: #f00;
	}
}
```

## demo_07 @arguments

```less
.border(@border-style: solid, @border-width: 2px, @border-color: red){
	border-radius: @arguments;
}

.box {
	.border;
}

.box-2 {
	.border(dashed);
}
```

