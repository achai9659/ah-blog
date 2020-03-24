---
title: css小计
date: 2020-03-13 10:57:35
tags: css
---

# CSS选择器以及优先级
(1) !important  
(2) 内联样式（1000）: 使用内联样式的方法是在相关的标签中使用样式属性。 style=""
(3) ID选择器（0100）：id="" #{}
(4) 类选择器/属性选择器/伪类选择器（0010）：class="" .{} / []{} /
(5) 元素选择器/关系选择器/伪元素选择器（0001）
(6) 通配符选择器（0000）

``` 
<!DOCTYPE html>  
<html lang="en">  
    <head>  
        <meta charset="UTF-8">  
        <title>Document</title>  
        <style>
            #ID-selector {
                font-size: 10px;
            }
            .class-selector {
                font-size: 12px;
            }
            *[proprty-selector] {
                font-size: 14px;
            }
            *:first-child {
                font-size: 16px;
            }
            div {
                font-size: 18px;
            }
            * div {
                font-size: 20px;
            }
            div::first-line {
                font-size: 22px;
            }
            * {
                font-size: 24px;
            }
        </style>
    </head>  
    <body>  
        <div style="font-size: 6px;" proprty-selector="true" id="ID-selector" class="class-selector">
            测试CSS选择器的特殊性
        </div>
    </body>  
</html
```

# 盒模型
包括内容区域、内边距区域、边框区域和外边距区域。
![](/images/box.jpg) 
