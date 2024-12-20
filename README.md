<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trust Dynamics and Market Behavior in Cryptocurrency</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            color: #333;
        }
        h1, h2, h3 {
            color: #0056b3;
        }
        table {
            border-collapse: collapse;
            width: 100%;
            margin-bottom: 20px;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: left;
        }
        th {
            background-color: #f4f4f4;
        }
        .highlight {
            background-color: #e8f4fa;
            padding: 10px;
            border-left: 4px solid #0056b3;
        }
        .emoji {
            font-size: 1.2em;
        }
        .icon {
            display: inline-block;
            margin-right: 8px;
        }
    </style>
</head>
<body>
    <h1>
        <span class="emoji">📊</span> Trust Dynamics and Market Behavior in Cryptocurrency: A Comparative Study of Centralized and Decentralized Exchanges
    </h1>

    <h2><span class="emoji">📘</span> Supplementary Resources, Data, and Code</h2>
    <p>
        by <strong>Xintong Wu</strong>†, <strong>Wanlin Deng</strong>†, <strong>Yutong Quan</strong>, and <strong>Luyao Zhang</strong>* <br>
        <small>(† Joint first authors, * Corresponding author: <a href="mailto:lz183@duke.edu">lz183@duke.edu</a>)</small>
    </p>

    <h2><span class="emoji">📄</span> Abstract</h2>
    <div class="highlight">
        <p>
            In the rapidly evolving cryptocurrency landscape, user trust dynamics shape market behaviors and preferences for centralized exchanges (CEXs) and decentralized exchanges (DEXs). The collapse of FTX, a major CEX, marked a critical moment, raising questions about the resilience of centralized trust systems and accelerating shifts toward decentralized alternatives.
        </p>
        <p>
            This research investigates the immediate and nuanced impacts of the FTX collapse on user trust, focusing on token valuation, trading flows, and sentiment dynamics. Employing robust analytical methods, including Regression Discontinuity Design (RDD) and Difference-in-Differences (DID), we reveal significant declines in WETH prices and NetFlow from CEX to DEX, signaling a measurable transfer of trust.
        </p>
        <p>
            Additionally, topic modeling and sentiment analysis expose the complexities of user responses, highlighting shifts from functional discussions to emotional fragmentation in Binance’s community, while Uniswap’s sentiment exhibits a gradual upward trend. Despite data limitations and external influences, the findings underscore the intricate interplay between trust, sentiment, and market behavior in the cryptocurrency ecosystem.
        </p>
    </div>

    <h2><span class="emoji">📚</span> Data Dictionary</h2>
    <h3><span class="emoji">📈</span> Dataset 1: WETH Daily Prices</h3>
    <table>
        <thead>
            <tr>
                <th>Variable Name</th>
                <th>Description</th>
                <th>Frequency</th>
                <th>Unit</th>
                <th>Type</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Date</td>
                <td>The date of the price record</td>
                <td>Daily</td>
                <td>Date</td>
                <td>Timestamp</td>
            </tr>
            <tr>
                <td>Price</td>
                <td>Average daily price of WETH</td>
                <td>Daily</td>
                <td>USD</td>
                <td>Numerical</td>
            </tr>
        </tbody>
    </table>

    <h3><span class="emoji">💸</span> Dataset 2: WETH NetFlow Data</h3>
    <table>
        <thead>
            <tr>
                <th>Variable Name</th>
                <th>Description</th>
                <th>Frequency</th>
                <th>Unit</th>
                <th>Type</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Date</td>
                <td>The date of the transaction record</td>
                <td>Daily</td>
                <td>Date</td>
                <td>Timestamp</td>
            </tr>
            <tr>
                <td>USER --> DEX</td>
                <td>Number of users transferring funds to DEX</td>
                <td>Daily</td>
                <td>Count</td>
                <td>Numerical</td>
            </tr>
            <tr>
                <td>USER --> CEX</td>
                <td>Number of users transferring funds to CEX</td>
                <td>Daily</td>
                <td>Count</td>
                <td>Numerical</td>
            </tr>
            <tr>
                <td>Net User</td>
                <td>Net user flow (DEX inflow - CEX inflow)</td>
                <td>Daily</td>
                <td>Count</td>
                <td>Numerical</td>
            </tr>
            <tr>
                <td>Amount --> DEX</td>
                <td>Total amount of WETH transferred to DEX</td>
                <td>Daily</td>
                <td>ETH</td>
                <td>Numerical</td>
            </tr>
            <tr>
                <td>Amount --> CEX</td>
                <td>Total amount of WETH transferred to CEX</td>
                <td>Daily</td>
                <td>ETH</td>
                <td>Numerical</td>
            </tr>
            <tr>
                <td>Net Amount ETH</td>
                <td>Net amount of WETH transferred (DEX - CEX)</td>
                <td>Daily</td>
                <td>ETH</td>
                <td>Numerical</td>
            </tr>
        </tbody>
    </table>

    <h2><span class="emoji">💻</span> Code</h2>
    <table>
        <thead>
            <tr>
                <th>File Name</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Causal_Inference</td>
                <td>Open code for causal inference analysis</td>
            </tr>
            <tr>
                <td>Topic_Analysis</td>
                <td>Open code for causal topic analysis</td>
            </tr>
        </tbody>
    </table>

    <p><span class="emoji">📧</span> For inquiries, contact us at: <a href="mailto:lz183@duke.edu">lz183@duke.edu</a></p>
</body>
</html>
