---
layout: default
title: Thor's One - Elite Performance
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

    .container { max-width: 1000px; margin: 0 auto; padding: 40px 20px; text-align: center; }

    .product-img {
        width: 100%;
        max-width: 550px;
        filter: drop-shadow(0 0 35px var(--electric-blue));
        margin-bottom: -20px;
    }

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
        letter-spacing: 6px; 
        font-size: 0.8rem; 
        color: var(--electric-blue);
        margin-top: 10px;
        font-weight: 700;
    }

    /* Supplement Facts UI */
    .supplement-facts { 
        background: #fff; 
        color: #000; 
        padding: 30px; 
        border: 4px solid #000; 
        width: 100%;
        max-width: 450px;
        margin: 40px auto;
        box-shadow: 12px 12px 0px var(--electric-blue);
        text-align: left;
    }

    .supplement-facts h2 { border-bottom: 12px solid #000; font-weight: 900; font-size: 2.4rem; margin: 0; font-family: 'Inter', sans-serif; }
    .sf-table { width: 100%; border-collapse: collapse; margin-top: 10px; }
    .sf-table td { padding: 12px 0; border-bottom: 1px solid #000; font-weight: bold; }
    .sf-header { border-bottom: 6px solid #000 !important; font-size: 1.1rem; }

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
    }

    .order-btn:hover { 
        background: var(--electric-blue); 
        color: #fff; 
        box-shadow: 0 0 60px var(--electric-blue);
        transform: translateY(-3px);
    }
</style>

<div class="container">
    <img src="banner.jpg" class="product-img" alt="Valhalla Lineup">
    
    <h1>THOR'S ONE</h1>
    <p class="tagline">MANY ARE CALLED BUT FEW ARE CHOSEN</p>
    
    <div style="margin: 40px 0;">
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
    </div>

    <footer style="margin-top: 80px; color: #444; font-size: 0.7rem; letter-spacing: 4px;">
        VALHALLA INNOVATIONS // NODE: SUPPS-01 // SECURE SESSION
    </footer>
</div>

<script>
    // Copy/Paste your runSentinel() function here to keep getting those Wichita pings!
</script>
