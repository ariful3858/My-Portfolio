<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Md Ariful Hasan | Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body {
            /* ডার্ক গ্রেডিয়েন্ট ব্যাকগ্রাউন্ড */
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #1a1a2e 100%);
            font-family: 'Segoe UI', sans-serif;
            display: flex; justify-content: center; align-items: center;
            min-height: 100vh; margin: 0; padding: 20px;
            overflow: hidden; /* ব্যাকগ্রাউন্ড অ্যানিমেশনের জন্য */
            position: relative;
        }

        /* ব্যাকগ্রাউন্ড অ্যানিমেশন ইফেক্ট (Particle লাইক) */
        body::before {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background-image: 
                radial-gradient(white, rgba(255,255,255,.2) 2px, transparent 3px),
                radial-gradient(white, rgba(255,255,255,.15) 1px, transparent 2px),
                radial-gradient(white, rgba(255,255,255,.1) 2px, transparent 3px);
            background-size: 550px 550px, 350px 350px, 250px 250px;
            background-position: 0 0, 40px 60px, 130px 270px;
            animation: backgroundMove 60s linear infinite;
            opacity: 0.3; /* খুব সূক্ষ্ম দেখানোর জন্য */
            z-index: -1;
        }

        @keyframes backgroundMove {
            from { background-position: 0 0, 40px 60px, 130px 270px; }
            to { background-position: 550px 550px, 40px 610px, 130px 820px; }
        }

        .card {
            /* ডার্ক থিমের কার্ড */
            background: rgba(255, 255, 255, 0.05); /* হালকা স্বচ্ছ */
            backdrop-filter: blur(10px); /* গ্লাস ইফেক্ট */
            width: 100%; max-width: 380px;
            padding: 35px 25px; border-radius: 25px; text-align: center;
            box-shadow: 0 20px 40px rgba(0,0,0,0.8);
            border: 1px solid rgba(255, 255, 255, 0.1); /* সূক্ষ্ম বর্ডার */
            color: #fff; /* সব লেখা সাদা */
            position: relative;
            z-index: 1;
        }
        
        .profile-img {
            width: 110px; height: 110px; 
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%; margin: 0 auto 15px;
            display: flex; justify-content: center; align-items: center;
            border: 3px solid #4facfe; overflow: hidden;
            box-shadow: 0 0 15px rgba(79, 172, 254, 0.5); /* গ্লো ইফেক্ট */
        }
        .profile-img img { width: 100%; height: 100%; object-fit: cover; }
        
        .name-container {
            display: flex; justify-content: center; align-items: center;
            gap: 8px; margin: 10px 0 5px;
        }
        h1 { margin: 0; font-size: 24px; color: #fff; }
        .verified-badge { color: #1DA1F2; font-size: 18px; }

        /* টাইপিং অ্যানিমেশন স্টাইল - ডার্ক থিমে আরও উজ্জ্বল */
        .typing-container {
            color: #4facfe; /* উজ্জ্বল নীল */
            font-weight: 600; font-size: 16px;
            height: 20px; margin-bottom: 20px;
        }
        .typing-text::after {
            content: "|";
            animation: blink 0.7s infinite;
        }
        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }

        .work-btn {
            display: inline-block; width: 100%; padding: 12px;
            background: linear-gradient(45deg, #6a11cb, #2575fc); /* গ্রেডিয়েন্ট বাটন */
            color: white; text-decoration: none;
            border-radius: 12px; font-weight: bold; margin-bottom: 20px;
            box-sizing: border-box; transition: 0.3s;
            box-shadow: 0 4px 15px rgba(106, 17, 203, 0.4);
        }
        .work-btn:hover { 
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(106, 17, 203, 0.6);
        }

        .details-box {
            text-align: left; 
            background: rgba(255, 255, 255, 0.03); /* খুব হালকা স্বচ্ছ */
            padding: 15px;
            border-radius: 12px; margin-bottom: 20px;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }
        .info-row {
            display: flex; justify-content: space-between; padding: 8px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05); /* ডার্ক বর্ডার */
            font-size: 14px;
        }
        .info-row:last-child { border-bottom: none; }
        .label { color: #ccc; /* হালকা ধূসর */ }
        .value { font-weight: bold; color: #fff; /* সাদা */ }

        #contactBtn {
            width: 100%; padding: 14px; 
            background: #4facfe; border: none;
            color: white; border-radius: 12px; cursor: pointer;
            font-weight: bold; font-size: 16px; display: flex;
            justify-content: center; align-items: center; gap: 10px;
            transition: 0.3s;
        }
        #contactBtn:hover {
            background: #008eff;
        }

        .social-links {
            display: none; grid-template-columns: 1fr 1fr;
            gap: 12px; margin-top: 15px;
        }
        .btn {
            text-decoration: none; color: white; padding: 12px 0;
            border-radius: 10px; font-size: 14px; display: flex;
            align-items: center; justify-content: center; gap: 8px;
            width: 100%;
            transition: 0.2s;
        }
        .btn:hover { transform: scale(1.05); }

        .wa { background: #25D366; } .fb { background: #1877F2; }
        .tt { background: #010101; border: 1px solid rgba(255,255,255,0.2); } .ig { background: #E4405F; }
        
        footer { margin-top: 30px; font-size: 11px; color: #888; }
    </style>
</head>
<body>

    <div class="card">
        <div class="profile-img">
            <img src="https://miserable-orange-bduxvhe74f.edgeone.app/1000043446.jpg" alt="Profile of Md Ariful Hasan">
        </div>

        <div class="name-container">
            <h1>Md Ariful Hasan</h1> 
            <i class="fas fa-check-circle verified-badge" title="Verified Profile"></i>
        </div>
        
        <div class="typing-container">
            <span class="typing-text"></span>
        </div>

        <a href="https://kommodo.ai/i/jjpnm8A3EcIFUFiebE1l" target="_blank" class="work-btn">
            <i class="fas fa-briefcase"></i> View My Works
        </a>

        <div class="details-box">
            <div class="info-row"><span class="label">Work Experience</span><span class="value">1 Year</span></div>
            
            <div class="info-row"><span class="label">Gender</span><span class="value">Male</span></div>
            <div class="info-row"><span class="label">Age</span><span class="value">20yrs</span></div>
            
            <div class="info-row"><span class="label">Religion</span><span class="value">Islam</span></div>
            <div class="info-row"><span class="label">Region</span><span class="value">Bangladesh</span></div>
            <div class="info-row"><span class="label">Address</span><span class="value">Joypurhat</span></div>
        </div>

        <button id="contactBtn">Contact Me <i class="fas fa-chevron-down"></i></button>
        
        <div id="socialLinks" class="social-links">
            <a href="https://wa.me/8801960973858" target="_blank" class="btn wa"><i class="fab fa-whatsapp"></i> WhatsApp</a>
            <a href="https://www.facebook.com/callmedevil.0" target="_blank" class="btn fb"><i class="fab fa-facebook-f"></i> Facebook</a>
            <a href="tiktok.com/@ariful3858" target="_blank" class="btn tt"><i class="fab fa-tiktok"></i> TikTok</a>
            <a href="https://www.instagram.com/ariful_3858" target="_blank" class="btn ig"><i class="fab fa-instagram"></i> Instagram</a>
        </div>

        <footer><p>&copy; 2026 Md Ariful Hasan. All rights reserved.</p></footer>
    </div>

    <script>
        // টাইপিং অ্যানিমেশন স্ক্রিপ্ট
        const textElement = document.querySelector(".typing-text");
        const words = ["Graphics Designer", "Thumbnail Designer", "Logo Designer"];
        let wordIndex = 0;
        let charIndex = 0;
        let isDeleting = false;

        function type() {
            const currentWord = words[wordIndex];
            if (isDeleting) {
                textElement.textContent = currentWord.substring(0, charIndex - 1);
                charIndex--;
            } else {
                textElement.textContent = currentWord.substring(0, charIndex + 1);
                charIndex++;
            }

            let typeSpeed = isDeleting ? 50 : 100;

            if (!isDeleting && charIndex === currentWord.length) {
                isDeleting = true;
                typeSpeed = 2000; // লেখা শেষ হলে ২ সেকেন্ড অপেক্ষা করবে
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                wordIndex = (wordIndex + 1) % words.length;
                typeSpeed = 500;
            }

            setTimeout(type, typeSpeed);
        }

        document.addEventListener("DOMContentLoaded", type);

        // কন্টাক্ট বাটন কন্ট্রোল
        const btn = document.getElementById('contactBtn');
        const links = document.getElementById('socialLinks');
        btn.onclick = function() {
            if (links.style.display === "grid") {
                links.style.display = "none";
                btn.innerHTML = 'Contact Me <i class="fas fa-chevron-down"></i>';
            } else {
                links.style.display = "grid";
                btn.innerHTML = 'Close <i class="fas fa-chevron-up"></i>';
            }
        }
    </script>
</body>
</html>
