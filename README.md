
<!DOCTYPE html>
<html lang="ur">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My New AI - Murtaza</title>
<style>
*{box-sizing:border-box}
body{
  margin:0;
  font-family:Arial,sans-serif;
  background:#101827;
  color:white;
  text-align:center;
}
header{
  background:#172b46;
  padding:25px 10px;
}
h1{color:#42e8d5}
.container{
  max-width:600px;
  margin:25px auto;
  padding:15px;
}
.card{
  background:#1d2b40;
  padding:20px;
  border-radius:15px;
  margin:15px 0;
}
input,button,textarea{
  width:100%;
  padding:13px;
  margin-top:10px;
  border:0;
  border-radius:9px;
  font-size:16px;
}
button{
  background:#16cdbb;
  color:#102030;
  font-weight:bold;
  cursor:pointer;
}
#answer{
  white-space:pre-wrap;
  line-height:1.7;
}
img{
  max-width:100%;
  margin-top:15px;
  border-radius:10px;
}
</style>
</head>
<body>

<header>
<h1>🤖 MY NEW AI</h1>
<p>Welcome to Murtaza AI</p>
</header>

<div class="container">

<div class="card">
<h2>💬 AI Chat</h2>
<input id="question" placeholder="اپنا سوال لکھیں...">
<button onclick="askAI()">Send Message</button>
<p id="answer">السلام علیکم! میں آپ کا My New AI ہوں۔</p>
</div>

<div class="card">
<h2>🖼️ Photo Cleaner</h2>
<input type="file" id="photo" accept="image/*">
<button onclick="clearPhoto()">تصویر صاف کریں</button>
<div id="result"></div>
</div>

<div class="card">
<h2>🌍 Languages</h2>
<p>Urdu | English | Hindi</p>
</div>

</div>

<script>
function askAI(){
 let q=document.getElementById("question").value.trim();
 let a=document.getElementById("answer");

 if(!q){
  a.innerText="براہ کرم اپنا سوال لکھیں۔";
  return;
 }

 a.innerText="آپ کا سوال موصول ہوگیا: "+q+
 "\n\nحقیقی AI جواب کے لیے AI API منسلک کرنا ضروری ہے۔";
}

function clearPhoto(){
 let file=document.getElementById("photo").files[0];
 let result=document.getElementById("result");

 if(!file){
  result.innerText="پہلے تصویر منتخب کریں۔";
  return;
 }

 let url=URL.createObjectURL(file);
 let img=document.createElement("img");
 img.src=url;
 img.style.filter="brightness(1.12) contrast(1.08)";

 result.innerHTML="";
 result.appendChild(img);
}
</script>

</body>
</html>
