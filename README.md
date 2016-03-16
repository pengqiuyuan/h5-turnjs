## h5-turnjs
 - 翻书页[效果](http://html.pengqiuyuan.com/h5/h5turnjs/index.html)展示内容

![gif6](https://cloud.githubusercontent.com/assets/4953205/13800958/a9777c7c-eb68-11e5-9264-f3478b9b27d8.gif)

#### 效果展示
-![img](https://cloud.githubusercontent.com/assets/4953205/13800902/49858890-eb68-11e5-8b50-b4ace08cbfbd.png)		

#### turn.js的使用

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

