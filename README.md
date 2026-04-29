# Trust Dynamics in Cryptocurrency Markets: Centralized vs. Decentralized Exchanges

![Python](https://img.shields.io/badge/python-3.9+-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/status-research-success)

Supplementary resources, data, and code for the research paper investigating Ethereum price movements through community sentiment, capital flows, and macroeconomic indicators.


## Repository Structure

```text
ETH_Multimodal_Analysis/
├── Code/
│   ├── Causal_Inference.ipynb    # RDD and causal impact analysis
│   └── Topic_Analysis.ipynb      # Sentiment extraction and LDA topic modeling
├── Data/
│   ├── 1_Price.csv               # Historical ETH price data
│   ├── 2_NetFlow.csv             # Net flows between USER, CEX, and DEX
│   ├── 3_Binance_Processed.csv   # Processed Binance community sentiment
│   ├── 3_Uniswap_Processed.csv   # Processed Uniswap community sentiment
│   ├── Gold_price_per_troy_ounce.csv # Macro control variable
│   ├── total_data.csv            # Final merged dataset for modeling
│   └── Binance - ⊱▬▬ Community ▬▬⊰ - 🌎┃global-chat [882554401154289667].csv/
│       ├── Binance_raw1.csv      # Split raw data (requires manual merge)
│       ├── Binance_raw2.csv
│       └── Binance_raw3.csv
├── spotlight/                    # Visualization assets
│   ├── co.png                    # Coherence score VS number of topics
│   └── lda1.png                  # Topic analysis (before)
│   └── lda2.png                  # Topic analysis (after)
│   └── net1.png                  # Nodes and connections (before)
│   └── net2.png                  # Nodes and connections (after)
│   └── netflow_rdd.png           # NetFlow regression discontinuity
│   └── price_did.png             # Price difference in differences
│   └── price_rdd.png             # Price regression discontinuity
│   └── senti_b_rdd.png           # Binance sentiment score regression discontinuity
│   └── senti_u_rdd.png           # Uniswap sentiment score regression discontinuity
│   └── word_freq1.png            # Binance word frequency distribution (before)
│   └── word_freq2.png            # Binance word frequency distribution (after)

└── README.md
```

## Quick Start

```bash
# Clone repository
git clone https://github.com/Xintong1122/Event_Study.git
cd Event_Study

# Note: Large raw Discord data files are split. 
# Please merge Binance_raw1.csv, raw2.csv, and raw3.csv before processing.
```


## 📚 Data Dictionary


### Financial & Flow Data

#### 1_Price.csv (ETH Price)
| Variable | Description |
|----------|-------------|
| Date     | Trading date (YYYY/MM/DD) |
| Price    | ETH daily closing price |

 📈 Dataset 1: WETH Daily Prices

| **Variable Name** | **Description**               | **Frequency** | **Unit** | **Type**     |
|--------------------|-------------------------------|---------------|----------|--------------|
| Date              | The date of the price record | Daily         | Date     | Timestamp    |
| Price             | Average daily price of WETH  | Daily         | USD      | Numerical    |




#### 2_NetFlow.csv (Inter-platform flows)
| Variable | Description |
|----------|-------------|
| Net User | Net change in users (USER -> DEX vs USER -> CEX) |
| Net Amount | Net ETH flow between DEX and CEX |
| Net Amount $ | Net USD value flow |

💸 Dataset 2: WETH NetFlow Data

| **Variable Name**  | **Description**                                        | **Frequency** | **Unit** | **Type**     |
|---------------------|--------------------------------------------------------|---------------|----------|--------------|
| Date               | The date of the transaction record                     | Daily         | Date     | Timestamp    |
| USER --> DEX       | Number of users transferring funds to DEX              | Daily         | Count    | Numerical    |
| USER --> CEX       | Number of users transferring funds to CEX              | Daily         | Count    | Numerical    |
| Net User           | Net user flow (DEX inflow - CEX inflow)                | Daily         | Count    | Numerical    |
| Amount --> DEX     | Total amount of WETH transferred to DEX                | Daily         | ETH      | Numerical    |
| Amount --> CEX     | Total amount of WETH transferred to CEX                | Daily         | ETH      | Numerical    |
| Net Amount ETH     | Net amount of WETH transferred (DEX - CEX)             | Daily         | ETH      | Numerical    |


#### Gold_price_per_troy_ounce.csv
| Variable | Description |
|----------|-------------|
| Date     | Trading date |
| USD      | Gold price per troy ounce |

### Social Sentiment Data

#### Discord Messages (Raw)
*Note: Binance data is split into `raw1`, `raw2`, and `raw3` for storage. Users must merge them before analysis.*

| Variable | Description |
|----------|-------------|
| AuthorID | Unique identifier for message authors |
| Author   | Discord username |
| Date     | Timestamp in ISO 8601 format |
| Content  | Raw message text |

#### total_data.csv (Merged for Modeling)
| Variable | Description |
|----------|-------------|
| Price    | ETH Price |
| Netflow  | Consolidated capital flows |
| Sentiment_b | Binance sentiment score |
| Sentiment_u | Uniswap sentiment score |

## Code

- **Topic_Analysis.ipynb**: Includes data cleaning, sentiment labeling using LLM, and LDA topic discovery.
- **Causal_Inference.ipynb**: Includes Regression Discontinuity Designs (RDD) and quantitative analysis of price impacts.

## Spotlight Visualizations

- **Topic Distribution:** Visual representation of key community discussion themes.
- **Price Impact:** RDD plots showing price behavior relative to specific sentiment cutoffs.

## License

This project is licensed under the MIT License. Data sourced from Discord is subject to platform's Terms of Service. This research is for academic purposes and does not constitute financial advice.


