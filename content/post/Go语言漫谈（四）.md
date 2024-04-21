---
title: "Go语言漫谈（四）"
date: 2024-04-21T14:38:17+08:00
draft: true
tags: ["hugo","go语言"]
categories: ["go语言漫谈"]
---

  这是第四篇go语言的漫谈，我已经学习go语言一段时间了。今天主要学习了整型。
  第一篇：如何配置go编程环境
  第二篇：变量的声明
  第三篇：常量的声明和使用
  第四篇：整型类型
  我不是每天都有时间学习go语言编程，但是我会慢慢的看，慢慢的学习。
  下面贴一下整型的内容。
  
  
```
package main

import "fmt"

// 整型
func main() {
	//十进制
	var i1 = 101
	fmt.Printf("%d\n", i1)
	fmt.Printf("%b\n", i1) //十进制转换为二进制
	fmt.Printf("%o\n", i1) //十进制转换为八进制
	fmt.Printf("%x\n", i1) //十进制转换为十六进制

	//八进制
	i2 := 077
	fmt.Printf("%d\n", i2)

	//十六进制
	i3 := 0x1234567
	fmt.Printf("%d\n", i3)

	//查看变量类型
	fmt.Printf("%T\n", i1)

	//声明int8类型的变量
	i4 := int8(9) //明确指定int8类型，否则就是默认为int类型
	fmt.Printf("%T\n", i4)

}

```