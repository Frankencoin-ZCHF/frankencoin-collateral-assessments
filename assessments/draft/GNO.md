---
{
  "asset_name": "Gnosis",
  "asset_ticker": "GNO",
  "contract_address": "0x6810e776880c02933d47db1b9fc05908e5386b96",
  "assessment_date": "2026-08-01",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x6810e776880c02933d47db1b9fc05908e5386b96",
    "coingecko": "https://www.coingecko.com/en/coins/gnosis",
    "website": "https://www.gnosis.io/",
    "docs": "https://docs.gnosischain.com/",
    "other": "https://forum.gnosis.io/"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "17.94%",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "GnosisDAO ecosystem",
          "probability": "Medium",
          "severity": "Severe",
          "compensation": "2.50%"
        }
      ],
      "smart_contract_risks": [
        {
          "name": "Smart-Contract Exploit",
          "probability": "Very Low",
          "severity": "Severe",
          "compensation": "0.25%"
        }
      ],
      "governance_risks": [
        {
          "name": "n/a",
          "probability": "n/a",
          "severity": "n/a",
          "compensation": "0%"
        }
      ],
      "legal_risks": [
        {
          "name": "n/a",
          "probability": "n/a",
          "severity": "n/a",
          "compensation": "0%"
        }
      ],
      "liquidity_risks": [
        {
          "name": "n/a",
          "probability": "Negligible",
          "severity": "n/a",
          "compensation": "0%"
        }
      ],
      "contagion_risks": [
        {
          "name": "Crypto ecosystem contagion",
          "probability": "Medium",
          "severity": "Moderate",
          "compensation": "1.25%"
        }
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.40,
    "target_interest_rate": 0.04,
    "global_minting_limit": 5000000,
    "liquidation_price": 30,
    "maturity": null,
    "auction_duration": 24,
    "minimum_collateral": 350
  }
}
---

# Collateral Risk Assessment: Gnosis

## Summary

GNO is the native token of the Gnosis ecosystem. It is used in relation to GnosisDAO, Gnosis Chain, and the broader Gnosis infrastructure stack.

GNO is a credible collateral candidate because it has strong public information, meaningful market liquidity, and a long operating history. The main residual risks are Gnosis ecosystem dependency, smart-contract risk, and broader DeFi-market contagion.

## Introduction

Gnosis is a long-standing Ethereum ecosystem project with a broad infrastructure footprint, including GnosisDAO, Gnosis Chain, and other products and initiatives.

The value of the GNO token thus depends primarily on the relevance, activity, governance, treasury strength, and perceived long-term viability of the Gnosis ecosystem.

If the Gnosis ecosystem were to lose relevance, mismanage its DAO treasury, or fail to sustain demand for GNO, the token could suffer a severe correction.

## Free Float/Liquidity

Classification: Strong

GNO has a meaningful circulating supply, a long trading history, and secondary-market liquidity across centralized and decentralized venues. It is a well-known Ethereum ecosystem asset and has sufficient liquidity.

## Public Information

Classification: Strong

Public information is strong since there is a liquid secondary market and auction outcomes could easily be assessed.

## Market Risk

99%-VaR, 48h close-to-close: 13.72%

Maximum Drawdown, 48h close-to-close: 17.94%

The 99% 48h close-to-close VaR in the dataset is 13.72%, while the maximum 48h close-to-close drawdown is 17.94%. The minimum reserve requirement should therefore be 20%.

## Tail Risks

### Counterparty Risk: GnosisDAO ecosystem

Description: GNO depends on the continued relevance, activity, and perceived long-term viability of the Gnosis ecosystem.

Probability: Medium

Severity: Severe

Compensation: 2.50%

GNO does not carry counterparty risk in the strict legal sense, because it is not a redeemable claim on an issuer, custodian, borrower, or off-chain asset. However, it does have material ecosystem and business-execution dependency.

However, if GnosisDAO, Gnosis Chain, or related ecosystem activity were to lose relevance, materially reduce operations, or wind down, GNO could suffer a severe repricing. The token has no hard redemption floor, so the downside in such a scenario could be materially larger than ordinary market volatility. A 2.50% compensation is assigned for this residual ecosystem-dependency risk.

Global Minting Limit: 5,000,000 ZCHF

Since this risk is classified as Medium probability, it triggers a global minting limit requirement under the framework. GNO is not a legal counterparty claim, but it is exposed to the continued relevance of the Gnosis ecosystem. If GnosisDAO, Gnosis Chain, or related activity were to wind down, GNO could suffer a severe correction without a hard redemption floor.

A 5,000,000 ZCHF global minting limit keeps this exposure absorbable by the system equity, given the withdrawable amount would be 3,000,000 ZCHF at a 40% reserve requirement.

### Smart Contract Risk: Smart-Contract Exploit

Description: GNO depends on the Ethereum token contract and related market infrastructure.

Probability: Very Low

Severity: Severe

Compensation: 0.25%

GNO is a long-standing ERC-20 token. Smart-contract risk is therefore low, but not zero. A 0.25% compensation is assigned.

### Governance Risk: n/a

Description: No separate governance-risk premium is assigned in the current classification, to avoid double-counting.

Probability: n/a

Severity: n/a

Compensation: 0%

GNO is a governance-linked ecosystem token, but the dominant governance and execution risk is already captured under ecosystem and business-execution dependency. Assigning an additional standalone governance-risk premium would double-count the same underlying risk driver.

### Legal Risk: n/a

Description: No separate legal-risk premium is assigned in the current classification.

Probability: n/a

Severity: n/a

Compensation: 0%

GNO is not a tokenized security, custodial wrapper, or redeemable off-chain claim.

### Liquidity Risk: n/a

Description: No separate liquidity-risk premium is assigned in the current classification.

Probability: Negligible

Severity: n/a

Compensation: 0%

GNO has meaningful secondary-market liquidity and public price discovery. Liquidation risk is still relevant during market stress, but this is addressed through the retained reserve and the global minting limit. No additional liquidity-risk premium is assigned.

### Contagion Risk: Crypto ecosystem contagion

Description: GNO may be affected by broader crypto/DeFi stress in the Ethereum ecosystem.

Probability: Medium

Severity: Moderate

Compensation: 1.25%

GNO is exposed to broader DeFi and Ethereum-market sentiment. A major DeFi stress event could have a major effect on GNO beyond the 20% reserve requirement.

A higher reserve requirement of 40% can buffer most of this tail risk, to ensure the impact would only be moderate (instead of severe). In that case, an additional 1.25% compensation is sufficient to account for this tail risk. If a future proposal requests a reserve requirement of just 20%, the compensation should be increased to 2.5%.

## Conclusion

GNO is a credible but higher-risk collateral candidate for Frankencoin.

The asset has strong public information, strong free float, and sufficient market liquidity, but its value is highly dependent on the continued relevance of the Gnosis ecosystem. The main risk is not legal counterparty exposure, but ecosystem and business-execution dependency: if GnosisDAO or related activity were to wind down or lose market relevance, GNO could experience a severe correction without a hard redemption floor.

A 40% retained reserve provides a substantial buffer above the observed 48h market-risk measures. The 4.00% target interest rate compensates for residual ecosystem, smart-contract, and contagion risks, while the 5,000,000 ZCHF global minting limit keeps initial protocol exposure contained.

