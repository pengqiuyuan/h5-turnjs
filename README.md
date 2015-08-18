h5-turnjs
=========

##翻书页效果展示内容
---
#### 1.效果展示
[效果](http://html.pengqiuyuan.com/h5/h5turnjs/index.html)

-![img](http://html.pengqiuyuan.com/images/h5-turnjs/1.png)		
-![img](http://html.pengqiuyuan.com/images/h5-turnjs/2.png)

#### 1.turn.js的使用
代码：
```
  <script type="text/javascript">
      $(function progressbar(){
        var w = $(".graph").width();
        $(".flipbook-viewport").show();
      });
      //屏蔽ios下上下弹性
      $(window).on('scroll.elasticity', function (e) {
          e.preventDefault();
      }).on('touchmove.elasticity', function (e) {
          e.preventDefault();
      });
      function loadApp() {
          var w=$(window).width();
          var h=$(window).height();
          $('.flipboox').width(w).height(h);
          $(window).resize(function(){
              w=$(window).width();
              h=$(window).height();
              $('.flipboox').width(w).height(h);
          });
          $('.flipbook').turn({
                  // Width
                  width:w,
                  // Height
                  height:h,
                  // Elevation
                  elevation: 50,
                  display :'single',
                  // Enable gradients
                  gradients: true,
                  // Auto center this flipbook
                  autoCenter: true
          });
      }
      yepnope({
          test : Modernizr.csstransforms,
          yep: ['js/turn.js'],
          complete: loadApp
      });
  </script>
```

