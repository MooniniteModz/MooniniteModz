# Hey there - I'm Mooninite

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pixel Perfect Mooninite Somersault</title>
    <style>
        body {
            background: #0a0a0a;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
            image-rendering: pixelated;
        }

        .animation-container {
            width: 100%;
            height: 400px;
            position: relative;
        }

        .mooninite-wrapper {
            position: absolute;
            animation: moveAcross 6s linear infinite;
            top: 150px;
        }

        .mooninite {
            width: 80px;
            height: 100px;
            position: relative;
            animation: somersault 1.5s linear infinite;
            transform-origin: center center;
        }

        /* Create pixel grid */
        .pixel {
            position: absolute;
            width: 8px;
            height: 8px;
        }

        /* Pink body pixels - 7x7 square */
        .body-pixel {
            background: #FF00FF;
        }

        /* Blue pixels for features */
        .blue-pixel {
            background: #0066FF;
        }

        /* Body - main pink square (7x7 grid) */
        .body-pixel:nth-child(1) { top: 16px; left: 16px; }
        .body-pixel:nth-child(2) { top: 16px; left: 24px; }
        .body-pixel:nth-child(3) { top: 16px; left: 32px; }
        .body-pixel:nth-child(4) { top: 16px; left: 40px; }
        .body-pixel:nth-child(5) { top: 16px; left: 48px; }
        .body-pixel:nth-child(6) { top: 16px; left: 56px; }
        .body-pixel:nth-child(7) { top: 16px; left: 64px; }

        .body-pixel:nth-child(8) { top: 24px; left: 16px; }
        .body-pixel:nth-child(9) { top: 24px; left: 24px; }
        .body-pixel:nth-child(10) { top: 24px; left: 32px; }
        .body-pixel:nth-child(11) { top: 24px; left: 40px; }
        .body-pixel:nth-child(12) { top: 24px; left: 48px; }
        .body-pixel:nth-child(13) { top: 24px; left: 56px; }
        .body-pixel:nth-child(14) { top: 24px; left: 64px; }

        .body-pixel:nth-child(15) { top: 32px; left: 16px; }
        .body-pixel:nth-child(16) { top: 32px; left: 24px; }
        .body-pixel:nth-child(17) { top: 32px; left: 32px; }
        .body-pixel:nth-child(18) { top: 32px; left: 40px; }
        .body-pixel:nth-child(19) { top: 32px; left: 48px; }
        .body-pixel:nth-child(20) { top: 32px; left: 56px; }
        .body-pixel:nth-child(21) { top: 32px; left: 64px; }

        .body-pixel:nth-child(22) { top: 40px; left: 16px; }
        .body-pixel:nth-child(23) { top: 40px; left: 24px; }
        .body-pixel:nth-child(24) { top: 40px; left: 32px; }
        .body-pixel:nth-child(25) { top: 40px; left: 40px; }
        .body-pixel:nth-child(26) { top: 40px; left: 48px; }
        .body-pixel:nth-child(27) { top: 40px; left: 56px; }
        .body-pixel:nth-child(28) { top: 40px; left: 64px; }

        .body-pixel:nth-child(29) { top: 48px; left: 16px; }
        .body-pixel:nth-child(30) { top: 48px; left: 24px; }
        .body-pixel:nth-child(31) { top: 48px; left: 32px; }
        .body-pixel:nth-child(32) { top: 48px; left: 40px; }
        .body-pixel:nth-child(33) { top: 48px; left: 48px; }
        .body-pixel:nth-child(34) { top: 48px; left: 56px; }
        .body-pixel:nth-child(35) { top: 48px; left: 64px; }

        .body-pixel:nth-child(36) { top: 56px; left: 16px; }
        .body-pixel:nth-child(37) { top: 56px; left: 24px; }
        .body-pixel:nth-child(38) { top: 56px; left: 32px; }
        .body-pixel:nth-child(39) { top: 56px; left: 40px; }
        .body-pixel:nth-child(40) { top: 56px; left: 48px; }
        .body-pixel:nth-child(41) { top: 56px; left: 56px; }
        .body-pixel:nth-child(42) { top: 56px; left: 64px; }

        .body-pixel:nth-child(43) { top: 64px; left: 16px; }
        .body-pixel:nth-child(44) { top: 64px; left: 24px; }
        .body-pixel:nth-child(45) { top: 64px; left: 32px; }
        .body-pixel:nth-child(46) { top: 64px; left: 40px; }
        .body-pixel:nth-child(47) { top: 64px; left: 48px; }
        .body-pixel:nth-child(48) { top: 64px; left: 56px; }
        .body-pixel:nth-child(49) { top: 64px; left: 64px; }

        /* Blue angry V eyebrows */
        .eyebrow-l1 { top: 24px; left: 24px; }
        .eyebrow-l2 { top: 32px; left: 32px; }
        
        .eyebrow-r1 { top: 24px; left: 56px; }
        .eyebrow-r2 { top: 32px; left: 48px; }

        /* Blue mouth/frown */
        .mouth1 { top: 48px; left: 32px; }
        .mouth2 { top: 48px; left: 40px; }
        .mouth3 { top: 48px; left: 48px; }

        /* Blue arms */
        .arm-l1 { top: 40px; left: 8px; }
        .arm-l2 { top: 40px; left: 0px; }
        
        .arm-r1 { top: 40px; left: 72px; }
        .arm-r2 { top: 40px; left: 80px; }

        /* Blue legs */
        .leg-l1 { top: 72px; left: 32px; }
        .leg-l2 { top: 80px; left: 32px; }
        .leg-l3 { top: 88px; left: 24px; }
        .leg-l4 { top: 88px; left: 32px; }
        
        .leg-r1 { top: 72px; left: 48px; }
        .leg-r2 { top: 80px; left: 48px; }
        .leg-r3 { top: 88px; left: 48px; }
        .leg-r4 { top: 88px; left: 56px; }

        @keyframes moveAcross {
            0% {
                left: -100px;
            }
            100% {
                left: calc(100% + 100px);
            }
        }

        @keyframes somersault {
            0% { transform: rotate(0deg); }
            25% { transform: rotate(90deg); }
            50% { transform: rotate(180deg); }
            75% { transform: rotate(270deg); }
            100% { transform: rotate(360deg); }
        }

        .mooninite-wrapper:nth-child(2) {
            animation-delay: 2s;
        }

        .mooninite-wrapper:nth-child(3) {
            animation-delay: 4s;
        }

        /* Glow effect */
        .body-pixel {
            box-shadow: 0 0 2px #FF00FF;
        }
        
        .blue-pixel {
            box-shadow: 0 0 2px #0066FF;
        }
    </style>
