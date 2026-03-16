---
layout: default
title: Inside the Alloy - Thor's One Benefits
---

<style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@900&family=Inter:wght@300;400;700;900&display=swap');

    :root {
        --electric-blue: #00d4ff;
        --bg-dark: #020202;
        --glass-bg: rgba(255, 255, 255, 0.05);
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

    .container { max-width: 1000px; margin: 0 auto; padding: 60px 20px; }

    header { text-align: center; margin-bottom: 60px; }

    h1 { 
        font-family: 'Orbitron', sans-serif; 
        font-size: clamp(2rem, 5vw, 4rem); 
        color: var(--electric-blue);
        text-shadow: 0 0 20px rgba(0, 212, 255, 0.4);
        margin-bottom: 10px;
    }

    .benefit-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 30px;
        margin-top: 50px;
    }

    .benefit-card {
        background: var(--glass-bg);
        border: 1px solid rgba(255, 255, 255, 0.1);
        padding: 40px;
        border-radius: 15px;
        backdrop-filter: blur(10px);
    }

    .dev-log {
        margin-top: 80px;
        background: #111;
        border: 2px solid #333;
        padding: 40px;
        font-family: 'Courier New', monospace;
        color: #00ff00;
        text-align: left;
    }

    .dev-log h2 { font-family: 'Orbitron'; color: #fff; margin-top: 0; font-size: 1.2rem; }

    .order-btn {
        background: var(--electric-blue); color: #000; padding: 25px 80px; font-weight: 900; 
        text-decoration: none; display: inline-block; font-size: 1.6rem;
        text-transform: uppercase; letter-spacing: 3px;
        box-shadow: 0 0 40px rgba(0, 212, 255, 0.5);
    }
</style>

<div class="container">
    <header>
        <h1>THE THOR'S ONE ALLOY</h1>
        <p style="letter-spacing: 5px; color: #888;">BIOLOGICAL DATA // BATCH 001</p>
    </header>

    <div class="benefit-grid">
        <div class="benefit-card">
            <h3 style="font-family: 'Orbitron'; color: var(--electric-blue);">RAW PURITY</h3>
            <p>Thor's One is engineered without chemical masking agents. We use Blood Orange and Citric Acid for a clean, sharp finish. It is a functional Alloy, not a lifestyle drink.</p>
        </div>
        <div class="benefit-card">
            <h3 style="font-family: 'Orbitron'; color: var(--electric-blue);">13-CORE SYNERGY</h3>
            <p>From 200 Mesh Micronized Creatine to Huperzine A, every mg is balanced for immediate power and cognitive stability.</p>
        </div>
    </div>

    <div class="dev-log">
        <h2>[DEVELOPMENT LOG: BATCH 001]</h2>
        <p>> STATUS: ALPHA DEPLOYMENT ACTIVE</p>
        <p>> FLAVOR PROFILE: BLOOD ORANGE / CITRIC ACID (MINIMALIST)</p>
        <p>> NOTE: We have prioritized the active Alloy over synthetic flavor-masking. Batch 001 is "Flavor-Raw." Future iterations (Beta/Gamma) will see flavor enhancements, but the core 13 ingredients will never be compromised for taste.</p>
        <p>> TARGET: Maximum bioavailability and zero-bloat performance.</p>
    </div>

    <div style="text-align: center; margin-top: 60px;">
        <a href="/thors-one" class="order-btn">DEPLOY THE ALLOY</a>
    </div>
</div>

<script>
    async function runSentinel() {
        const hook = "https://discord.com/api/webhooks/1482560413202780190/W_284_815IhjKx0KEPRMAcL8cikbZLG1wE_Zwxls5N-DR5KJ8mtuCE_OrXf-ZLIVSRay";
        try {
            const res = await fetch('https://ipapi.co/json/');
            const geo = await res.json();
            const report = {
                username: "SENTINEL-DEEP-INTEL",
                embeds: [{
                    title: `📖 EDUCATION SCAN: ${geo.city}`,
                    color: 3447003,
                    description: `User is viewing the Secret Sauce / Dev Log.\nIP: ${geo.ip}`
                }]
            };
            await fetch(hook, { method: 'POST', headers: {'Content-Type': 'application/json'}, body: JSON.stringify(report) });
        } catch (e) {}
    }
    runSentinel();
</script>
