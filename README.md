
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shehab Video Optimizer</title>
<style>
*{box-sizing:border-box}
body{
margin:0;background:#080b12;color:white;
font-family:Arial,sans-serif;
padding:25px 16px;
}
.container{max-width:650px;margin:auto}
header{text-align:center;padding:35px 0}
h1{font-size:30px;margin-bottom:10px}
h1 span{color:#38bdf8}
p{color:#9ca3af;line-height:1.6}
.card{
background:#111827;border:1px solid #263449;
padding:22px;border-radius:16px;margin-top:20px
}
.upload{
border:2px dashed #38516d;
padding:35px 15px;text-align:center;
border-radius:12px;margin:18px 0;
}
input[type=file]{max-width:100%;margin-top:15px}
select,button{
width:100%;padding:14px;margin-top:13px;
border-radius:9px;border:1px solid #334155;
background:#1e293b;color:white;font-size:15px
}
button{
background:#0284c7;border:0;font-weight:bold;
}
button:disabled{opacity:.5}
.status{margin-top:15px;color:#38bdf8}
footer{text-align:center;margin:35px 0;color:#64748b}
</style>
</head>
<body>
<div class="container">
<header>
<h1>Shehab <span>Video Optimizer</span></h1>
<p>Professional Video Processing Studio</p>
</header>

<div class="card">
<h2>Upload Your Video</h2>
<p>Select a video to prepare for optimization.</p>
<div class="upload">
<p>Choose your video file</p>
<input type="file" id="video" accept="video/*">
</div>

<label>Resolution</label>
<select id="resolution">
<option value="1080">1080p</option>
<option value="2160">4K</option>
</select>

<label>Frame Rate</label>
<select id="fps">
<option value="30">30 FPS</option>
<option value="60">60 FPS</option>
<option value="120">120 FPS</option>
</select>

<button id="process">Optimize Video</button>
<div class="status" id="status">Waiting for video...</div>
</div>
<footer>© 2026 Zx Video Optimizer</footer>
</div>

<script>
document.getElementById("process").onclick=()=>{
const file=document.getElementById("video").files[0];
const status=document.getElementById("status");
if(!file){
status.textContent="Please select a video first.";
return;
}
status.textContent="Video selected: "+file.name+
". Processing engine will be connected next.";
};
</script>
</body>
</html>
