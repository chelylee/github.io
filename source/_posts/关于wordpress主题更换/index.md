---
title: "关于WordPress主题更换"
date: 2014-12-09
categories: 
  - "yxeg"
---

关于更换WordPress主题后所需修改： 1.去掉google字体：在主题文件functions.php内查找”googleapis“代码直接注释掉（使用”//“双斜杠注释），或直接替换为useso，另可安装插件解决； 2.更改页面显示字体：style.css内查找”font-family“，后面添加喜欢字体即可； 3.去除评论框下的注释：打开wp-includes/comment-template.php查找： 将其注释掉或删除即可； 4.去除页面底部版权信息：footer.php内查找版权信息，替换或删除，替换内容为： `<a href="<?php echo get_option('home'); ?>" title="<?php bloginfo('name'); ?>" rel="generator"><?php bloginfo('name'); ?></a>` 大体如此，以上！
