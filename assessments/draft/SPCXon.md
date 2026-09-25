---
{
  "asset_name": "Space Exploration Technologies Corp. (Ondo Tokenized)",
  "asset_ticker": "SPCXon",
  "contract_address": "0xc9eef266834730340A55B6CC24621B31BAF55581",
  "assessment_date": "2026-09-25",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/address/0xc9eef266834730340a55b6cc24621b31baf55581",
    "coingecko": "https://www.coingecko.com/en/coins/spacex-ondo-tokenized-stock",
    "website": "https://app.ondo.finance/assets/spcxon",
    "docs": "https://docs.ondo.finance/ondo-stocks/overview",
    "other": "https://ondo.finance/ondo-stocks"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "19.40%",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "SpaceX",
          "probability": "Medium",
          "severity": "Severe",
          "compensation": "1.00%"
        },
        {
          "name": "Ondo Finance",
          "probability": "Very Low",
          "severity": "Severe",
          "compensation": "0.25%"
        }
      ],
      "smart_contract_risks": [
        {
          "name": "Smart-Contract Exploit",
          "probability": "Low",
          "severity": "Critical",
          "compensation": "0.50%"
        }
      ],
      "governance_risks": [
        {
          "name": "Transfer restrictions / Admin Control",
          "probability": "Low",
          "severity": "Severe",
          "compensation": "0.50%"
        }
      ],
      "legal_risks": [
        {
          "name": "n/a",
          "probability": "n/a",
          "severity": "n/a",
          "compensation": "n/a"
        }
      ],
      "liquidity_risks": [
        {
          "name": "Secondary-market or redemption impairment",
          "probability": "Negligible",
          "severity": "n/a",
          "compensation": "0%"
        }
      ],
      "contagion_risks": [
        {
          "name": "n/a",
          "probability": "n/a",
          "severity": "n/a",
          "compensation": "0%"
        }
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.30,
    "target_interest_rate": 0.0225,
    "global_minting_limit": 1000000,
    "liquidation_price": 100,
    "maturity": null,
    "auction_duration": 24,
    "minimum_collateral": 7.5
  }
}
---

# Collateral Risk Assessment: Space Exploration Technologies Corp. (Ondo Tokenized)

## Summary

SPCXon is a tokenized representation of Space Exploration Technologies Corp. issued through Ondo’s tokenized-stock infrastructure. It gives holders economic exposure to SpaceX in ERC-20 form.

The main risks are not only the exposure to a stock with limited price history itself, but the tokenized-security structure: issuer dependency, admin controls, and residual smart-contract risk.

## Introduction

SPCXon represents tokenized exposure to Space Exploration Technologies Corp. SpaceX is one of the largest and most widely followed technology companies globally, with exposure to launch services, satellite infrastructure, and broader space-related infrastructure.

The tokenized version introduces an additional RWA/security-token layer. The token is not only exposed to the ordinary price movement of the underlying equity exposure, but also to the mechanics of the Ondo tokenized asset wrapper.

## Free Float/Liquidity

Classification: Strong

SPCXon has strong public market visibility since listing and is supported by Ondo’s tokenized-stock infrastructure, and Ondo's own interface taps directly into traditional market liquidity. Besides Ondo's market place, the token is also listed on several venues like Binance, Gate, MEXC, BingX, and Uniswap.

## Public Information

Classification: Strong

SPCXon is pegged to SPCX, which has a highly liquid secondary market, meaning potential auction outcomes can be assessed using both tokenised and traditional secondary market data.

## Market Risk

Maximum Drawdown, 48h close-to-close: 19.40%

Using Yahoo Finance daily OHLC data for SPCX from its first trading day on 12 June 2026 to 24 September 2026:

Current price: $148.03

Listing/reference price: $150.00

First trading-day close: $160.95, after an intraday high of $176.52

Highest observed intraday price: $225.64 on 16 June 2026

Lowest observed intraday price: $104.83 on 3 August 2026

Worst 24h close-to-close drawdown: -16.4% from 18 June to 22 June 2026

Worst 48h close-to-close drawdown: -19.4% from 17 June to 22 June 2026

