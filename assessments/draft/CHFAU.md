---
{
  "asset_name": "AllUnity CHF",
  "asset_ticker": "CHFAU",
  "contract_address": "0xbd4dfc058eb95b8de5ceaf39966a1a70f5556f78",
  "assessment_date": "2026-09-11",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0xbd4dfc058eb95b8de5ceaf39966a1a70f5556f78",
    "coingecko": "https://www.coingecko.com/en/coins/allunity-chf",
    "website": "https://allunity.com/chfau/",
    "docs": "https://allunity.com/chfau/",
    "other": "https://www.allunity.com/"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Sufficient",
    "market_risk": "0%",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "AllUnity",
          "probability": "Negligible",
          "severity": "n/a",
          "compensation": "0%"
        }
      ],
      "smart_contract_risks": [
        {
          "name": "Smart-Contract Risk",
          "probability": "Negligible",
          "severity": "n/a",
          "compensation": "0%"
        }
      ],
      "governance_risks": [
        {
          "name": "Governance Risk",
          "probability": "Negligible",
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
          "name": "n/a",
          "probability": "Negligible",
          "severity": "n/a",
          "compensation": "0%"
        }
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.00,
    "target_interest_rate": 0.00,
    "global_minting_limit": 10000000,
    "liquidation_price": 1,
    "maturity": null,
    "auction_duration": 24,
    "minimum_collateral": null
  }
}
---

# Collateral Risk Assessment: AllUnity CHF

## Summary

CHFAU is a centrally issued Swiss franc stablecoin by AllUnity. It is designed to maintain a one-to-one peg to CHF, and is fully backed by CHF reserves.

CHFAU is a credible collateral candidate because minting/redemption access is available through reputable participants such as Bitcoin Suisse and Mt Pelerin. The risk premium is 0% so it can be used as a 1:1 bridge module.

## Introduction

AllUnity CHF (CHFAU) is a CHF-denominated MiCAR-compliant ERC-20 stablecoin. It is backed by CHF cash reserves on the bank accounts of AllUnity, a German company registered in Frankfurt.

Pursuant to Article 49 MiCAR, the holders of EMTs have a statutory right of redemption against AllUnity at any time and at par value. 

## Free Float/Liquidity

Classification: Sufficient

CHFAU has sufficient free float. Supply can be minted and redeemed through participants such as Bitcoin Suisse and Mt Pelerin, supporting the bridge function between CHFAU and broader CHF liquidity.

## Public Information

Classification: Strong

Public information is strong as it is pegged 1:1 to CHF.

## Market Risk

99%-VaR, 48h close-to-close: 0%

Maximum Drawdown, 48h close-to-close: 0%

CHFAU is pegged to CHF. Since ZCHF is also CHF-denominated, no separate market-risk reserve is required for ordinary price volatility.

## Tail Risks

### Counterparty Risk: AllUnity

Description: CHFAU depends on AllUnity as the central issuer and on the operational process supporting issuance and redemption.

Probability: Negligible

Severity: n/a

Compensation: 0%

AllUnity is the relevant issuer counterparty. The counterparty dependency is acknowledged, but no compensation is assigned.

### Smart Contract Risk: Smart-Contract Risk

Description: CHFAU is an ERC-20 token and therefore carries residual smart-contract risk.

Probability: Negligible

Severity: n/a

Compensation: 0%

The residual smart-contract risk is considered negligible for this use case. No compensation is assigned.

### Governance Risk: Governance Risk

Description: CHFAU is centrally issued and therefore carries residual issuer-governance and administrative-control risk.

Probability: Negligible

Severity: n/a

Compensation: 0%

This risk is considered negligible in the context of CHFAU's role as bridge collateral. No compensation is assigned.

### Legal Risk: n/a

Description: No separate legal-risk premium is assigned in the current classification.

Probability: n/a

Severity: n/a

Compensation: 0%

Legal and regulatory considerations are mainly captured through the AllUnity counterparty assessment. No additional standalone legal-risk premium is assigned.

### Liquidity Risk: n/a

Description: No separate liquidity-risk premium is assigned in the current classification.

Probability: Negligible

Severity: n/a

Compensation: 0%

CHFAU can be minted and redeemed through participants such as Bitcoin Suisse and Mt Pelerin. No additional liquidity-risk premium is assigned for the proposed limited allocation.

### Contagion Risk: n/a

Description: No separate contagion-risk premium is assigned.

Probability: Negligible

Severity: n/a

Compensation: 0%

CHFAU is a CHF stablecoin and is not expected to carry material crypto-market contagion risk. No separate compensation is needed.

## Conclusion

CHFAU is a credible collateral candidate for Frankencoin as bridge collateral.

There is no material market risk relative to ZCHF, and the tail-risk premia for counterparty risk, smart-contract risk, and governance risk are each set to 0%.

The proposed global minting limit of 10,000,000 ZCHF is the main safeguard. It allows CHFAU to support CHF bridge liquidity while reducing dependency on a single counterparty.
