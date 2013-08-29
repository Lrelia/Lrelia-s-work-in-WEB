Lrelia-s-work-in-WEB, a solution for showing/hiding photos
====================
<!DOCTYPE html>
<head>
<title>Canvas Square</title>
<meta charset="utf-8">
<!-- [if IE 6]>
<![endif]-->
<style type="text/css">
.way {
  width: 600px;
  height: 450px;
  border: 10px solid;
  border-radius: 8px;
  margin: 0 auto;
  background:HSLA(30,50%,80%,.6);
   box-shadow: inset 0px 0px 8px 2px #FF00FF;
}
.inactive {
  display:none;
}
.content {
  width: 560px;
  height: 400px;
  text-align: center; 
  margin: 0 auto;
  margin-top: 20px; 

}
.prev{
  float: left;
  text-decoration: none;
  padding: 10px;
  margin-left: 25px;
  line-height: 10px;
  border-radius:4px;
  background: HSLA(60,70%,40%,.6);
}
a {
  box-shadow: 0 0 3px 1px #000000;
}
a:hover {
  background: #FFFF00;
  color: white;
  font-size: 1.2em;
}
.next {
  float: right;
  text-decoration: none;
  padding: 10px;
  margin-right: 25px;
  line-height: 10px;
  border-radius:4px;
  background: HSLA(60,70%,40%,.6);
}
img {
 margin-top: 15px; 
 width: 530px;
 height: 380px;
 overflow: hidden;
 box-shadow: 3px 3px 8px 3px #000;
}
</style>
<!--[if IE 6]><script type="text/javascript" src=""></script><![endif]--> 
<script type="text/javascript" src="jquery-2.0.3.min.js"></script>
<script type="text/javascript">
$(function() {
 var current=0; 
 var now=$('.content img');
  var last=now.length-1;
  now.addClass('inactive');
  now.eq(current).removeClass('inactive');
  var handle_prev= function () {
      now.eq(current).addClass('inactive');
         current = current - 1 == -1?last: current - 1;
         now.eq(current).removeClass('inactive');
      };
  var handle_next= function () {
      now.eq(current).addClass('inactive');
         current = current + 1 > last ? 0: current + 1;
         now.eq(current).removeClass('inactive');
      };
  $('.prev').click(handle_prev);
  $('.next').click(handle_next);
});
</script>
</head>
<body>
<div class='way'>
  <div class='content'>
    <img src='image\1.jpg' alt='First'>
      <img src='image\2.jpg' alt='Second' >
        <img src='image\3.jpg' alt='Thrid'>
  </div>
  <div class='operator'>
  <a href='#' class='prev'>prev</a>
  <a href='#' class='next'>next</a>
  </div>
 </div>
</body> 
</html>
