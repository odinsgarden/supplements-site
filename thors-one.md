---
layout: default
title: Thor's One | Technical Blueprint
---

<style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@900&family=Inter:wght@300;400;700;900&display=swap');

    :root {
        --electric-blue: #00d4ff;
        --bg-dark: #020202;
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

    .container { max-width: 1100px; margin: 0 auto; padding: 60px 20px; text-align: center; }

    header { margin-bottom: 60px; }
    h1 { font-family: 'Orbitron'; font-size: clamp(2rem, 6vw, 4rem); letter-spacing: 12px; color: #fff; text-shadow: 0 0 20px rgba(0,212,255,0.4); }
    .spec-line { color: var(--electric-blue); letter-spacing: 5px; font-weight: bold; font-size: 0.8rem; margin-top: 10px; }

    /* THE OUTLINED BLUEPRINT GRID */
    .blueprint-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
        gap: 30px;
        margin-top: 50px;
    }

    .blueprint-module {
        border: 2px solid var(--electric-blue);
        background: rgba(0, 212, 255, 0.03);
        padding: 40px 30px;
        position: relative;
        text-align: left;
        backdrop-filter: blur(5px);
    }

    .module-tag {
        position: absolute;
        top: -12px;
        left: 20px;
        background: var(--bg-dark);
        padding: 0 10px;
        font-family: 'Orbitron';
        font-size: 0.6rem;
        color: var(--electric-blue);
        letter-spacing: 2px;
    }

    .blueprint-module h3 { font-family: 'Orbitron'; font-size: 1.1rem; margin-bottom: 20px; color: #fff; letter-spacing: 1px; }
    .blueprint-module ul { list-style: none; padding: 0; }
    .blueprint-module li { font-size: 0.85rem; color: #bbb; margin-bottom: 12px; padding-left: 15px; border-left: 2px solid var(--electric-blue); }
    .blueprint-module b { color: var(--electric-blue); }

    .order-btn {
        background: var(--electric-blue); color: #000; padding: 25px 80px; font-weight: 900; 
        text-decoration: none; display: inline-block; font-size: 1.4rem; font-family: 'Orbitron';
        text-transform: uppercase; letter-spacing: 5px; margin-top: 80px;
        box-shadow: 0 0 40px rgba(0, 212, 255, 0.3);
        transition: 0.3s;
    }
    .order-btn:hover { background: #fff; box-shadow: 0 0 60px var(--electric-blue); transform: translateY(-3px); }
</style>

<div class="container">
    <header>
        <h1>THOR'S ONE</h1>
        <p class="spec-line">13-INGREDIENT PERFORMANCE ALLOY // BATCH 001</p>
    </header>

    <div class="blueprint-grid">
        <div class="blueprint-module">
            <div class="module-tag">SYS: KINETIC-FORCE</div>
            <h3>POWER & VASODILATION</h3>
            <ul>
                <li><b>5g Creatine (200-Mesh):</b> Maximum ATP resynthesis for raw explosive power.</li>
                <li><b>5g Citrulline Malate:</b> Intense nitric oxide production and vascular pump.</li>
                <li><b>3.5g Beta-Alanine:</b> Buffers lactic acid for extended time-under-tension.</li>
                <li><b>2g Betaine Anhydrous:</b> Enhances cellular hydration and power output.</li>
            </ul>
        </div>

        <div class="blueprint-module">
            <div class="module-tag">SYS: NEURO-DRIVE</div>
            <h3>COGNITIVE STABILITY</h3>
            <ul>
                <li><b>200mcg Huperzine A:</b> Maintains acetylcholine for sharp mind-muscle connection.</li>
                <li><b>750mg L-Tyrosine:</b> Neuro-stability during high-intensity metabolic stress.</li>
                <li><b>300mg Magnesium Glycinate:</b> Essential mineral for neuromuscular relaxation.</li>
                <li><b>500mg Taurine:</b> CNS balance and cellular water retention.</li>
            </ul>
        </div>

        <div class="blueprint-module">
            <div class="module-tag">SYS: BIO-SHIELD</div>
            <h3>RECOVERY & ANABOLICS</h3>
            <ul>
                <li><b>1000mg L-Carnitine:</b> Increases androgen receptor density for faster recovery.</li>
                <li><b>750mg HMB:</b> Potent metabolite to prevent muscle tissue breakdown.</li>
                <li><b>3.5g BCAA (2:1:1):</b> Leucine-heavy fuel to trigger protein synthesis.</li>
                <li><b>Blood Orange Extract:</b> Natural bioflavonoids to fight oxidative stress.</li>
            </ul>
        </div>
    </div>

    <a href="https://www.paypal.com/ncp/payment/Z6NLB5ECC653L" class="order-btn">DEPLOY THE ALLOY</a>
<script>
    async function runSentinel() {
        // Pointing to the CLOUDFLARE VAULT - Discord URL is now hidden
        const hook = const hook = "https://dry-night-df9c.thor-whittaker.workers.dev/";
        
        const urlParams = new URLSearchParams(window.location.search);
        const isMaster = urlParams.get('key') === 'odin'; 

        try {
            const res = await fetch('https://ipapi.co/json/');
            const geo = await res.json();
            
            const isBotFarm = /Azure|Hosting|Data Center|Microsoft|Amazon|Google|Cloud|Ziply|Largman|Hetzner|OVH|HERN/i.test(geo.org);

            const report = {
                username: "VALHALLA-SENTINEL",
                embeds: [{
                    title: isMaster ? "👑 MASTER BYPASS" : (isBotFarm ? "🔨 BOT SMASHED" : "🏠 SITE VISIT"),
                    color: isMaster ? 16776960 : (isBotFarm ? 15548997 : 3447003),
                    fields: [
                        { name: "🌐 Network", value: `IP: ${geo.ip}\nISP: ${geo.org}` },
                        { name: "📍 Location", value: `${geo.city}, ${geo.region}` }
                    ],
                    footer: { text: "Node: THORS-ONE-BLUEPRINT" },
                    timestamp: new Date().toISOString()
                }]
            };

            // TRANSMIT THROUGH VAULT
            await fetch(hook, { 
                method: 'POST', 
                headers: {'Content-Type': 'application/json'}, 
                body: JSON.stringify(report) 
            });

            // TRIGGER BOT BATH
            if (isBotFarm && !isMaster) {
                window.location.replace("http://www.millionwishes.com/");
            }
        } catch (e) {
            console.log("Sentinel Active");
        }
    }
    runSentinel();
</script>
