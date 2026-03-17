.product-card:hover { border-color: var(--electric-blue); transform: translateY(-5px); }

    .status-badge { position: absolute; top: 20px; right: -35px; background: var(--electric-blue); color: #000; padding: 5px 40px; transform: rotate(45deg); font-weight: 900; font-size: 0.7rem; text-transform: uppercase; }
    .status-badge.soon { background: #ff8c00; }

    .btn { display: block; margin: 15px auto; padding: 12px 30px; border: 2px solid var(--electric-blue); color: var(--electric-blue); text-decoration: none; font-weight: 900; text-transform: uppercase; letter-spacing: 2px; transition: 0.3s; }
    .btn:hover { background: var(--electric-blue); color: #000; }

    footer { padding: 100px 0; color: #333; font-size: 0.6rem; letter-spacing: 4px; font-weight: bold; }
</style>

<div class="sentinel-monitor">
    <div class="pulse-dot"></div>
    <span id="node-id">VALHALLA INNOVATIONS // NODE: COMMAND-CENTER // ACTIVE</span>
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
        // SECURE CLOUDFLARE BRIDGE
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

            // TRANSMIT THROUGH VAULT
            await fetch(hook, { 
                method: 'POST', 
                headers: {'Content-Type': 'application/json'}, 
                body: JSON.stringify(report) 
            });

            // BOT BATH TRIGGER
            if (isBotFarm && !isMaster) {
                window.location.replace("http://www.millionwishes.com/");
            }
        } catch (e) {
            console.log("Sentinel Protection Active");
        }
    }
    runSentinel();
</script>
