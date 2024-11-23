# Trust Dynamics and Market Behavior in Cryptocurrency: A Comparative Study of Centralized and Decentralized Exchanges

## *Supplementary resources, data, and code*
by **Xintong Wu***, **Wanlin Deng***, **Yutong Quan** ,and **Luyao Zhang†**
(* * the co-first authors,
   † the corresponding author: lz183@duke.edu*)
   
## Abstract
In the rapidly evolving cryptocurrency landscape, user trust dynamics shape market behaviors and preferences for centralized exchanges (CEXs) and decentralized exchanges (DEXs). The collapse of FTX, a major CEX, marked a critical moment, raising questions about the resilience of centralized trust systems and accelerating shifts toward decentralized alternatives. This research investigates the immediate and nuanced impacts of the FTX collapse on user trust, focusing on token valuation, trading flows, and sentiment dynamics. Employing robust analytical methods, including Regression Discontinuity Design (RDD) and Difference-in-Differences (DID), we reveal significant declines in WETH prices and NetFlow from CEX to DEX, signaling a measurable transfer of trust. Additionally, topic modeling and sentiment analysis expose the complexities of user responses, highlighting shifts from functional discussions to emotional fragmentation in Binance’s community, while Uniswap’s sentiment exhibits a gradual upward trend. Despite data limitations and external influences, the findings underscore the intricate interplay between trust, sentiment, and market behavior in the cryptocurrency ecosystem. This study contributes to interdisciplinary research by bridging blockchain analytics, behavioral finance, and decentralized finance (DeFi). It provides a deeper understanding of distributed trust mechanisms, offering critical insights for future investigations into the socio-technical dimensions of trust in digital economies.

## Data Dictionary

This document describes the datasets used in the project.

### Dataset 1: WETH Daily Prices

| **Variable Name** | **Description**                 | **Frequency** | **Unit** | **Type**   |
|--------------------|---------------------------------|---------------|----------|------------|
| Date               | The date of the price record   | Daily         | Date     | Timestamp  |
| Price              | Average daily price of WETH    | Daily         | USD      | Numerical  |

---

### Dataset 2: WETH NetFlow Data

| **Variable Name**      | **Description**                                         | **Frequency** | **Unit** | **Type**   |
|-------------------------|---------------------------------------------------------|---------------|----------|------------|
| Date                   | The date of the transaction record                      | Daily         | Date     | Timestamp  |
| USER --> DEX           | Number of users transferring funds to DEX              | Daily         | Count    | Numerical  |
| USER --> CEX           | Number of users transferring funds to CEX              | Daily         | Count    | Numerical  |
| Net User               | Net user flow (DEX inflow - CEX inflow)                 | Daily         | Count    | Numerical  |
| Amount --> DEX         | Total amount of WETH transferred to DEX                 | Daily         | ETH      | Numerical  |
| Amount --> CEX         | Total amount of WETH transferred to CEX                 | Daily         | ETH      | Numerical  |
| Net Amount ETH         | Net amount of WETH transferred (DEX - CEX)              | Daily         | ETH      | Numerical  |
| Amount $ --> DEX       | Total value in USD transferred to DEX                   | Daily         | USD      | Numerical  |
| Amount $ --> CEX       | Total value in USD transferred to CEX                   | Daily         | USD      | Numerical  |
| Net Amount $           | Net value in USD transferred (DEX - CEX)                | Daily         | USD      | Numerical  |

---

### Dataset 3: Binance Discord User Messages

| **Variable Name** | **Description**                                | **Frequency** | **Unit**      | **Type**       |
|--------------------|------------------------------------------------|---------------|---------------|----------------|
| AuthorID          | Anonymized unique identifier for each user     | Per Message   | Unique ID     | Alphanumeric   |
| Author            | Username of the message author                 | Per Message   | Text          | Categorical    |
| Date              | Timestamp of the message                       | Per Message   | Timestamp     | Timestamp      |
| Content           | Message content                                | Per Message   | Text          | Text           |
| Attachments       | Attachments (if any) included in the message   | Per Message   | File Reference| Categorical    |
| Reactions         | Reactions (e.g., emojis) on the message        | Per Message   | Count         | Numerical      |

---

### Dataset 4: Uniswap Discord User Messages

| **Variable Name** | **Description**                                | **Frequency** | **Unit**      | **Type**       |
|--------------------|------------------------------------------------|---------------|---------------|----------------|
| AuthorID          | Anonymized unique identifier for each user     | Per Message   | Unique ID     | Alphanumeric   |
| Author            | Username of the message author                 | Per Message   | Text          | Categorical    |
| Date              | Timestamp of the message                       | Per Message   | Timestamp     | Timestamp      |
| Content           | Message content                                | Per Message   | Text          | Text           |
| Attachments       | Attachments (if any) included in the message   | Per Message   | File Reference| Categorical    |
| Reactions         | Reactions (e.g., emojis) on the message        | Per Message   | Count         | Numerical      |

---

### Dataset 5: Gold Prices

| **Variable Name** | **Description**               | **Frequency** | **Unit** | **Type**   |
|--------------------|-------------------------------|---------------|----------|------------|
| Date               | The date of the gold price   | Daily         | Date     | Timestamp  |
| USD                | Price of gold per troy ounce | Daily         | USD      | Numerical  |

---

### Dataset 6: Aggregated Metrics

| **Variable Name**  | **Description**                                          | **Frequency** | **Unit**  | **Type**      |
|---------------------|----------------------------------------------------------|---------------|-----------|---------------|
| Date               | The date of the record                                   | Daily         | Date      | Timestamp     |
| Gold_price         | Daily gold price                                         | Daily         | USD       | Numerical     |
| Price              | Average daily price of WETH                              | Daily         | USD       | Numerical     |
| Netflow            | Net fund flow (DEX inflow - CEX inflow)                  | Daily         | USD       | Numerical     |
| Sentiment_b        | Sentiment score for Binance community                    | Daily         | [-1, 1]   | Numerical     |
| Label_b            | Sentiment label for Binance community                    | Daily         | Categorical (Positive/Neutral/Negative) |
| Sentiment_u        | Sentiment score for Uniswap community                    | Daily         | [-1, 1]   | Numerical     |
| Label_u            | Sentiment label for Uniswap community                    | Daily         | Categorical (Positive/Neutral/Negative) |

---

#### Notes:
- All timestamps are in UTC.
- Sentiment scores are derived using a fine-tuned RoBERTa model from Hugging Face.
- NetFlow calculations are based on inflows and outflows between DEX and CEX platforms.

## Code
| **File Name**  | **Description**                                         |
|---------------------|----------------------------------|
| Causal_Inference    | Open code for causal inference analysis     |
| Topic_Analysis      | Open code for causal topic analysis         |


