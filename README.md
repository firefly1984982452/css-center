---
title: 手机端、电脑端中CSS居中的多种方法
date: 2018-04-24 11:56:41
---
# 布局

## 首先，让我们的背景宽和高都是100%

```
html,body{
	height: 100%;
}
.box {
	height: 100%;
}

```

## html页面

```
<div class="box">
	<div class="item">
		item
	</div>
</div>
```

## 基础的CSS

```
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}
html,body{
	height: 100%;
}
.box {
	width: 100%;
	height: 100%;
	background-color: #f7b2bb;
}

.item {
	width: 50%;
	height: 100px;
	background-color: #1296db;
	text-align: center;
	line-height: 100px;
	color: #fff;
}
```

**tips:因为我的布局很简单，页面也不多，所以我用了`*`号选择器**

# absolute方法实现

## 固定宽高

```
.box{
	position: relative;
}
.item{
	position: absolute;
	width: 200px;
	height: 100px;
	left: 50%;
	top: 50%;
	margin-left: -100px;
	margin-top: -50px;
}
```

## 百分比宽高

```
.box{
	position: relative;
}
.item{
	width: 50%;
	height: 20%;
	position: absolute;
	left: 50%;
	top: 50%;
	transform: translate(-50%,-50%);
}
```

**重点：`transform: translate(-50%,-50%);`**

# 块级元素实现水平居中

```
.box{
	position: relative;
}
.item{
	width: 50%;
	margin: 0 auto;
}
```

# flex方法实现

```
.box{
	display: flex;
	justify-content: center;
	align-items: center;
}
.item{
	
}
```

# 文本居中

- 文字水平居中：`text-align:center;`

- 文字垂直居中：`line-height:height`

------

附：
[案例预览](https://firefly1984982452.github.io/css-center/)
[案例下载地址](https://github.com/firefly1984982452/css-center)