<h1>TON Connect</h1>
<script src="https://unpkg.com/@tonconnect/ui@latest/dist/tonconnect-ui.min.js"></script>
<div id="ton-connect"></div>
<body>
    <script>
        const tonConnectUI = new TON_CONNECT_UI.TonConnectUI({
            manifestUrl: 'https://t.me/PresaleCoin_bot/Presale>/tonconnect-manifest.json',
            buttonRootId: 'ton-connect'
        });
    </script>
    <script>
        async function connectToWallet() {
            const connectedWallet = await tonConnectUI.connectWallet();
            // Do something with connectedWallet if needed
            console.log(connectedWallet);
        }
    
        // Call the function
        connectToWallet().catch(error => {
            console.error("Error connecting to wallet:", error);
        });
    </script>
</body>
