---
title: "关于ajax库"
date: 2015-04-11
categories: 
  - "yxeg"
---

部分主题会出现加载ajax.proxy.ustclug.org未响应的情况，可以查找主题内header.php文件，替换里面的Google jQuery库链接即可； 以下代码的效果是：当外部引用的jQuery库无法加载时，就自动加载网站本地的jQuery库，所以你首先要先下载jQuery库，然后上传到你正在使用的Wordpress主题的根目录，这样下面的代码才能正常工作。 jQuery库1.4.2 mini版下载 任选一个地址下载即可 http://code.jquery.com/jquery-1.4.2.min.js http://ajax.proxy.ustclug.org/ajax/libs/jquery/1.4.2/jquery.min.js http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.4.2.min.js http://lib.sinaapp.com/js/jquery/1.4.2/jquery.min.js 如果你需要其他版本的jQuery库，请到 SAE开放库 下载;
