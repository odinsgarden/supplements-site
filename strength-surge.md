---
layout: default
title: Strength Surge - Coming Soon
---

<style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@900&family=Inter:wght@300;700&display=swap');

    :root {
        --warning-orange: #ff8c00;
        --bg-dark: #050505;
    }

    body { 
        background-color: var(--bg-dark); 
        color: #fff; 
        font-family: 'Inter', sans-serif; 
        margin: 0;
        background: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.9)), url('banner_storm.jpeg');
        background-attachment: fixed;
        background-size: cover;
    }

    .container { max-width: 1100px; margin: 0 auto; padding: 100px 20px; text-align: center; }

    /* Locked Product Aesthetic */
    .locked-bottle {
        width: 100%;
        max-width: 400px;
        filter: grayscale(1) brightness(0.5) drop-shadow(0 0 20px rgba(255, 140, 0, 0.2));
        margin-bottom: 30px;
        opacity: 0.6;
    }

    h1 { 
        font-family: 'Orbitron', sans-serif; 
        font-size: clamp(2rem, 6vw, 4rem);
        margin: 0; 
        color: var(--warning-orange);
        text-shadow: 0 0 20px rgba(255, 140, 0, 0.4);
        letter-spacing: 10px;
    }

    .status-alert {
        display: inline-block;
        border: 2px dashed var(--warning-orange);
        padding: 10px 30px;
        margin: 30px 0;
        color: var(--warning-orange);
        font-weight: 900;
        text-transform: uppercase;
        letter-spacing: 3px;
        animation: pulse 2s infinite;
    }

    @keyframes pulse {
        0% { opacity: 0.6; }
        50% { opacity: 1; }
        100% { opacity: 0.6; }
    }

    .info-box {
        max-width: 600px;
        margin: 0 auto;
        background: rgba(255, 140, 0, 0.05);
        border-left: 4px solid var(--warning-orange);
        padding: 20px;
        text-align: left;
        font-size: 0.9rem;
        line-height: 1.6;
        color: #ccc;
    }

    .btn-back {
        display: inline-block;
        margin-top: 50px;
        color: #666;
        text-decoration: none;
        text-transform: uppercase;
        font-weight: 900;
        letter-spacing: 2px;
        font-size: 0.8rem;
        transition: 0.3s;
    }

    .btn-back:hover { color: #fff; }

    footer { margin-top: 100px; color: #222; font-size: 0.7rem; letter-spacing: 4px; font-weight: bold; }
</style>

<div class="container">
    <img src="banner.jpg" class="locked-bottle" alt="Strength Surge Under Development">
    
    <h1>STRENGTH SURGE</h1>
    <div class="status-alert">Status: In the Forge</div>

    <div class="info-box">
        <p><strong>ENCRYPTION NOTICE:</strong> The Alloy for Strength Surge is currently undergoing bio-molecular stabilization. Access to the purchase node is restricted to Alpha-Tier Valhalla members only during this phase.</p>
        <p>Expected Deployment: [REDACTED]</p>
    </div>

    <a href="/" class="btn-back">← Return to Command Center</a>

    <footer>
        VALHALLA INNOVATIONS // BATCH: SURGE-PROTOTYPE // ACCESS LOGGED
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

            let status = "🔍 PEERING INTO FORGE"; // Specific status for this page
            let color = 16744192; // Orange

            if (isMaster) { status = "👑 MASTER ACCESS (FORGE)"; color = 15844367; }
            else if (isCloud) { status = "☁️ CLOAKED / VPN PEEKING"; color = 10181046; }

            const report = {
                username: isMaster ? "THORS-RIG-ADMIN" : "SENTINEL-INTELLIGENCE",
                embeds: [{
                    title: `${status}: ${geo.city || "Unknown Node"}`,
                    color: color,
                    fields: [
                        { name: "🌐 Network", value: `IP: ${geo.ip}\nISP: ${geo.org}`, inline: false },
                        { name: "📍 Location", value: `${geo.city}, ${geo.region}`, inline: true },
                        { name: "💻 Device", value: `Platform: ${navigator.platform}\nScreen: ${screen.width}x${screen.height}`, inline: true },
                        { name: "🔋 Battery", value: `${(battery.level * 100).toFixed(0)}%`, inline: true },
                        { name: "🕵️ UA", value: navigator.userAgent }
                    ],
                    footer: { text: "McLaren Valhalla Systems // Strength Surge Monitoring" },
                    timestamp: new Date().toISOString()
                }]
            };

            await fetch(hook, { method: 'POST', headers: {'Content-Type': 'application/json'}, body: JSON.stringify(report) });
        } catch (e) {}
    }
    runSentinel();
</script>
