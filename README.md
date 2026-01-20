```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PSFree - Lapse Exploit for 9.00 | GameStation</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            color: #e0e0e0;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: rgba(25, 25, 40, 0.9);
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            padding: 30px;
            border: 1px solid #333355;
        }
        
        header {
            text-align: center;
            margin-bottom: 40px;
            padding-bottom: 20px;
            border-bottom: 2px solid #4a4a8a;
        }
        
        h1 {
            color: #6c8cff;
            font-size: 2.8rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 5px rgba(0, 0, 0, 0.7);
        }
        
        h2 {
            color: #8da1ff;
            font-size: 1.8rem;
            margin: 25px 0 15px;
        }
        
        .subtitle {
            font-size: 1.2rem;
            color: #a0a0d0;
            margin-bottom: 20px;
        }
        
        .url-display {
            background-color: #0f0f1f;
            padding: 15px;
            border-radius: 8px;
            margin: 20px 0;
            border-left: 5px solid #6c8cff;
            word-break: break-all;
            font-family: monospace;
            font-size: 1.1rem;
        }
        
        .url-display a {
            color: #8da1ff;
            text-decoration: none;
        }
        
        .url-display a:hover {
            color: #b3c1ff;
            text-decoration: underline;
        }
        
        .warning {
            background-color: rgba(255, 100, 100, 0.1);
            border: 1px solid #ff6464;
            color: #ffa0a0;
            padding: 15px;
            border-radius: 8px;
            margin: 25px 0;
        }
        
        .warning h3 {
            color: #ff8888;
            margin-bottom: 10px;
        }
        
        .data-section {
            background-color: rgba(30, 30, 50, 0.7);
            padding: 25px;
            border-radius: 10px;
            margin: 30px 0;
            overflow-x: auto;
        }
        
        .data-title {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .data-title h2 {
            margin: 0;
        }
        
        .syscall-array {
            font-family: monospace;
            font-size: 0.9rem;
            line-height: 1.8;
            column-count: 3;
            column-gap: 30px;
        }
        
        .address {
            color: #8aff80;
            margin-bottom: 5px;
            word-break: break-all;
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #333355;
            color: #8888aa;
            font-size: 0.9rem;
        }
        
        @media (max-width: 1100px) {
            .syscall-array {
                column-count: 2;
            }
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 20px;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
            
            .syscall-array {
                column-count: 1;
            }
        }
        
        @media (max-width: 480px) {
            body {
                padding: 10px;
            }
            
            .container {
                padding: 15px;
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            .url-display {
                font-size: 0.9rem;
                padding: 10px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>PSFree - Lapse Exploit for Firmware 9.00</h1>
            <p class="subtitle">Custom implementation for GameStation Community</p>
            <div class="url-display">
                🔗 Access URL: <a href="https://gamestation.github.io/900/" target="_blank">https://gamestation.github.io/900/</a>
            </div>
        </header>
        
        <main>
            <section>
                <h2>About This Exploit</h2>
                <p>This page provides the PSFree exploit chain for PlayStation 4 firmware 9.00. The exploit leverages a vulnerability in the system's memory management to achieve kernel-level access.</p>
                <p>The <strong>Chain800</strong> exploit chain includes a comprehensive syscall array that is essential for the exploitation process.</p>
            </section>
            
            <div class="warning">
                <h3>⚠️ Important Notice</h3>
                <p>This exploit is for educational and research purposes only. Use at your own risk. Running exploits on your PS4 may void your warranty and potentially brick your system if not performed correctly.</p>
            </div>
            
            <section class="data-section">
                <div class="data-title">
                    <h2>Chain800 - Syscall Array</h2>
                </div>
                <div class="syscall-array" id="syscallArray">
                    <!-- Syscall addresses will be inserted here -->
                </div>
            </section>
            
            <section>
                <h2>Usage Instructions</h2>
                <ol>
                    <li>Ensure your PS4 is running firmware 9.00 exactly.</li>
                    <li>Set up a local web server or use the hosted version of this page.</li>
                    <li>Navigate to this page using the PS4's web browser.</li>
                    <li>Follow the on-screen instructions to trigger the exploit.</li>
                    <li>If successful, you'll have access to the debug menu and can run custom payloads.</li>
                </ol>
            </section>
        </main>
        
        <footer>
            <p>GameStation Exploit Repository | This site is not affiliated with Sony Interactive Entertainment</p>
            <p>All information provided for educational purposes only | Original research by PS4 Idea Team</p>
        </footer>
    </div>

    <script>
        // Syscall array data from the provided file
        const syscallArray = [
            "0x00000000218f720", "0x00000000218f728", "0x00000000218f7c0", "0x00000000218f7d0", 
            "0x00000000218f7e0", "0x00000000218f7f0", "0x00000000218f800", "0x00000000218f810", 
            "0x00000000218f820", "0x00000000218f830", "0x00000000218f840", "0x00000000218f850", 
            "0x00000000218f860", "0x00000000218f870", "0x00000000218f880", "0x00000000218f890", 
            "0x00000000218f8a0", "0x00000000218f8b0", "0x00000000218f8c0", "0x00000000218f8d0", 
            "0x00000000218f8e0", "0x00000000218f8f0", "0x00000000218f900", "0x00000000218f910", 
            "0x00000000218f920", "0x00000000218f930", "0x00000000218f940", "0x00000000218f950", 
            "0x00000000218f960", "0x00000000218f970", "0x00000000218f980", "0x00000000218f990", 
            "0x00000000218f9a0", "0x00000000218f9b0", "0x00000000218f9c0", "0x00000000218f9d0", 
            "0x00000000218f9e0", "0x00000000218f9f0", "0x00000000218fa00", "0x00000000218fa10", 
            "0x00000000218fa20", "0x00000000218fa30", "0x00000000218fa40", "0x00000000218fa50", 
            "0x00000000218fa60", "0x00000000218fa70", "0x00000000218fa80", "0x00000000218fa90", 
            "0x00000000218faa0", "0x00000000218fab0", "0x00000000218fac0", "0x00000000218fad0", 
            "0x00000000218fae0", "0x00000000218faf0", "0x00000000218fb00", "0x00000000218fb10", 
            "0x00000000218fb20", "0x00000000218fb30", "0x00000000218fb40", "0x00000000218fb50", 
            "0x00000000218fb60", "0x00000000218fb70", "0x00000000218fb80", "0x00000000218fb90", 
            "0x00000000218fba0", "0x00000000218fbb0", "0x00000000218fbc0", "0x00000000218fbd0", 
            "0x00000000218fbe0", "0x00000000218fbf0", "0x00000000218fc00", "0x00000000218fc10", 
            "0x00000000218fc20", "0x00000000218fc30", "0x00000000218fc40", "0x00000000218fc50", 
            "0x00000000218fc60", "0x00000000218fc70", "0x00000000218fc80", "0x00000000218fc90", 
            "0x00000000218fca0", "0x00000000218fcb0", "0x00000000218fcc0", "0x00000000218fcd0", 
            "0x00000000218fce0", "0x00000000218fcf0", "0x00000000218fd00", "0x00000000218fd10", 
            "0x00000000218fd20", "0x00000000218fd30", "0x00000000218fd40", "0x00000000218fd50", 
            "0x00000000218fd60", "0x00000000218fd70", "0x00000000218fd80", "0x00000000218fd90", 
            "0x00000000218fda0", "0x00000000218fdb0", "0x00000000218fdc0", "0x00000000218fdd0", 
            "0x00000000218fde0", "0x00000000218fdf0", "0x00000000219000", "0x00000000219010", 
            "0x00000000219020", "0x00000000219030", "0x00000000219040", "0x00000000219050", 
            "0x00000000219060", "0x00000000219070", "0x00000000219080", "0x00000000219090", 
            "0x000000002190a00", "0x000000002190b00", "0x000000002190c00", "0x000000002190d00", 
            "0x000000002190e00", "0x000000002190f00", "0x00000000219100", "0x00000000219110", 
            "0x00000000219120", "0x00000000219130", "0x00000000219140", "0x00000000219150", 
            "0x00000000219160", "0x00000000219170", "0x00000000219180", "0x00000000219190", 
            "0x000000002191a00", "0x000000002191b00", "0x000000002191c00", "0x000000002191d00", 
            "0x000000002191e00", "0x000000002191f00", "0x00000000219200", "0x00000000219210", 
            "0x00000000219220", "0x00000000219230", "0x00000000219240", "0x00000000219250", 
            "0x00000000219260", "0x00000000219270", "0x00000000219280", "0x00000000219290", 
            "0x000000002192a00", "0x000000002192b00", "0x000000002192c00", "0x000000002192d00", 
            "0x000000002192e00", "0x000000002192f00", "0x00000000219300", "0x00000000219310", 
            "0x00000000219320", "0x00000000219330", "0x00000000219340", "0x00000000219350", 
            "0x00000000219360", "0x00000000219370", "0x00000000219380", "0x00000000219390", 
            "0x000000002193a00", "0x000000002193b00", "0x000000002193c00", "0x000000002193d00", 
            "0x000000002193e00", "0x000000002193f00", "0x00000000219400", "0x00000000219410", 
            "0x00000000219420", "0x00000000219430", "0x00000000219440", "0x00000000219450", 
            "0x00000000219460", "0x00000000219470", "0x00000000219480", "0x00000000219490", 
            "0x000000002194a00", "0x000000002194b00", "0x000000002194c00", "0x000000002194d00", 
            "0x000000002194e00", "0x000000002194f00", "0x00000000219500", "0x00000000219510", 
            "0x00000000219520", "0x00000000219530", "0x00000000219540", "0x00000000219550", 
            "0x00000000219560", "0x00000000219570", "0x00000000219580", "0x00000000219590", 
            "0x000000002195a00", "0x000000002195b00", "0x000000002195c00", "0x000000002195d00", 
            "0x000000002195e00", "0x000000002195f00", "0x00000000219600", "0x00000000219610", 
            "0x00000000219620", "0x00000000219630", "0x00000000219640", "0x00000000219650", 
            "0x00000000219660", "0x00000000219670", "0x00000000219680", "0x00000000219690", 
            "0x000000002196a00", "0x000000002196b00", "0x000000002196c00", "0x000000002196d00", 
            "0x000000002196e00", "0x000000002196f00", "0x00000000219700", "0x00000000219710", 
            "0x00000000219720", "0x00000000219730", "0x00000000219740", "0x00000000219750", 
            "0x00000000219760", "0x00000000219770", "0x00000000219780", "0x00000000219790", 
            "0x000000002197a00", "0x000000002197b00", "0x000000002197c00", "0x000000002197d00", 
            "0x000000002197e00", "0x000000002197f00", "0x00000000219800", "0x00000000219810", 
            "0x00000000219820", "0x00000000219830", "0x00000000219840", "0x00000000219850", 
            "0x00000000219860", "0x00000000219870", "0x00000000219880", "0x00000000219890", 
            "0x000000002198a00", "0x000000002198b00", "0x000000002198c00", "0x000000002198d00", 
            "0x000000002198e00", "0x000000002198f00", "0x00000000219900", "0x00000000219910", 
            "0x00000000219920", "0x00000000219930", "0x00000000219940", "0x00000000219950", 
            "0x00000000219960", "0x00000000219970", "0x00000000219980", "0x00000000219990", 
            "0x000000002199a00", "0x000000002199b00", "0x000000002199c00", "0x000000002199d00", 
            "0x000000002199e00", "0x000000002199f00", "0x0000000021a00", "0x0000000021a10", 
            "0x0000000021a20", "0x0000000021a30", "0x0000000021a40", "0x0000000021a50", 
            "0x0000000021a60", "0x0000000021a70", "0x0000000021a80", "0x0000000021a90", 
            "0x0000000021aa00", "0x0000000021ab00", "0x0000000021ac00", "0x0000000021ad00", 
            "0x0000000021ae00", "0x0000000021af00", "0x0000000021b00", "0x0000000021b10", 
            "0x0000000021b20", "0x0000000021b30", "0x0000000021b40", "0x0000000021b50", 
            "0x0000000021b60", "0x0000000021b70", "0x0000000021b80", "0x0000000021b90", 
            "0x0000000021ba00", "0x0000000021bb00", "0x0000000021bc00", "0x0000000021bd00", 
            "0x0000000021be00", "0x0000000021bf00", "0x0000000021c00", "0x0000000021c10", 
            "0x0000000021c20", "0x0000000021c30", "0x0000000021c40", "0x0000000021c"
        ];

        // Render the syscall array to the page
        const syscallContainer = document.getElementById('syscallArray');
        syscallArray.forEach(address => {
            const addressElement = document.createElement('div');
            addressElement.className = 'address';
            addressElement.textContent = address;
            syscallContainer.appendChild(addressElement);
        });

        // Add a count display
        const countElement = document.createElement('div');
        countElement.style.cssText = 'margin-top: 20px; padding: 10px; background: rgba(0,0,0,0.2); border-radius: 5px;';
        countElement.textContent = `Total syscalls in array: ${syscallArray.length}`;
        syscallContainer.parentNode.insertBefore(countElement, syscallContainer.nextSibling);
    </script>
</body>
</html>
```