The first weeks after a public listing are usually the most volatile, as the market is still finding an appropriate price. This is visible in SPCX: the strongest upside move and the worst close-to-close drawdown both occurred shortly after trading began. The asset moved from a first-day close of $160.95 to an intraday high of $225.64 only two trading days later, before falling sharply to $154.60 by 22 June.

This means a retained reserve of 30% should be applied as the maximum drawdown is based on a very limited trading history. This way, it should cover market volatility under normal circumstances and account for the challenger reward.

## Tail Risks

### Counterparty Risk: SpaceX

Description: SPCXon ultimately references the equity value of Space Exploration Technologies Corp. The collateral is therefore exposed to company-specific tail events affecting SpaceX.

Probability: Medium

Severity: Severe

Compensation: 1.00%

SpaceX is a large and strategically important publicly listed company. Severe tail scenarios could materially impair the equity value, including fraud, governance failure, major operational disruption, a failed launch with significant financial or reputational consequences, regulatory intervention, loss of key contracts, or a material deterioration in investor confidence.

These risks are not captured by ordinary short-term price volatility alone. A 1.00% compensation is therefore assigned to account for the single-company counterparty and business-risk exposure of the underlying asset.

### Counterparty Risk: Ondo Finance

Description: SPCXon depends on Ondo’s tokenized-asset issuance, redemption, operational, and custody structure.

Probability: Low

Severity: Moderate

Compensation: 0.25%

Even if the underlying SpaceX exposure remains valuable, liquidation efficiency may be impaired if Ondo fails in its duties as an issuer, leading to depegs from the underlying stock price.

### Smart Contract Risk: Smart-Contract Exploit

Description: SPCXon is implemented as an ERC-20 token linked to a real-world asset off-chain, and therefore carries residual smart-contract risk.

Probability: Low

Severity: Critical

Compensation: 0.50%

The probability of a major smart-contract issue appears low, but the severity could be critical if the token contract or transfer mechanics were impaired.

Unlike a native asset, the collateral value depends on the underlying equity exposure in custody and the correct representation of the tokenized wrapper, meaning that a technical issue could lead to unbacked tokens or impaired transferability.

### Governance Risk: Transfer restrictions / admin controls

Description: SPCXon is a tokenized security-style asset and carries transfer, compliance, redemption, or admin-control considerations.

Probability: Low

Severity: Severe

Compensation: 0.50%

Tokenized securities generally require admin and compliance controls. These controls are not automatically disqualifying, but they introduce risk because transferability may depend on issuer-controlled compliance and pause mechanisms.

For Frankencoin, the relevant governance risk is the possibility that transferability could be impaired for example due to a regulator request to freeze certain tokens.

### Legal Risk: n/a

Description: No separate legal-risk premium is assigned in the current classification.

Probability: n/a

Severity: n/a

Compensation: n/a

Legal and regulatory considerations are mainly captured through the counterparty and governance/admin-control risk categories. No additional standalone legal-risk premium is assigned to avoid double-counting.

### Liquidity Risk: Secondary-market or redemption impairment

Description: SPCXon liquidity depends on both token-level secondary markets and the ability of eligible participants to access Ondo’s issuance and redemption mechanics.

Probability: Negligible

Severity: n/a

Compensation: 0%

Liquidity is available through multiple independent venues. No compensation is required.

### Contagion Risk: n/a

Description: No separate contagion-risk premium is assigned.

Probability: n/a

Severity: n/a

Compensation: 0%

SPCXon is primarily exposed to single-name equity risk and tokenized-security infrastructure risk, not to correlated DeFi contagion. No separate contagion premium is assigned under the current classification.

## Conclusion

SPCXon is a credible collateral candidate for Frankencoin.

PCX has shown significant post-listing volatility, with a worst 48h close-to-close drawdown of 19.4%. The price history is however limited, so a retained reserve of 30% should be applied.

The total risk premium of 2.25% compensates FPS holders for the the counterparty risk of SpaceX, the issuer risk of Ondo Finance, as well as smart-contract and governance risk.
