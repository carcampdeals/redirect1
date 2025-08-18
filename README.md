<!doctype html>
<html lang="he" dir="rtl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Car & Camp - מצטרפים לקבוצה</title>
  <meta http-equiv="refresh" content="7; url=https://linkly.link/2DKDf">
  <style>
    body{
      margin:0; height:100vh; display:grid; place-items:center;
      font-family:Arial, sans-serif; color:#fff;
      background:url('./background.jpg.png') no-repeat center center/cover;
    }
    .overlay{position:fixed; inset:0; background:rgba(0,0,0,.7);}
    .card{
      position:relative; z-index:1; text-align:center;
      background:rgba(0,0,0,.6); padding:24px; border-radius:16px;
      width:min(700px,90%); box-shadow:0 8px 30px rgba(0,0,0,.6);
    }
    .logo{max-width:260px; margin:0 auto 12px;}
    h1{margin:0 0 8px; font-size:28px; color:#fff;}
    h2{margin:0 0 18px; font-size:20px; color:#ff4c4c;}
    .progress{margin:16px auto; width:240px; height:10px; background:#333;
              border-radius:999px; overflow:hidden;}
    .bar{height:100%; width:0%; background:linear-gradient(90deg,#ff0000,#ff4c4c);
         transition:width .25s ease;}
    .count{margin-top:6px; font-size:16px;}
    .btn{
      display:inline-block; margin-top:16px; padding:12px 18px; border-radius:12px;
      background:#ff0000; color:#fff; font-weight:bold; text-decoration:none;
      transition:background .2s;
    }
    .btn:hover{background:#cc0000;}
  </style>
</head>
<body>
  <div class="overlay"></div>
  <div class="card">
    <img src="./CAR001.png" alt="Car & Camp" class="logo"/>
    <h1>עוד רגע… מצטרפים לקבוצת Car & Camp</h1>
    <h2>דילים שווים לאוהבי הרכב וחובבי הפנאי והשטח</h2>
    <div class="progress"><div class="bar" id="bar"></div></div>
    <p class="count">מעבר אוטומטי בעוד <span id="sec">7</span> שניות…</p>
    <a href="https://linkly.link/2DKDf" class="btn" id="cta">כניסה מידית לקבוצה</a>
  </div>
  <script>
    const url = "https://linkly.link/2DKDf";
    const total = 7; let left = total;
    const sec=document.getElementById("sec"), bar=document.getElementById("bar");
    sec.textContent=total;
    const int=setInterval(()=>{
      left--; sec.textContent=left;
      bar.style.width=((total-left)/total*100)+"%";
      if(left<=0){clearInterval(int); window.location.replace(url);}
    },1000);
    document.getElementById("cta").addEventListener("click",()=>clearInterval(int),{once:true});
  </script>
</body>
</html>
