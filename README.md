# Trust Dynamics and Market Behavior in Cryptocurrency: A Comparative Study of Centralized and Decentralized Exchanges

## 📘 Supplementary Resources, Data, and Code

by **Xintong Wu**†, **Wanlin Deng**†, **Yutong Quan**, **Lin William Cong**, and **Luyao Zhang***  
(*† Joint first authors, * Corresponding author: [lz183@duke.edu](mailto:lz183@duke.edu)*)

---

## 📄 Abstract

In the rapidly evolving cryptocurrency landscape, user trust dynamics shape market behaviors and preferences for centralized exchanges (CEXs) and decentralized exchanges (DEXs). The collapse of FTX, a major CEX, marked a critical moment, raising questions about the resilience of centralized trust systems and accelerating shifts toward decentralized alternatives.

This research investigates the immediate and nuanced impacts of the FTX collapse on user trust, focusing on token valuation, trading flows, and sentiment dynamics. Employing robust analytical methods, including Regression Discontinuity Design (RDD) and Difference-in-Differences (DID), we reveal significant declines in WETH prices and NetFlow from CEX to DEX, signaling a measurable transfer of trust.

Additionally, topic modeling and sentiment analysis expose the complexities of user responses, highlighting shifts from functional discussions to emotional fragmentation in Binance’s community, while Uniswap’s sentiment exhibits a gradual upward trend. Despite data limitations and external influences, the findings underscore the intricate interplay between trust, sentiment, and market behavior in the cryptocurrency ecosystem.

---

## 📚 Data Dictionary

### 📈 Dataset 1: WETH Daily Prices

| **Variable Name** | **Description**               | **Frequency** | **Unit** | **Type**     |
|--------------------|-------------------------------|---------------|----------|--------------|
| Date              | The date of the price record | Daily         | Date     | Timestamp    |
| Price             | Average daily price of WETH  | Daily         | USD      | Numerical    |

---

### 💸 Dataset 2: WETH NetFlow Data

| **Variable Name**  | **Description**                                        | **Frequency** | **Unit** | **Type**     |
|---------------------|--------------------------------------------------------|---------------|----------|--------------|
| Date               | The date of the transaction record                     | Daily         | Date     | Timestamp    |
| USER --> DEX       | Number of users transferring funds to DEX              | Daily         | Count    | Numerical    |
| USER --> CEX       | Number of users transferring funds to CEX              | Daily         | Count    | Numerical    |
| Net User           | Net user flow (DEX inflow - CEX inflow)                | Daily         | Count    | Numerical    |
| Amount --> DEX     | Total amount of WETH transferred to DEX                | Daily         | ETH      | Numerical    |
| Amount --> CEX     | Total amount of WETH transferred to CEX                | Daily         | ETH      | Numerical    |
| Net Amount ETH     | Net amount of WETH transferred (DEX - CEX)             | Daily         | ETH      | Numerical    |

---

## 💻 Code

| **File Name**      | **Description**                       |
|--------------------|---------------------------------------|
| Causal_Inference   | Open code for causal inference analysis |
| Topic_Analysis     | Open code for causal topic analysis     |

---

# Trust Dynamics in Cryptocurrency Markets: Centralized vs. Decentralized Exchanges

![Python](https://img.shields.io/badge/python-3.9+-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/status-research-success)

Supplementary resources, data, and code for the research paper investigating Ethereum price movements through community sentiment, capital flows, and macroeconomic indicators.

## Table of Contents

- [Quick Start](#quick-start)
- [Abstract](#abstract)
- [Methodology](#methodology)
- [Repository Structure](#repository-structure)
- [Data](#data)
  - [Financial & Flow Data](#financial--flow-data)
  - [Social Sentiment Data](#social-sentiment-data)
- [Code](#code)
- [Spotlight Visualizations](#spotlight-visualizations)
- [License](#license)

## Quick Start

```bash
# Clone repository
git clone https://github.com/Xintong1122/Event_Study.git
cd Event_Study

# Note: Large raw Discord data files are split. 
# Please merge Binance_raw1.csv, raw2.csv, and raw3.csv before processing.
```

## Abstract

add abstract

**Research Questions:**
- RQ1
- RQ2

## Methodology

### Sentiment Analysis Pipeline
We utilize Large Language Models (LLMs) to perform sentiment extraction from community discussions.
- **Model:** Fine-tuned Transformer-based architecture for crypto-specific sentiment.
- **Classes:** Positive, Neutral, Negative.
- **Features:** Categorical labels and continuous sentiment scores.

### Analytical Framework
- **Topic Modeling:** Utilizing LDA to identify key discussion themes.
- **Causal Inference:** Implementing Regression Discontinuity Designs (RDD) to validate the impact of community events on token returns.
- **Feature Integration:** Combining On-chain flows, Off-chain sentiment, and Macro benchmarks (Gold prices).

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

## Data

### Financial & Flow Data

#### 1_Price.csv (ETH Price)
| Variable | Description |
|----------|-------------|
| Date     | Trading date (YYYY/MM/DD) |
| Price    | ETH daily closing price |

#### 2_NetFlow.csv (Inter-platform flows)
| Variable | Description |
|----------|-------------|
| Net User | Net change in users (USER -> DEX vs USER -> CEX) |
| Net Amount | Net ETH flow between DEX and CEX |
| Net Amount $ | Net USD value flow |

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

This project is licensed under the MIT License. Data sourced from Discord is subject to platform Terms of Service. This research is for academic purposes and does not constitute financial advice.

---

📧 For inquiries, contact us at: [lz183@duke.edu](mailto:lz183@duke.edu)
