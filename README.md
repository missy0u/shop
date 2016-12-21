 基地商城 Demo
 ============

 > 无耐被拉去帮忙切图，看了一下设计图，挺简单的嘛，反正都要做，就当做个制作分享

 分享要点
 ---------------

 **css reset**

 > base.css 有详尽注释，可以直接使用，PS:记得把自己没用到的css reset去掉

 **循环列表HTML结构尽量简单**

 > 列表为什么非要套ul>li？为什么非要在div定义class？很多时候直接定义标签就能实现需求，html结构要灵活，代码量有多简单就多简单，能省即省

 ```html
 <!-- bad -->
 <ul>
   <li>
     <div class="pic">
       <a href="javascript:;"><img src="//images.apple.com/cn/iphone/compare/images/tech_specs_iphone7_large.jpg" alt=""></a>
       <span class="auction">竞拍</span>
     </div>
     <div class="info">
         <div><a href="javascript:;">爱疯手机</a></div>
         <span>¥8000/部</span>
     </div>
   </li>
   ...
 </ul>
 ```

 ```html
 <!-- best -->
 <dl>
     <dt>
       <a href="javascript:;"><img src="//images.apple.com/cn/iphone/compare/images/tech_specs_iphone7_large.jpg" alt=""></a>
       <span class="auction">竞拍</span>
     </dt>
     <dd>
         <div><a href="javascript:;">爱疯手机</a></div>
         <span>¥8000/部</span>
     </dd>
 </dl>
 ...
 ```

 **循环列表间距父元素用负值清除**

 > 不要在第一个和最后一个列表元素加class清除间距

 **雪碧图玩法**

 > 不规则图形png8毛边问题，图与图之间的间距，background-position的运用

 **inline-block布局玩法**

 > inline-block 排版的运用，具体参考源码

 **HTML tag**

 ```html
 <!-- bad -->
 <div class="nav"><span>全部商品</span> > 我的购买</div>
 ```

 ```html
 <!-- good -->
 <div class="nav"><span>全部商品</span> &gt; <span>我的购买</span></div>
 ```

 > “我的购买”文字尽量用标签包裹，免得像Safari这样的高级浏览器出现问题

 浏览器兼容
---------------
- IE 6+
- Firefox (latest)
- Chrome (latest)
- Safari (latest)
- Opera (latest)

PS
---------------

1.分页按程序给出的HTML格式要求兼容的，也支持到ie6+，可参考
2.由于项目简单样式命名没有包裹，例如table
3.时间关系没有响应式
4.js代码不用理会
