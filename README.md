# Trust Dynamics and Market Behavior in Cryptocurrency: A Comparative Study of Centralized and Decentralized Exchanges

## 📘 Supplementary Resources, Data, and Code

by **Xintong Wu**†, **Wanlin Deng**†, **Yutong Quan**, and **Luyao Zhang***  
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

📧 For inquiries, contact us at: [lz183@duke.edu](mailto:lz183@duke.edu)
