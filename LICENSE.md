Index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Block Insure - Crypto Insurance Protocol</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <nav>
        <div class="logo">BLOCK INSURE</div>
        <div class="nav-links">
            <a href="#about">About</a>
            <a href="docs.html">Docs</a>
            <a href="whitepaper.html">Whitepaper</a>
            <button id="connectWallet">Connect Wallet</button>
        </div>
    </nav>

    <header>
        <h1>Decentralized Crypto Insurance</h1>
        <p>Secure your digital assets against hacks, theft, and accidents</p>
    </header>

    <section id="features">
        <!-- Add feature cards -->
    </section>

    <script src="https://cdn.jsdelivr.net/npm/web3@1.5.2/dist/web3.min.js"></script>
    <script src="js/app.js"></script>
</body>
</html>

css/style.css

:root {
    --deep-blue: #0A1A2F;
    --accent-grey: #E0E0E0;
}

body {
    background: var(--deep-blue);
    color: var(--accent-grey);
    font-family: 'Arial', sans-serif;
}

nav {
    padding: 1rem 5%;
    background: rgba(10, 26, 47, 0.9);
    display: flex;
    justify-content: space-between;
}

.logo {
    font-weight: bold;
    font-size: 1.5rem;
}

js/app.js

// Wallet connection
document.getElementById('connectWallet').addEventListener('click', async () => {
    if (window.ethereum) {
        try {
            const accounts = await ethereum.request({ method: 'eth_requestAccounts' });
            console.log("Connected:", accounts[0]);
        } catch (error) {
            console.error("Connection failed:", error);
        }
    } else {
        alert("Please install MetaMask!");
    }
});
