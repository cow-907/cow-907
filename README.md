<!-- Header Section -->

<p align="center">
  <img src="gif/x.gif" alt="Deskripsi GIF">

</p>



## “Program yang baik bukanlah yang rumit, tapi yang mudah dipahami oleh manusia.” 



<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer&text=Good%20Job%20!!!&fontSize=16&fontColor=fff&animation=twinkling"/>
</div>

<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AI Matrix Loader</title>
  <style>
    /* Styling dasar untuk halaman (agar terlihat di tengah & gelap) */
    body {
      background-color: #111; /* Background gelap untuk efek matrix */
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      margin: 0;
    }

    .ai-matrix-loader {
      width: 120px;
      height: 160px;
      margin: 30px auto;
      position: relative;
      perspective: 800px;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 5px;
    }

    .digit {
      color: #00ff88;
      font-family: monospace;
      font-size: 18px;
      text-align: center;
      text-shadow: 0 0 5px #00ff88;
      animation:
        matrix-fall 2s infinite,
        matrix-flicker 0.5s infinite;
      opacity: 0;
    }

    .digit:nth-child(1) { animation-delay: 0.1s; }
    .digit:nth-child(2) { animation-delay: 0.3s; }
    .digit:nth-child(3) { animation-delay: 0.5s; }
    .digit:nth-child(4) { animation-delay: 0.7s; }
    .digit:nth-child(5) { animation-delay: 0.9s; }
    .digit:nth-child(6) { animation-delay: 1.1s; }
    .digit:nth-child(7) { animation-delay: 1.3s; }
    .digit:nth-child(8) { animation-delay: 1.5s; }
    /* Saya tambahkan yang ke-9 agar grid 3x3 terisi penuh */
    .digit:nth-child(9) { animation-delay: 1.7s; } 

    .glow {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: radial-gradient(
        circle,
        rgba(0, 255, 136, 0.1) 0%,
        transparent 70%
      );
      animation: matrix-pulse 2s infinite;
      z-index: -1; /* Agar glow berada di belakang angka */
    }

    @keyframes matrix-fall {
      0% {
        transform: translateY(-50px) rotateX(90deg);
        opacity: 0;
      }
      20%,
      80% {
        transform: translateY(0) rotateX(0deg);
        opacity: 0.8;
      }
      100% {
        transform: translateY(50px) rotateX(-90deg);
        opacity: 0;
      }
    }

    @keyframes matrix-flicker {
      0%, 19%, 21%, 100% { opacity: 0.8; }
      20% { opacity: 0.2; }
    }

    @keyframes matrix-pulse {
      0%, 100% { opacity: 0.3; }
      50% { opacity: 0.7; }
    }
    
  </style>
</head>
<body>

  <div class="ai-matrix-loader">
    <div class="glow"></div>
    <div class="digit">1</div>
    <div class="digit">0</div>
    <div class="digit">1</div>
    <div class="digit">0</div>
    <div class="digit">1</div>
    <div class="digit">0</div>
    <div class="digit">1</div>
    <div class="digit">0</div>
    <div class="digit">1</div>
  </div>

</body>
</html>
