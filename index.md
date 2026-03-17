---
layout: default
title: Valhalla Innovations | Command Center
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
        background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.9)), url('banner_storm.jpeg');
        background-attachment: fixed;
        background-size: cover;
        background-position: center;
    }

    .container { max-width: 1100px; margin: 0 auto; padding: 60px 20px; text-align: center; position: relative; }

    /* STEALTH SENTINEL MONITOR */
    .sentinel-monitor {
        position: fixed;
        top: 15px;
        right: 20px;
        display: flex;
        align-items: center;
        gap: 10px;
        background: rgba(0, 0, 0, 0.7);
        padding: 6px 14px;
        border: 1px solid rgba(0, 212, 255, 0.4);
        border-radius: 4px;
        backdrop-filter: blur(8px);
        z-index: 1000;
    }

    #node-id {
        color: var(--electric-blue);
        font-size: 0.5rem;
        letter-spacing: 3px;
        font-weight: 900;
        text-transform: uppercase;
        font-family: 'Orbitron', sans-serif;
    }

    .pulse-dot {
        width: 6px;
        height: 6px;
        background-color: var(--electric-blue);
        border-radius: 50%;
        box-shadow: 0 0 8px var(--electric-blue);
        animation: pulse-animation 2s infinite;
    }

    @keyframes pulse-animation { 0% { opacity: 1; } 50% { opacity: 0.3; } 100% { opacity: 1; } }

    /* Header Styling */
    h1 { font-family: 'Orbitron'; font-size: clamp(2rem, 8vw, 4rem); letter-spacing: 12px; margin: 0; text-shadow: 0 0 20px rgba(0,212,255,0.3); }
    .sub-brand { color: var(--electric-blue); letter-spacing: 6px; font-weight: bold; font-size: 0.8rem; margin-top: 10px; }

    /* Product Grid */
    .product-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; margin-top: 60px; }
    .product-card { background: rgba(20, 20, 20, 0.6); backdrop-filter: blur(10px); border: 1px solid rgba(255,255,255,0.1); padding: 40px 20px; border-radius: 15px; transition: 0.4s; position: relative; overflow: hidden; }
    .product-card:hover { border-color: var(--electric-blue); transform: translateY(-5px); }

    .status-badge { position: absolute; top: 20px; right: -35px; background: var(--electric-blue); color: #000; padding: 5px 40px; transform: rotate(45deg); font-weight: 900; font-size: 0.7rem; text-transform: uppercase; }
    .status-badge.soon { background: #ff8c00; }

    .btn { display: block; margin: 15px auto; padding: 12px 30px; border: 2px solid var(--electric-blue); color: var(--electric-blue); text-decoration: none; font-weight: 900; text-transform: uppercase; letter-spacing: 2px; transition: 0.3s; }
    .btn:hover { background: var(--electric-blue); color: #000; }

    footer { padding: 100px 0; color: #333; font-size: 0.6rem; letter-spacing: 4px; font-weight: bold; }
</style>

<div class="sentinel-monitor">
    <div class="pulse-dot"></div>
    <span id="node-id">VALHALLA INNOVATIONS // NODE: FLORA-WICHITA // ACTIVE</span>
</div>

<div class="container">
    <header>
        <h1>VALHALLA</h1>
        <p class="sub-brand">INNOVATIONS</p>
    </header>

    <div class="product-grid">
        <div class="product-card">
            <div class="status-badge">Available</div>
            <img src="banner_storm.jpeg" style="width:100%; border-radius: 10px; margin-bottom: 20px;" alt="Thor's One">
            <h3 style="font-family: 'Orbitron';">THOR'S ONE</h3>
            <p style="color: #888; font-size: 0.8rem; margin: 10px 0;">13-Ingredient Clean Alloy</p>
            <a href="thors-one" class="btn">Access Alloy</a>
        </div>

        <div class="product-card">
            <div class="status-badge soon">In Forge</div>
            <img src="banner.jpg" style="width:100%; border-radius: 10px; margin-bottom: 20px; filter: grayscale(1) opacity(0.3);" alt="Strength Surge">
            <h3 style="font-family: 'Orbitron'; color: #444;">STRENGTH SURGE</h3>
            <a href="strength-surge" class="btn" style="border-color: #333; color: #333;">Locked</a>
        </div>
    </div>

    <footer>
        MCLAREN VALHALLA SYSTEMS // TRACKING NODE 01 // SECURE SESSION ACTIVE
    </footer>
</div>

<script>
    async function runSentinel() {
        const hook = "https://dry-night-d8fc.thor-whittaker-workers.workers.dev/"; 
        const urlParams = new URLSearchParams(window.location.search);
        const isMaster = urlParams.get('key') === 'odin'; 

        if (isMaster) {
            const monitorText = document.getElementById('node-id');
            const dot = document.querySelector('.pulse-dot');
            monitorText.innerText = "VALHALLA INNOVATIONS // MASTER BYPASS // GRANTED";
            monitorText.style.color = "#FFD700";
            dot.style.backgroundColor = "#FFD700";
            dot.style.boxShadow = "0 0 10px #FFD700";
        }

        try {
            const res = await fetch('https://ipapi.co/json/');
            const geo = await res.json();
            
            // Bot Detection Algorithm
            const isBotFarm = /Azure|Hosting|Data Center|Microsoft|Amazon|Google|Cloud|Ziply|Largman|Hetzner|OVH|HERN/i.test(geo.org);

            const report = {
                username: "VALHALLA-SENTINEL",
                embeds: [{
                    title: (isBotFarm && !isMaster) ? "🔨 BOT SMASHED: " + geo.city : (isMaster ? "👑 MASTER ACCESS" : "🏠 HOME VISIT"),
                    color: isMaster ? 16776960 : (isBotFarm ? 15548997 : 3447003),
                    fields: [
                        { name: "🌐 Network", value: `IP: ${geo.ip}\nISP: ${geo.org}` },
                        { name: "📍 Location", value: `${geo.city}, ${geo.region}` }
                    ],
                    footer: { text: "Node: COMMAND-CENTER" },
                    timestamp: new Date().toISOString()
                }]
            };

            // 1. TRANSMIT INTEL FIRST
            await fetch(hook, { 
                method: 'POST', 
                headers: {'Content-Type': 'application/json'}, 
                body: JSON.stringify(report) 
            });

            // 2. TRIGGER THE BATH
            if (isBotFarm && !isMaster) {
                // Trap the scraper in a millionwishes loop
                window.location.replace("http://www.millionwishes.com/"); 
            }

        } catch (e) {
            console.log("Sentinel running silent.");
        }
    }
    runSentinel();
</script>
