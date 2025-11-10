<!DOCTYPE html>
<html lang="vi">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Thả Quẻ Kinh Dịch Huyền Bí</title>
    <style>
      body {
    background: radial-gradient(circle at center, #0d0d0d, #000);
    color: #f0e6d2;
    font-family: 'Times New Roman', serif;
    text-align: center;
    height: 100vh;
    margin: 0;
    overflow: hidden; }
      h1 {
    font-size: 2.2em;
    margin-top: 50px;
    text-shadow: 0 0 15px #f5e2a4; }
  .circle { 
    width: 200px;
    height: 200px;
    border-radius: 50%;
    border: 2px solid #c4a962;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 40px auto;
    font-size: 4em;
    text-shadow: 0 0 20px #f5e2a4;
    box-shadow: 0 0 40px #c4a962 inset, 0 0 20px #c4a962;
    animation: rotate 10s linear infinite;}
@keyframes rotate {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); } }
     button {
  background: #c4a962;
    border: none;
    color: #000;
    padding: 10px 25px;
    border-radius: 10px;
    font-weight: bold;
    cursor: pointer;
    transition: 0.3s;}
       button:hover {
    background: #f5e2a4;
    transform: scale(1.1);}
 .result {
    font-size: 1.2em;
    margin-top: 30px;
    line-height: 1.6em;
    max-width: 80%;
    margin-left: auto;
    margin-right: auto;}
  .smoke {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: url('https://i.ibb.co/6YShYWS/smoke.gif') center/cover no-repeat;
    opacity: 0.2;
    z-index: -1;}
</style>
</head>
    <body>
        <div class="smoke"></div>
        <h1>🔮 Thả Quẻ Kinh Dịch Huyền Bí 🔮</h1>
        <div class="circle" id="guaSymbol">☯</div>
        <button onclick="drawHexagram()">Thả Quẻ</button>
        <div class="result" id="result"></div>
        <script>
const hexagrams = [
  {name: "乾卦 (Càn)", symbol: "☰", meaning: "Trời – cương kiện, sáng suốt, khởi đầu, lãnh đạo."},
  {name: "坤卦 (Khôn)", symbol: "☷", meaning: "Đất – nhu thuận, bao dung, sinh trưởng vạn vật."},
  {name: "屯卦 (Truân)", symbol: "☳☵", meaning: "Khởi đầu gian nan, cần kiên định vượt qua."},
  {name: "蒙卦 (Mông)", symbol: "☵☶", meaning: "Trẻ dại, cần khai sáng trí tuệ, học hỏi đúng đạo."},
  {name: "需卦 (Nhu)", symbol: "☰☵", meaning: "Chờ đợi thời cơ, tích lũy nội lực."},
  {name: "讼卦 (Tụng)", symbol: "☵☰", meaning: "Tranh chấp, nên dùng lý trí, tránh cứng đối cứng."},
  {name: "师卦 (Sư)", symbol: "☷☵", meaning: "Quân đội, trật tự, cần người lãnh đạo minh triết."},
  {name: "比卦 (Tỷ)", symbol: "☵☷", meaning: "Gắn bó, hợp tác, đồng tâm hiệp lực thì thành công."},]
function drawHexagram() {
  const random = Math.floor(Math.random() * hexagrams.length);
  const gua = hexagrams[random];
  document.getElementById("guaSymbol").textContent = gua.symbol;
  document.getElementById("result").innerHTML = `
    <h2>${gua.name}</h2>
    <p>${gua.meaning}</p>
  `;
  const sound = new Audio('https://assets.mixkit.co/sfx/preview/mixkit-small-gong-hit-1955.mp3');
  sound.play();}
        </script>
    </body>
</html>