</head>
<body>
    <div class="animation-container">
        <!-- First Mooninite -->
        <div class="mooninite-wrapper">
            <div class="mooninite">
                <!-- Pink body pixels -->
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                
                <!-- Blue eyebrows -->
                <div class="pixel blue-pixel eyebrow-l1"></div>
                <div class="pixel blue-pixel eyebrow-l2"></div>
                <div class="pixel blue-pixel eyebrow-r1"></div>
                <div class="pixel blue-pixel eyebrow-r2"></div>
                
                <!-- Blue mouth -->
                <div class="pixel blue-pixel mouth1"></div>
                <div class="pixel blue-pixel mouth2"></div>
                <div class="pixel blue-pixel mouth3"></div>
                
                <!-- Blue arms -->
                <div class="pixel blue-pixel arm-l1"></div>
                <div class="pixel blue-pixel arm-l2"></div>
                <div class="pixel blue-pixel arm-r1"></div>
                <div class="pixel blue-pixel arm-r2"></div>
                
                <!-- Blue legs -->
                <div class="pixel blue-pixel leg-l1"></div>
                <div class="pixel blue-pixel leg-l2"></div>
                <div class="pixel blue-pixel leg-l3"></div>
                <div class="pixel blue-pixel leg-l4"></div>
                <div class="pixel blue-pixel leg-r1"></div>
                <div class="pixel blue-pixel leg-r2"></div>
                <div class="pixel blue-pixel leg-r3"></div>
                <div class="pixel blue-pixel leg-r4"></div>
            </div>
        </div>
        
        <!-- Second Mooninite -->
        <div class="mooninite-wrapper">
            <div class="mooninite">
                <!-- Repeat all pixels -->
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                
                <div class="pixel blue-pixel eyebrow-l1"></div>
                <div class="pixel blue-pixel eyebrow-l2"></div>
                <div class="pixel blue-pixel eyebrow-r1"></div>
                <div class="pixel blue-pixel eyebrow-r2"></div>
                <div class="pixel blue-pixel mouth1"></div>
                <div class="pixel blue-pixel mouth2"></div>
                <div class="pixel blue-pixel mouth3"></div>
                <div class="pixel blue-pixel arm-l1"></div>
                <div class="pixel blue-pixel arm-l2"></div>
                <div class="pixel blue-pixel arm-r1"></div>
                <div class="pixel blue-pixel arm-r2"></div>
                <div class="pixel blue-pixel leg-l1"></div>
                <div class="pixel blue-pixel leg-l2"></div>
                <div class="pixel blue-pixel leg-l3"></div>
                <div class="pixel blue-pixel leg-l4"></div>
                <div class="pixel blue-pixel leg-r1"></div>
                <div class="pixel blue-pixel leg-r2"></div>
                <div class="pixel blue-pixel leg-r3"></div>
                <div class="pixel blue-pixel leg-r4"></div>
            </div>
        </div>
        
        <!-- Third Mooninite -->
        <div class="mooninite-wrapper">
            <div class="mooninite">
                <!-- Repeat all pixels -->
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                <div class="pixel body-pixel"></div>
                
                <div class="pixel blue-pixel eyebrow-l1"></div>
                <div class="pixel blue-pixel eyebrow-l2"></div>
                <div class="pixel blue-pixel eyebrow-r1"></div>
                <div class="pixel blue-pixel eyebrow-r2"></div>
                <div class="pixel blue-pixel mouth1"></div>
                <div class="pixel blue-pixel mouth2"></div>
                <div class="pixel blue-pixel mouth3"></div>
                <div class="pixel blue-pixel arm-l1"></div>
                <div class="pixel blue-pixel arm-l2"></div>
                <div class="pixel blue-pixel arm-r1"></div>
                <div class="pixel blue-pixel arm-r2"></div>
                <div class="pixel blue-pixel leg-l1"></div>
                <div class="pixel blue-pixel leg-l2"></div>
                <div class="pixel blue-pixel leg-l3"></div>
                <div class="pixel blue-pixel leg-l4"></div>
                <div class="pixel blue-pixel leg-r1"></div>
                <div class="pixel blue-pixel leg-r2"></div>
                <div class="pixel blue-pixel leg-r3"></div>
                <div class="pixel blue-pixel leg-r4"></div>
            </div>
        </div>
    </div>
