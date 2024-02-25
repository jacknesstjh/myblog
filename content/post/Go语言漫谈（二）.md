---
title: "Go语言漫谈（二）"
date: 2024-02-23T06:36:11+08:00
draft: true
tags: ["hugo","go语言"]
categories: ["go语言漫谈"]
---
	
  第三次接触go语言编程了，由于间隔时间过长，所以我的环境出了很大的问题，我到处找大佬帮忙，终于把环境搭建好了。
	
	
	
  买了一个30套的GO语言编程视频教程，我每天估计能看7个，慢慢看吧。现在看到了变量声明这一段。基本的编程方法算是掌握了。不知道我学得会不会一直好下去。

```
package main

import "fmt"

//Go语言中推荐使用驼峰式命名
//var student_name string
//var studentName string

//var StudentName string

// 声明变量
//var name string
//var age int
//var isOK bool

// 批量声明
var (
	name string //""
	age  int    //0
	isOK bool   //false
)

func main() {
	name = "理想"
	age = 16
	isOK = true
	//Go语言中声明的非全局变量必须使用，不使用就会编译不过去
	//var heiheihei string
	fmt.Print(isOK) //在终端中输出要打印的内容
	fmt.Println()
	fmt.Printf("name:%s", name) //%s:占位符 使用name这个变量值去替换占位符
	fmt.Println(age)            //打印完指定内容后会在后面跟一个换行符
	//heiheihei = "嘿嘿嘿"

	//声明变量并同时赋值
	var s1 string = "whb"
	fmt.Println(s1)
	//类型推导（根据值判断该变量是什么类型）
	var s2 = "20"
	fmt.Println(s2)
	//简短变量声明 只能在函数里面用
	s3 := "哈哈哈"
	fmt.Println(s3)
	//s1 :="10"//同一个作用域（{}）中不能重复声明同名的变量
	//匿名变量是一个特殊的变量 _(后面学了函数再说)

}

```
