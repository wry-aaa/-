# -
点击导航按钮，按钮样式在三道横和×之间动态切换

css代码
< style type= "text/css" >
     .close {
        font-size : 14 px;
        position : absolute ;
        left :8 px ;
        top : 20 px;
        height : 25 px;
        width : 25 px;
        text-align : left ;
        /*background-color: #26a2ff;*/
        background-color : #fff ;
     }
     .close-icon {
          display : inline-block ;
        /*line-height: 20px;*/
        position : relative ;
     }
      .close-icon ,.close-icon : before, .close-icon :after {
        width : 25 px;
        height : 2 px;
        /*background-color: #fff;*/
       background-color : #000000 ;
        -webkit-transition : .3 s;
        transition : .3 s;
        border-radius : 1 px;
     }
       .close-icon :before , .close-icon: after {
           content : '' ;
        position : absolute ;
        -webkit-transform-origin : left 50% ;
        transform-origin : left 50 % ;
        outline : 1 px solid transparent ;
     }
     .close-icon :before {
        top : -8 px;
     }
     .close-icon :after {
          bottom : -8 px;
     }

     .open {
        background-color : #ffffff ;
     }
     .open :before , .open: after {
          width : 29 px;
     }
     .open :before {
        -webkit-transform : translate3d( 0 ,-2 px ,0 ) rotate( 45 deg) ;
        transform : translate3d ( 0, -2 px, 0 ) rotate( 45 deg) ;
     }
     .open :after {
        -webkit-transform : translate3d ( 0, 2 px, 0 ) rotate( -45 deg) ;
        transform : translate3d ( 0, 2 px, 0 ) rotate( -45 deg) ;
     }
 </ style>
 
 
html代码
< div class= "close" >
    < span class= "close-icon open" ></ span>
</ div >

js代码
< script src= "js/jquery-1.8.3.js" type ="text/javascript" charset = "utf-8"></ script >
< script type= "text/javascript" >
      $(' . close').click(function(){
           $(' . close-icon').toggleClass(' open ');
      });
</ script >
