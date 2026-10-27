---
title: "关于友链页面"
date: 2015-08-07
categories: 
  - "yxeg"
coverImage: "link-1-1.jpg"
---

上图为友情页面样式，以下为代码部分： PHP参考：

**Code**   [View](file:///C:/Users/lichao/Desktop/CodeRenderUnmi/CodeRender.hta#)[Copy](file:///C:/Users/lichao/Desktop/CodeRenderUnmi/CodeRender.hta#)[Print](file:///C:/Users/lichao/Desktop/CodeRenderUnmi/CodeRender.hta#)[](file:///C:/Users/lichao/Desktop/CodeRenderUnmi/CodeRender.hta#)

1. <?php   
2. $bookmarks = get\_bookmarks();   
3. if ( !emptyempty($bookmarks) ){   
4.     echo '<ul class\="link-content clearfix"\>';   
5.     foreach ($bookmarks as $bookmark) {   
6.         echo '<li><a href="' . $bookmark->link\_url . '" title="' . $bookmark->link\_description . '" target="\_blank" >'. get\_avatar($bookmark\->link\_notes,64) . '<span class\="sitename"\>'. $bookmark\->link\_name .'</span></a></li>';   
7.     }   
8.     echo '</ul>';   
9. }   
10. ?>   
11.                 <?php   
12.                     // If comments are open or we have at least one comment, load up the comment template   
13.                     if ( comments\_open() || get\_comments\_number() ) :   
14.                         comments\_template();   
15.                     endif;   
16.                 ?></code>   
17. CSS参考：   

19. <code lang="php"\>.link-content li{float:left;text-align: center;width: 100px;font-size:12px;margin-bottom:10px}.link-content li img{border-radius:100%;margin-bottom:5px;transition:0.5s;-webkit-transtion:0.5s} .link-content li span{display:block} .link-content li:hover img{transform:rotate(360deg);-webkit-transform:rotate(360deg);}
