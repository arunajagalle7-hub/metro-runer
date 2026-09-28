# metro-runer <!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Metro Runner</title>

<style>
*{box-sizing:border-box}
body{
  margin:0;
  background:#111;
  color:white;
  font-family:Arial,sans-serif;
  text-align:center;
  overflow:hidden;
}
#game{
  position:relative;
  width:100%;
  max-width:500px;
  height:100vh;
  margin:auto;
  background:linear-gradient(#55b8ff,#dff6ff 55%,#555 56%,#222);
  overflow:hidden;
}
#score{
  position:absolute;
  top:15px;
  left:15px;
  font-size:22px;
  font-weight:bold;
  z-index:10;
}
#road{
  position:absolute;
  bottom:0;
  width:100%;
  height:45%;
  background:#333;
}
.lane{
  position:absolute;
  width:6px;
  height:100%;
  background:#777;
}
.l1{left:33%}.l2{left:66%}

#player{
  position:absolute;
  bottom:70px;
  left:calc(50% - 25px);
  width:50px;
  height:70px;
  background:#e91e63;
  border-radius:15px 15px 8px 8px;
  z-index:5;
}
#player:before{
  content:"";
  position:absolute;
  width:30px;
  height:30px;
  background:#ffd2a6;
  border-radius:50%;
  top:-25px;
  left:10px;
}
.coin{
  position:absolute;
  width:25px;
  height:25px;
  background:gold;
  border:4px solid #ff9800;
  border-radius:50%;
  z-index:4;
}
.train{
  position:absolute;
  width:65px;
  height:90px;
  background:#1565c0;
  border-radius:10px;
  z-index:3;
}
.train:after{
  content:"";
  position:absolute;
  top:15px;
  left:10px;
  width:45px;
  height:25px;
  background:#b3e5fc;
}
#message{
  position:absolute;
  top:42%;
  width:100%;
  font-size:30px;
  font-weight:bold;
  z-index:20;
}
button{
  position:absolute;
  bottom:15px;
  padding:12px 25px;
  border:0;
  border-radius:10px;
  background:#ff9800;
  color:white;
  font-size:18px;
  font-weight:bold;
  z-index:30;
}
#left{left:20px}
#right{right:20px}
</style>
</head>

<body>

<div id="game">

<div id="score">Score: 0</div>

<div id="road">
  <div class="lane l1"></div>
  <div class="
