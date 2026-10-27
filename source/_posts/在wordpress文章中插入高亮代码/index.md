---
title: "在wordpress文章中插入高亮代码"
date: 2015-01-06
categories: 
  - "yxeg"
---

1.后台搜索CodeColorer安装，使用默认设置即可，也可以勾选“显示行号”； 2.编写或复制好代码后，转到文本编辑模式下，使用下面格式即可，记得去掉“/”前的空格 `` `此处插入已编写好的代码< /code>` 3.可以修改插件目录下的“codecolorer.php”启用可视化编辑，具体方法为注释掉几行代码，如下： `[cce_php first_line='136'] // if (get_user_option('rich_editing') == 'true') { // add_filter('mce_external_plugins', array('CodeColorerLoader', 'AddTinyMCEPlugin')); // add_filter('mce_buttons', array('CodeColorerLoader', 'RegisterTinyMCEButton')); // }` ``
