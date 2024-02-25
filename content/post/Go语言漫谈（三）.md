---
title: "Go语言漫谈（三）"
date: 2024-02-25T12:15:08+08:00
draft: true
tags: ["hugo","go语言"]
categories: ["go语言漫谈"]
---

  坚持学习go语言编程的第3天，我觉得编程学习起来还是不容易的，特别是对我来说。第一天学了如何配置go编程环境，然后第二天学了变量的声明。今天是第三天学了常量的声明和使用。
  
  我每天可以看最多7个视频，还要看时间长短，短的可以看7个，如果是长的，我大概一天可以看3-4个。每天坚持下去吧，坚持看和学习。
  
  我现在基本的概念就学了变量和常量。希望我坚持下去，不要学2天就忘记学习了。我从现在开始每天看视频，每天发博文。下面贴一下常量的学习内容。
  
  ```
package main

import "fmt"

//常量
//常量定义了之后不能修改
//在程序运行期间不会改变的量

const pi = 3.1415926

// 批量声明常量
const (
	statusOK = 200
	notFound = 404
)

// 批量声明常量时，如果某一行声明后没有赋值，默认就和上一行一致
const (
	n1 = 100
	n2
	n3
)

// iota:类似枚举
const (
	a1 = iota //0
	a2        //1
	a3        //2
)
const (
	b1 = iota //0
	b2        //1
	_         //2
	b3        //3
)

// 插队
const (
	c1 = iota //0
	c2 = 100  //100
	c3 = iota //2
	c4        //3
)

// 多个常量声明在一行
const (
	d1, d2 = iota + 1, iota + 2 //d1:1,d2:2
	d3, d4 = iota + 1, iota + 2 //d3:2,d4:3
)

// 定义数量级
const (
	_  = iota
	KB = 1 << (10 * iota)
	MB = 1 << (10 * iota)
	GB = 1 << (10 * iota)
	TB = 1 << (10 * iota)
	PB = 1 << (10 * iota)
)

func main() {
	//pi = 123
	fmt.Println("n1", n1)
	fmt.Println("n2", n2)
	fmt.Println("n3", n3)

	fmt.Println("a1", a1)
	fmt.Println("a2", a2)
	fmt.Println("a3", a3)

	fmt.Println("b1", b1)
	fmt.Println("b2", b2)
	fmt.Println("b3", b3)

	fmt.Println("c1", c1)
	fmt.Println("c2", c2)
	fmt.Println("c3", c3)
	fmt.Println("c4", c4)

	fmt.Println("d1", d1)
	fmt.Println("d2", d2)
	fmt.Println("d3", d3)
	fmt.Println("d4", d4)
}

  ```
