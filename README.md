情人节表白自动生成程序
=========
情人节已经过去几个月了，不知道各位博友有没有吃到巧克力馅的汤圆。

无聊，为了明年情人节，笨猫修改了个表白程序。

模版文件说明

/just4u  用于存放生成的静态页面

/css

  /css/all.min.css
  
/fonts

  /fonts/RuiHeiXiTi.otf
  
/img

  /img/***.jpg
  
  /img/***.gif
  
/js

  /js/all.min.js
  
  /js/audio.min.js
  
  /js/brav1toolbox.js
  
  /js/flowtime.js
  
  /js/love.min.js
  
  /js/jquery.min.js
  
  /js/love.src.js
  
/music

  /music/saveme.mp3
  
  /music/lovebgm.mp3
  
index.php

love.php  核心处理文件

loveNote.txt  数据记录

loveTpl.html  页面模版文件 love.php生成的页面以此文件为模版

程序运行原理

给页面文字添加span标签，设置id="text-xx"唯一属性，使用contenteditable="true"，开启该元素的编辑模式，用jQuery属性.click()判断点击，用.text()返回此元素的文本内容，并用正则进行判断内容是否合法，然后通过AJAX POST给php处理，php对传入的参数进行过滤，然后读取模版文件，替换模版文件对应内容，保存为新文件并记录操作，最后返回数据给前端，前端处理数据并更新页面。

使用说明

解压上传到网站根目录，通过 http://你的域名/ 进行访问 

下载和演示

下载地址：http://github.com/fengmoxi/love-html
在线演示：http://love.fengmx.com
