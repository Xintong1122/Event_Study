## Data Dictionary



### Transaction volume of CEX and DEX

| Variable Name    | Description           | Frequency | Unit | Type   | Indirect Data Source | Original Data Source | Cross-Validation Data Source |
| ---------------- | --------------------- | --------- | ---- | ------ | --------------------- | -------------------- | ---------------------------- |
| DATE             | Date of transaction   | Daily     | Date | Date   | N/A                   | N/A                  | N/A                          |
| INFLOW\_USD      | Inflow in USD         | Daily     | USD  | Numeric| N/A                   | N/A                  | N/A                          |
| OUTFLOW\_USD     | Outflow in USD        | Daily     | USD  | Numeric| N/A                   | N/A                  | N/A                          |
| TOTAL\_USD\_VOLUME | Total USD Volume    | Daily     | USD  | Numeric| N/A                   | N/A                  | N/A                          |


### Transaction between CEX and DEX

| Variable Name          | Description           | Frequency | Unit | Type | Indirect Data Source | Original Data Source | Cross-Validation Data Source |
|------------------------|-----------------------|-----------|------|------|-----------------------|----------------------|-----------------------------|
| DATE                   | Date of transfer      | Daily     | Date | Date | N/A                   | N/A                  | N/A                         |
| N\_TRANSFER            | Number of transfers   | Daily     | Count| Integer | N/A               | N/A                  | N/A                         |
| USER                   | User identifier      | Daily     | Count | Integer | N/A               | N/A                  | N/A                         |
| AMOUNT\_USD            | Amount in USD         | Daily     | USD  | Numeric | N/A               | N/A                  | N/A                         |
| AMOUNT\_ETH            | Amount in ETH         | Daily     | ETH  | Numeric | N/A               | N/A                  | N/A                         |
| CEX                    | Centralized Exchange  | Daily     | Text | Categorical | N/A        | N/A                  | N/A                         |
| DEX                    | Decentralized Exchange| Daily     | Text | Categorical | N/A        | N/A                  | N/A                         |

### Netflow between CEX and DEX

| Variable Name         | Description            | Frequency | Unit     | Type    | Indirect Data Source | Original Data Source | Cross-Validation Data Source |
| --------------------- | ---------------------- | --------- | -------- | ------- | -------------------- | --------------------- | ---------------------------- |
| DATE                  | Transaction Date       | Daily     | Date     | Date    | N/A                  | N/A                 | N/A                          |
| USER $\rightarrow$ DEX | User Interaction with DEX | Daily  | Count    | Integer | N/A                  | N/A                 | N/A                          |
| USER $\rightarrow$ CEX | User Interaction with CEX | Daily  | Count    | Integer | N/A                  | N/A                 | N/A                          |
| Net User              | Net User Interaction    | Daily     | Count    | Integer | N/A                  | N/A                 | N/A                          |
| Amount $\rightarrow$ DEX | Amount Related to DEX | Daily | USD      | Numeric | N/A                  | N/A                 | N/A                          |
| Amount $\rightarrow$ CEX | Amount Related to CEX | Daily | USD      | Numeric | N/A                  | N/A                 | N/A                          |
| Net Amount ETH        | Net ETH Amount          | Daily     | ETH      | Numeric | N/A                  | N/A                 | N/A                          |
| Amount \$ $\rightarrow$ DEX | Amount in USD Related to DEX | Daily | USD | Numeric | N/A             | N/A                 | N/A                          |
| Amount \$ $\rightarrow$ CEX | Amount in USD Related to CEX | Daily | USD | Numeric | N/A             | N/A                 | N/A                          |
| Net Amount \$         | Net USD Amount          | Daily     | USD      | Numeric | N/A                  | N/A                 | N/A                          |

