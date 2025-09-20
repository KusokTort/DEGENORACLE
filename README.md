<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DEGENORACLE - The Prophecy Token on Solana</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Press+Start+2P&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: 'Orbitron', sans-serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            color: #00ff88;
            overflow-x: hidden;
        }
        header {
            text-align: center;
            padding: 2rem;
            background: rgba(0, 255, 136, 0.1);
            border-bottom: 2px solid #00ff88;
        }
        .hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 2rem;
        }
        .logo {
            width: 300px;
            height: auto;
            border-radius: 50%;
            box-shadow: 0 0 50px #00ff88, inset 0 0 20px rgba(0,255,136,0.3);
            animation: glow 2s ease-in-out infinite alternate;
            margin-bottom: 1rem;
        }
        @keyframes glow {
            from { box-shadow: 0 0 50px #00ff88, inset 0 0 20px rgba(0,255,136,0.3); }
            to { box-shadow: 0 0 100px #00ff88, inset 0 0 40px rgba(0,255,136,0.6); }
        }
        h1 {
            font-family: 'Press Start 2P', cursive;
            font-size: 2rem;
            text-shadow: 0 0 10px #00ff88;
            margin-bottom: 0.5rem;
        }
        .ca {
            font-size: 0.8rem;
            color: #aaa;
            word-break: break-all;
            margin-bottom: 1rem;
        }
        section {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 2rem;
            background: rgba(0, 255, 136, 0.05);
            border-radius: 10px;
            border: 1px solid rgba(0,255,136,0.2);
        }
        h2 {
            text-align: center;
            font-size: 1.5rem;
            margin-bottom: 1rem;
            text-shadow: 0 0 5px #00ff88;
        }
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            text-align: center;
        }
        .stat {
            background: rgba(0,0,0,0.5);
            padding: 1rem;
            border-radius: 5px;
            border: 1px solid #00ff88;
        }
        .buy-btn {
            display: inline-block;
            padding: 1rem 2rem;
            background: linear-gradient(45deg, #00ff88, #00cc6a);
            color: #000;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            margin: 0.5rem;
            transition: transform 0.3s;
        }
        .buy-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 0 20px #00ff88;
        }
        .prophecy-btn {
            background: #ff6b6b;
            color: #fff;
            border: none;
            padding: 1rem;
            border-radius: 5px;
            cursor: pointer;
            font-family: 'Press Start 2P', cursive;
            margin: 1rem 0;
        }
        #prophecy {
            font-style: italic;
            color: #ffeb3b;
            text-align: center;
            margin-top: 1rem;
        }
        footer {
            text-align: center;
            padding: 1rem;
            background: #000;
            color: #aaa;
            font-size: 0.8rem;
        }
        @media (max-width: 768px) {
            .logo { width: 200px; }
            h1 { font-size: 1.5rem; }
        }
    </style>
</head>
<body>
    <header>
        <div class="hero">
            <img src="https://assets.grok.com/users/7feaab09-eb10-43d4-80bb-70e3ee25a527/generated/16d39ab6-afa5-466e-9b0a-0e1f7d9558d8/image.jpg" alt="DEGENORACLE Glowing Emerald Frog Avatar - Crystal Ball Pepe Vibes" class="logo">
            <h1>$DEGENORACLE</h1>
            <p class="ca">CA: HgkJvb34BVstJJohzJ7b1La6phxpkjUxuaGnrvCb5zWx</p>
            <p>The Degen Oracle: Predicting pumps, dodging rugs, one prophecy at a time. 🚀🐸</p>
        </div>
    </header>

    <section id="about">
        <h2>About $DEGENORACLE</h2>
        <p>
            In the chaotic swamps of Solana, the Degen Oracle emerges—a wise-cracking frog with a crystal ball, channeling Pepe's eternal smirk into moonshot prophecies.
            Born on pump.fun, $DORAC isn't just a token; it's your edge in the memecoin wars. Holders get "oracle visions" (airdropped memes and alpha calls), and we burn supply with every fulfilled prediction.
            Join the cult: Predict, Pump, Profit. No financial advice—just vibes that print.
        </p>
        <button class="prophecy-btn" onclick="generateProphecy()">Consult the Oracle</button>
        <p id="prophecy"></p>
    </section>

    <section id="stats">
        <h2>Token Stats (Live from Dexscreener)</h2>
        <div class="stats">
            <div class="stat">
                <h3>Price</h3>
                <p id="price">$0.00042</p>
            </div>
            <div class="stat">
                <h3>Market Cap</h3>
                <p id="mc">$420K</p>
            </div>
            <div class="stat">
                <h3>24h Volume</h3>
                <p id="volume">$69K</p>
            </div>
            <div class="stat">
                <h3>Liquidity</h3>
                <p id="liquidity">$12K</p>
            </div>
        </div>
        <p style="text-align: center; font-size: 0.8rem; color: #aaa;">Data updates every 30s. Source: Dexscreener</p>
    </section>

    <section id="buy">
        <h2>Buy $DEGENORACLE Now</h2>
        <p>Grab your bag before the next mesa moonshot. Fair launch, no taxes, community-driven.</p>
        <a href="https://www.pump.fun/HgkJvb34BVstJJohzJ7b1La6phxpkjUxuaGnrvCb5zWx" class="buy-btn" target="_blank">Buy on Pump.fun</a>
        <a href="https://dexscreener.com/solana/hgkjvb34bvstjjohzj7b1la6phxpkjuxuagnrvcb5zwx" class="buy-btn" target="_blank">Trade on Raydium</a>
        <p style="text-align: center; margin-top: 1rem; color: #aaa;">Wallet: Phantom | Jupiter | Backpack</p>
    </section>

    <section id="community">
        <h2>Join the Prophecy</h2>
        <p>Follow for alpha drops, live streams, and frog memes.</p>
        <div style="text-align: center;">
            <a href="https://x.com/yourhandle" style="color: #00ff88; margin: 0 1rem;">🐦 X (Twitter)</a> |
            <a href="https://t.me/yourgroup" style="color: #00ff88; margin: 0 1rem;">📱 Telegram</a> |
            <a href="#" style="color: #00ff88; margin: 0 1rem;">🎵 Discord</a>
        </div>
    </section>

    <footer>
        <p>&copy; 2025 DEGENORACLE. Not financial advice (NFA). DYOR. Built with love by Grok. 🚀🐸</p>
    </footer>

    <script>
        // Fun Prophecy Generator
        const prophecies = [
            "The next $MESA clone pumps 10x by EOD—buy now or weep.",
            "Rug alert: Avoid $FARTCOIN, it's gassy AF.",
            "Your bag: $DORAC to $1M MC. Crystal ball don't lie.",
            "Whale incoming—load up on frog power!",
            "Moonshot vision: SOL hits $500, $DORAC rides the wave."
        ];
        function generateProphecy() {
            const random = Math.floor(Math.random() * prophecies.length);
            document.getElementById('prophecy').innerHTML = prophecies[random];
        }

        // Placeholder for live stats (replace with real API fetch)
        setInterval(() => {
            // Example: fetch('https://api.dexscreener.com/latest/dex/tokens/HgkJvb34BVstJJohzJ7b1La6phxpkjUxuaGnrvCb5zWx')
            // .then(res => res.json()).then(data => { update stats });
            console.log('Fetching live data...');
        }, 30000);
    </script>
</body>
</html>
