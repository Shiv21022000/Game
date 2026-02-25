<!DOCTYPE html>
<html>
<head>
<title>Shivaay Colour Trading</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body{
font-family: Arial;
text-align:center;
background:black;
color:white;
}
button{
padding:15px;
margin:10px;
font-size:18px;
border-radius:10px;
border:none;
cursor:pointer;
}
.red{background:red}
.green{background:green}
.white{background:white;color:black}
.violet{background:violet;color:black}
.yellow{background:yellow;color:black}
</style>
</head>

<body>

<h1>Shivaay Colour Trading</h1>
<h2>Balance: ₹<span id="balance">100</span></h2>

<button class="red" onclick="play('Red')">Red</button>
<button class="green" onclick="play('Green')">Green</button>
<button class="white" onclick="play('White')">White</button>
<button class="violet" onclick="play('Violet')">Violet</button>
<button class="yellow" onclick="play('Yellow')">Yellow</button>

<h3 id="result"></h3>

<script>
let balance=100;
function play(color){
let colors=["Red","Green","White","Violet","Yellow"];
let winColor=colors[Math.floor(Math.random()*colors.length)];
if(color==winColor){
balance+=10;
document.getElementById("result").innerHTML="You WON! "+winColor;
}else{
balance-=10;
document.getElementById("result").innerHTML="You LOST! Winning colour was "+winColor;
}
document.getElementById("balance").innerHTML=balance;
}
</script>

</body>
</html>
