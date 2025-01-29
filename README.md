# zegribot
Auto Trading bot
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trading Bot Dashboard</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .dashboard {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 400px;
        }
        h1 {
            text-align: center;
            color: #333;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            color: #555;
        }
        input[type="text"], input[type="number"], select {
            width: 100%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #28a745;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #218838;
        }
        .status {
            margin-top: 20px;
            text-align: center;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <div class="dashboard">
        <h1>Trading Bot Dashboard</h1>

        <div class="form-group">
            <label for="symbol">Trading Pair:</label>
            <input type="text" id="symbol" placeholder="e.g., BTC/USD">
        </div>

        <div class="form-group">
            <label for="strategy">Trading Strategy:</label>
            <select id="strategy">
                <option value="mean-reversion">Mean Reversion</option>
                <option value="momentum">Momentum</option>
                <option value="arbitrage">Arbitrage</option>
            </select>
        </div>

        <div class="form-group">
            <label for="amount">Amount to Trade:</label>
            <input type="number" id="amount" placeholder="e.g., 0.01">
        </div>

        <button id="startBot">Start Trading Bot</button>

        <div class="status" id="status">
            Bot Status: Idle
        </div>
    </div>

    <script>
        document.getElementById('startBot').addEventListener('click', function() {
            const symbol = document.getElementById('symbol').value;
            const strategy = document.getElementById('strategy').value;
            const amount = document.getElementById('amount').value;

            if (symbol && strategy && amount) {
                document.getElementById('status').innerText = 'Bot Status: Running...';
                // Here you would typically send a request to your backend to start the bot
                console.log(`Starting bot with Symbol: ${symbol}, Strategy: ${strategy}, Amount: ${amount}`);
            } else {
                alert('Please fill in all fields.');
            }
        });
    </script>

</body>
</html>
