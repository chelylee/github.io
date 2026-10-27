---
title: "Wordpress后台登录过慢"
date: 2014-11-13
categories: 
  - "yxeg"
---

换了皮肤后登录后台好慢，开始还以为是公司网络问题，后来发现家里也一样；但奇怪的是网站前台登录很快，只有后台登录非常慢，一直在加载，无意中看到左下角显示“等待 fonts.useso.com 响应”，虽然刚开始玩这个，但是看到fonts、google字样，也就大概明白问题出现在哪里了。百度了一下，很快解决： 问题是因为调用google字体而产生，墙内访问google服务可想而知，解决方法是在主题文件下的 “functions.php”文件，添加如下代码即可：`   ``` add_filter('gettext_with_context', 'disable_open_sans', 888, 4 ); function disable_open_sans( $translations, $text, $context, $domain ) {     if ( 'Open Sans font: on or off' == $context && 'on' == $text )     {         $translations = 'off';     }     return $translations; } ```   `or： `class Disable_Google_Fonts { public function __construct() { add_filter( 'gettext_with_context', array( $this, 'disable_open_sans' ), 888, 4 ); } public function disable_open_sans( $translations, $text, $context, $domain ) { if ( 'Open Sans font: on or off' == $context && 'on' == $text ) { $translations = 'off'; } return $translations; } } $disable_google_fonts = new Disable_Google_Fonts;`
