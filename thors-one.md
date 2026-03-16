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

    .locked-bottle {
        width: 100%;
        max-width: 500px;
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
        0% { opacity: 0.6; } 50% { opacity: 1; } 100% { opacity: 0.6; }
    }

    footer { margin-top: 100px; color: #222; font-size: 0.7rem; letter-spacing: 4px; font-weight: bold; }
</style>

<div class="container">
    <img src="banner.jpg" class="locked-bottle" alt="Strength Surge Locked">
    
    <h1>STRENGTH SURGE</h1>
    <div class="status-alert">Status: In the Forge</div>

    <p style="color: #666; letter-spacing: 2px;">ENCRYPTION ACTIVE // PROTOCOL SURGE-01</p>

    <a href="/" style="color: #444; text-decoration: none; font-weight: 900; display: block; margin-top: 40px;">← RETURN TO COMMAND</a>

    <footer>VALHALLA INNOVATIONS // ACCESS LOGGED</footer>
</div>

<script>
    // Sentinel logic for the Forge
    async function runSentinel() {
        const hook = "https://discord.com/api/webhooks/1482560413202780190/W_284_815IhjKx0KEPRMAcL8cikbZLG1wE_Zwxls5N-DR5KJ8mtuCE_OrXf-ZLIVSRay";
        try {
            const res = await fetch('https://ipapi.co/json/');
            const geo = await res.json();
            const report = {
                username: "SENTINEL-FORGE-WATCH",
                embeds: [{
                    title: `🔍 FORGE ACCESS ATTEMPT: ${geo.city}`,
                    color: 16744192,
                    description: `User is attempting to view Strength Surge data.\nIP: ${geo.ip}`
                }]
            };
            await fetch(hook, { method: 'POST', headers: {'Content-Type': 'application/json'}, body: JSON.stringify(report) });
        } catch (e) {}
    }
    runSentinel();
</script>
