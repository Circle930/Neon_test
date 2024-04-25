# CSS Neon Text

1. 这是一个演示如何使用 CSS 创建霓虹文本效果的简单示例。
2. 原文来自 [3个使用CSS创建的霓虹灯效果/发光效果文本](http://www.webkaka.com/tutorial/html/2021/0628121/)




## 说明
- HTML 文档类型声明，指示浏览器使用 HTML5 解析页面。
- 设置文档字符编码为 UTF-8，支持显示多语言字符。
- 设置视口的宽度等于设备的宽度，并初始化缩放比例为 1.0，用于响应式布局。
- 设置页面标题。
- .neonText 样式：定义了文本的颜色和霓虹效果，使用 text-shadow 属性实现霓虹光晕。
- body 样式：设置页面背景色为深绿色，采用 Flexbox 布局使文本水平和垂直居中。
- h1 样式：设置文本的字体、大小、边框、阴影和动画效果。
- @keyframes pulsate 动画：定义了文本的闪烁动画效果，通过改变 text-shadow 属性值实现。


## HTML 结构

```
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>css neon text</title>
    <style type="text/css">
    .neonText {
      color: #fff;
      text-shadow:
        0 0 7px #fff,
        0 0 10px #fff,
        0 0 21px #fff,
        0 0 42px #bc13fe,
        0 0 82px #bc13fe,
        0 0 92px #bc13fe,
        0 0 102px #bc13fe,
        0 0 151px #bc13fe;
    }
    
    body {
      font-size: 18px;
      font-family: "Sacramento", sans-serif;
      background-color: #010a01;
      display: flex;
      justify-content: center;
      align-items: center;  
    }  
    
    h1, h2 {
      text-align: center;
      font-weight: 400;
    }
    
    h1 {
      font-size: 6.2rem;
      animation: pulsate 1.5s infinite alternate;  
      border: 0.2rem solid #fff;
      border-radius: 2rem;
      padding: 0.4em;
      box-shadow: 0 0 .2rem #fff,
                0 0 .2rem #fff,
                0 0 2rem #bc13fe,
                0 0 0.8rem #bc13fe,
                0 0 2.8rem #bc13fe,
                inset 0 0 1.3rem #bc13fe; 
    }

    @keyframes pulsate {
        
      100% {

          text-shadow:
          0 0 4px #fff,
          0 0 11px #fff,
          0 0 19px #fff,
          0 0 40px #bc13fe,
          0 0 80px #bc13fe,
          0 0 90px #bc13fe,
          0 0 100px #bc13fe,
          0 0 150px #bc13fe;
      
      }
      
      0% {

        text-shadow:
        0 0 2px #fff,
        0 0 4px #fff,
        0 0 6px #fff,
        0 0 10px #bc13fe,
        0 0 45px #bc13fe,
        0 0 55px #bc13fe,
        0 0 70px #bc13fe,
        0 0 80px #bc13fe;

    }
    </style>
</head>

<body>

<h1 class="neonText">
 CIRCLE IS GLOWING！
</h1>

</body>

</html>
```
