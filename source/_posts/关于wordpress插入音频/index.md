---
title: "关于wordpress插入音频"
date: 2015-01-01
categories: 
  - "yxeg"
---

1.wordpress添加音频方法： `[audio src="音频位置.mp3"]` `[audio mp3="音频网址.mp3"]`  后面可加loop或autoplay参数 2.网易云音乐添加方法： `iframe src="http://miantiao.jd-app.com/m163player/音乐ID" frameborder="0" scrolling="0" width="430" height="200" allowtransparency></iframe>`   3.免插件修改文件 主题functions.php内，在php循环中插入以下内容： `/**添加 flash player */ function myplayer($atts, $content=null){ extract(shortcode_atts(array("auto"=>'no',"loop"=>'no'),$atts)); return ''; } add_shortcode('music','myplayer');` 然后复制player.swf到主题根目录：[下载地址](http://mraaaa.com/wp-content/themes/maupassant-master/player.swf) 使用以下代码插入音乐： `[music]音乐文件地址[/music]` 可用music auto="yes or no" loop="yes or no"
