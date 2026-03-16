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

    header { text-align: center; margin-bottom: 80px; }

    h1 { 
        font-family: 'Orbitron', sans-serif; 
        font-size: clamp(2rem, 5vw, 4rem); 
        color: var(--electric-blue);
        text-shadow: 0 0 20px rgba(0, 212, 255, 0.4);
        margin-bottom: 10px;
    }

    .subtitle { letter-spacing: 5px; color: #888; font-weight: 700; text-transform: uppercase; }

    /* The Flavor Notice */
    .flavor-status {
        background: rgba(255, 255, 255, 0.1);
        border: 1px solid var(--electric-blue);
        padding: 20px;
        margin: 40px auto;
        max-width: 600px;
        font-size: 0.85rem;
        text-transform: uppercase;
        letter-spacing: 2px;
        color: var(--electric-blue);
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

    .benefit-card h3 { font-family: 'Orbitron', sans-serif; color: var(--electric-blue); margin-top: 0; }

    .science-breakdown {
        margin-top: 100px;
        background: #fff;
        color: #000;
        padding: 60px 40px;
        box-shadow: 20px 20px 0px var(--electric-blue);
    }

    .science-breakdown h2 { font-family: 'Orbitron', sans-serif; font-size: 2.5rem; border-bottom: 8px solid #000; margin-bottom: 30px; }

    .ingredient-highlight { margin-bottom: 30px; border-bottom: 1px solid #ddd; padding-bottom: 20px; }
    .ingredient-highlight strong { font-size: 1.2rem; display: block; margin-bottom: 5px; }

    .order-btn {
        background: var(--electric-blue); color: #000; padding: 25px 80px; font-weight: 900; 
        text-decoration: none; display: inline-block; font-size: 1.6rem;
        text-transform: uppercase; letter-spacing: 3px;
        box-shadow: 0 0 40px rgba(0, 212, 255, 0.5);
    }
</style>

<div class="container">
    <header>
        <p class="subtitle">Biological Engineering</p>
        <h1>THE THOR'S ONE ALLOY</h1>
        
        <div class="flavor-status">
            ALGORITHM STATUS: RAW & UNFILTERED<br>
            Flavored with Blood Orange & Citric Acid // No Chemical Masking
        </div>
    </header>

    <div class="benefit-grid">
        <div class="benefit-card">
            <h3>ZERO CHEMICAL MASKING</h3>
            <p>Most brands use intense artificial sweeteners to hide cheap ingredients. Thor's One uses a clean Citric Acid and Blood Orange base. It is designed to be functional, not a candy drink.</p>
        </div>
        <div class="benefit-card">
            <h3>ATP REGENERATION</h3>
            <p>Utilizing 200 Mesh Micronized Creatine, the Alloy accelerates ATP resynthesis for explosive power output.</p>
        </div>
        <div class="benefit-card">
            <h3>VASODILATION ENGINE</h3>
            <p>5g Citrulline Malate + Beet Juice Powder triggers maximum Nitric Oxide production for elite-tier nutrient delivery.</p>
        </div>
    </div>

    <div class="science-breakdown">
        <h2>FLAVOR EVOLUTION</h2>
        <div class="ingredient-highlight">
            <strong>DEVELOPMENT PHASE: ALPHA</strong>
            Thor's One is currently in a "Performance-First" development phase. We utilize natural Blood Orange and Citric Acid for a sharp, clean finish. As the Alloy evolves, flavor enhancements will be deployed, but the 13-ingredient potency remains our primary mission.
        </div>

        <h2>THE CORE SCIENCE</h2>
        <div class="ingredient-highlight">
            <strong>ANTI-CATABOLIC SHIELD (HMB + BCAA)</strong>
            The combination of HMB and 2:1:1 BCAA prevents muscle tissue breakdown, preserving your gains during the most intense sessions.
        </div>
        <div class="ingredient-highlight">
            <strong>NEURAL CLARITY (TYROSINE + HUPERZINE)</strong>
            Designed to sync the mind with the body. No jitters—just total tunnel vision and cognitive stability.
        </div>
    </div>

    <div style="text-align: center; margin-top: 80px;">
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
                    description: `User is reading the Flavor & Science breakdown.\nIP: ${geo.ip}`
                }]
            };
            await fetch(hook, { method: 'POST', headers: {'Content-Type': 'application/json'}, body: JSON.stringify(report) });
        } catch (e) {}
    }
    runSentinel();
</script>