</body>
</html>
  
  [![GitHub followers](https://img.shields.io/github/followers/MooniniteModz?style=for-the-badge&logo=github&color=00D4AA)](https://github.com/MooniniteModz)
  [![GitHub stars](https://img.shields.io/github/stars/MooniniteModz?style=for-the-badge&logo=github&color=FFD700)](https://github.com/MooniniteModz)
  [![Profile views](https://komarev.com/ghpvc/?username=MooniniteModz&style=for-the-badge&color=00D4AA)](https://github.com/MooniniteModz)

</div>

---

## 🛠️Tech Stack, Tools, and interests

<div align="center">

### Languages & Frameworks
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)

### Cloud & DevOps
![Azure](https://img.shields.io/badge/Microsoft_Azure-0089D0?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![AWS](https://img.shields.io/badge/Amazon_AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326ce5?style=for-the-badge&logo=kubernetes&logoColor=white)

### Databases & Tools
![SQL Server](https://img.shields.io/badge/Microsoft%20SQL%20Server-CC2927?style=for-the-badge&logo=microsoft%20sql%20server&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

</div>

---

## 📊 GitHub Stats

<div align="center">
  
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=MooniniteModz&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=MooniniteModz&layout=compact&langs_count=8&theme=tokyonight"/>

</div>

<div align="center">
  
  [![GitHub Streak](https://streak-stats.demolab.com/?user=MooniniteModz&theme=tokyonight)](https://git.io/streak-stats)

</div>

---

## 🏆 Featured Projects

<div align="center">

[![TradeNetics](https://github-readme-stats.vercel.app/api/pin/?username=MooniniteModz&repo=TradeNetics&theme=tokyonight)](https://github.com/MooniniteModz/TradeNetics)
[![PST-Fuze](https://github-readme-stats.vercel.app/api/pin/?username=MooniniteModz&repo=PST-Fuze&theme=tokyonight)](https://github.com/MooniniteModz/PST-Fuze)

</div>

###  TradeNetics
**AI-Powered Cryptocurrency Trading Bot with ML.NET**
- Machine learning classification for trading decisions
- Real-time Binance API integration
- Technical analysis with RSI, MACD, Bollinger Bands
- Built with C# and ML.NET for maximum performance

###  PST-Fuze  
**Cross-Platform PST File Management Tool**
- Avalonia-based desktop application
- Works on Windows, macOS, and Linux
- No dependency on Microsoft Outlook
- Built for modern .NET development

---

## ⌨️ Ergonomic Setup

FIrst time meessing with a split orthokeyboard. Verry much enjoying it so far..........

### 🌙 **ZSA Moonlander** - Split Ortholinear Keyboard
- **Custom Colemak layout** optimized for C# and PowerShell development
- **Dedicated VS Code layer** with IDE shortcuts and debugging controls
- **PowerShell workflow optimization** for pipeline and cmdlet development
- **RSI prevention** through proper ergonomic design

*Check out my [keyboard layout documentation](https://github.com/MooniniteModz/NVim-Config) for the full setup!*

---

## 📈 Activity Graph

[![MooniniteModz's github activity graph](https://github-readme-activity-graph.vercel.app/graph?username=MooniniteModz&theme=tokyo-night)](https://github.com/ashutosh00710/github-readme-activity-graph)

---

## 📫 Let's Connect!

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/your-profile)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://x.com/mooniNitemodz/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:MooniniteModz@proton.me)

</div>

---

<div align="center">
  
  **Thanks for visiting! Feel free to explore my repositories and don't hesitate to reach out if you want to collaborate on something awesome! 🚀**
  
  ![Wave](https://raw.githubusercontent.com/mayhemantt/mayhemantt/Update/svg/Bottom.svg)

</div>

---

<div align="center">
  <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight" />
</div>
