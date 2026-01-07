<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<title>🧸💖</title>

<style>
body{
  margin:0;
  height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  background:linear-gradient(#ffd1e8,#ff9ecf);
  font-family:Arial,sans-serif;
  overflow:hidden;
}

.card{
  background:white;
  padding:30px;
  border-radius:25px;
  width:320px;
  text-align:center;
}

.bears{
  font-size:70px;
  transition:0.5s;
}

.hug{
  transform:scale(1.2);
}

button{
  width:100%;
  padding:14px;
  margin-top:10px;
  font-size:18px;
  border:none;
  border-radius:20px;
}

#yes{
  background:#ff4f8b;
  color:white;
}

#no{
  background:#ddd;
}

#msg{
  margin-top:15px;
  font-size:20px;
  color:#ff4f8b;
}

.heart{
  position:fixed;
  bottom:-20px;
  font-size:26px;
  animation:up 3s linear forwards;
  pointer-events:none;
}

@keyframes up{
  to{
    transform:translateY(-700px);
    opacity:0;
  }
}
</style>
</head>

<body>

<div class="card">
  <div class="bears" id="bears">🧸 🧸</div>

  <h3>جميلة قلبي، هل تحبينني؟</h3>

  <button id="yes">نعم 💕</button>
  <button id="no">لا 🙈</button>

  <div id="msg"></div>
</div>

<script>
document.getElementById("yes").onclick = function(){
  document.getElementById("bears").textContent = "🧸🤗🧸";
  document.getElementById("bears").classList.add("hug");

  document.getElementById("msg").textContent =
    "Ben de seni çok seviyorum güzelim 💖";

  this.style.display="none";
  document.getElementById("no").style.display="none";

  for(let i=0;i<40;i++){
    let h=document.createElement("div");
    h.className="heart";
    h.textContent="💖";
    h.style.left=Math.random()*100+"vw";
    document.body.appendChild(h);
    setTimeout(()=>h.remove(),3000);
  }
}
</script>

</body>
</html>
