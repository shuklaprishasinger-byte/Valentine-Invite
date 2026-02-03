<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>Karthik, Be My Valentine?</title>
<style>
body{
  margin:0;
  min-height:100vh;
  font-family: system-ui, Arial;
  background: linear-gradient(135deg, #ffdde1, #ee9ca7);
  display:flex;
  align-items:center;
  justify-content:center;
  overflow:hidden;
}
.card{
  background:white;
  padding:30px 22px;
  border-radius:22px;
  box-shadow:0 20px 40px rgba(0,0,0,0.15);
  text-align:center;
  max-width:520px;
  width:90%;
  position:relative;
}
h1{font-size:32px;margin-bottom:10px;}
p{font-size:18px;}
button{
  padding:14px 20px;
  font-size:18px;
  border:none;
  border-radius:14px;
  cursor:pointer;
  margin:6px;
}
#yesBtn{background:#ff4d6d;color:white;}
#noBtn{position:absolute;background:#eee;}
#result{display:none;margin-top:18px;font-size:18px;}
</style>
</head>

<body>
<div class="card">
  <h1>Karthik, will you be my Valentine? 💘</h1>
  <p>
    From Prisha ❤️ <br><br>
    My handsome stink,<br>
    3 years of cooking, traveling, and doing life together…<br>
    I still choose you every day 🥰
  </p>

  <button id="yesBtn">Yes 💖</button>
  <button id="noBtn">No 🙈</button>

  <div id="result">
    YAYYY 🥰 Valentine secured! <br>
    More adventures, more food dates, and more us forever 🌍🍳❤️
  </div>
</div>

<audio id="song" src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3"></audio>

<script>
const yesBtn=document.getElementById("yesBtn");
const noBtn=document.getElementById("noBtn");
const result=document.getElementById("result");
const song=document.getElementById("song");

function moveButton(){
  noBtn.style.left=Math.random()*(window.innerWidth-100)+"px";
  noBtn.style.top=Math.random()*(window.innerHeight-60)+"px";
}
noBtn.addEventListener("mouseenter",moveButton);

yesBtn.addEventListener("click",()=>{
  result.style.display="block";
  yesBtn.innerText="Valentine secured ✅";
  noBtn.style.display="none";
  song.play();
});
</script>
</body>
</html>
