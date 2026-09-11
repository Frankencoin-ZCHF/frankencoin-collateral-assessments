---
{
  "asset_name": "Bitget Token",
  "asset_ticker": "BGB",
  "contract_address": "0x54D2252757e1672EEaD234D27B1270728fF90581",
  "assessment_date": "2026-09-11",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x54D2252757e1672EEaD234D27B1270728fF90581",
    "coingecko": "https://www.coingecko.com/en/coins/bitget-token",
    "website": "https://www.morphl2.io/",
    "docs": "https://docs.morphl2.io/",
    "other": "https://github.com/Frankencoin-ZCHF/Frankencoin/discussions/112"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "22.07%",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "Bitget / Morph ecosystem dependency",
          "probability": "Medium",
          "severity": "Critical",
          "compensation": "3.00%"
        }
      ],
      "smart_contract_risks": [
        {
          "name": "Smart-Contract Risk",
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
          "name": "Exchange-concentrated liquidity",
          "probability": "Low",
          "severity": "Severe",
          "compensation": "0.50%"
        }
      ],
      "contagion_risks": [
        {
          "name": "Crypto exchange and market contagion",
          "probability": "Medium",
          "severity": "Moderate",
          "compensation": "1.25%"
        }
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.40,
    "target_interest_rate": 0.05,
    "global_minting_limit": 2000000,
    "liquidation_price": 0.99,
    "maturity": null,
    "auction_duration": 24,
    "minimum_collateral": null
  }
}
---

# Collateral Risk Assessment: Bitget Token

## Summary

BGB is the native gas, governance, and ecosystem token of Morph, a payments-focused Ethereum Layer 2 closely linked to the broader Bitget ecosystem.

BGB is a strong but non-standard collateral candidate. It has strong public information, strong secondary-market availability, and meaningful market capitalization, but its collateral quality depends heavily on Bitget's exchange business, liquidity support, and continued commitment to BGB.

## Introduction

BGB was originally launched as an incentive and utility token for Bitget users and has since been upgraded to serve as the gas and governance token for Morph. Morph is a payments-focused Ethereum Layer 2 settlement layer with native stablecoin support and broader integrations across the Bitget and payments ecosystem.

The relevant collateral exposure is therefore not a neutral crypto asset like BTC or ETH. It is exposure to an exchange- and sponsor-linked ecosystem token whose value depends on Bitget's exchange business, Morph adoption, token utility, and continued market confidence.

Bitget has a strong incentive to maintain liquidity, credibility, and utility around BGB. This strategic linkage is also the main collateral risk.

## Free Float/Liquidity

Classification: Strong

BGB has a meaningful market capitalization, a multi-year trading history, and secondary-market availability across centralized exchanges such as Bitget, Kraken, MEXC, Bitfinex, and others.

Liquidity is nevertheless concentrated. Most BGB trading volume takes place on Bitget, while on-chain liquidity is materially smaller. This makes BGB liquid in normal market conditions, but dependent on the continued operation and market confidence of Bitget.

## Public Information

Classification: Strong

Public information is strong. BGB has public exchange pricing, a CoinGecko listing, a multi-year trading history, public token information, and public ecosystem documentation through Bitget and Morph.

Bitget also publishes monthly proof-of-reserve information, which provides useful transparency on the exchange's reserve position. This does not eliminate operational, security, or solvency risk, but it improves public observability.

## Market Risk

99%-VaR, 48h close-to-close: 13.27%

Maximum Drawdown, 48h close-to-close: 22.07%

BGB's observed 48h close-to-close market-risk metrics remain below the proposed 40% retained reserve. The 40% reserve is therefore defensible against historical close-to-close price moves and leaves an additional buffer for challenger rewards and liquidation execution.

Daily close-to-close data can nevertheless understate very short-term stress. In October 2024, BGB briefly fell by more than 50% intraday before recovering quickly. Frankencoin's slower auction-based liquidation process is helpful for this type of flash crash, as the auction mechanism gives the market time to normalize before collateral is sold.

## Tail Risks

### Counterparty Risk: Bitget / Morph ecosystem dependency

Description: BGB depends on Bitget's exchange business, brand, liquidity support, and continued commitment to BGB and Morph.

Probability: Medium

Severity: Critical

Compensation: 3.00%

This is the dominant tail risk. BGB is not a redeemable claim on Bitget, but its market value is closely linked to Bitget's exchange franchise and the broader Bitget/Morph ecosystem. If Bitget suffered a severe solvency, operational, regulatory, or security event, BGB could lose market confidence very quickly.

The relevant adverse comparison is the FTX collapse, where FTT lost most of its value within 48 hours once confidence in FTX's solvency broke. A 40% reserve requirement would not protect against such an extreme exchange-token collapse. The correct control is therefore a conservative global minting limit, combined with an interest premium that compensates FPS holders for bearing this residual tail risk.

Global Minting Limit: 2,000,000 ZCHF

At the full 2,000,000 ZCHF minting limit, up to 1,200,000 ZCHF could be withdrawn at a 40% reserve requirement. If BGB suffered an FTX-style collapse, the remaining collateral value could be materially impaired. The global minting limit therefore needs to remain conservative and well below the size of the equity pool, so that even an extreme Bitget-related event cannot threaten the system's survival.

### Smart Contract Risk: Smart-Contract Risk

Description: BGB depends on the Ethereum ERC-20 token contract and related bridge and market infrastructure.

Probability: Very Low

Severity: Severe

Compensation: 0.25%

BGB is an established ERC-20 token with a multi-year history. A review of the Ethereum token contract did not indicate standard admin freeze, blacklist, or direct admin minting controls. Smart-contract risk is therefore considered very low, but not zero.

Residual technical risk remains around ERC-20 transferability, exchange infrastructure, bridge infrastructure, and the broader Morph/CCIP ecosystem. A 0.25% compensation is assigned.

### Governance Risk: n/a

Description: No separate governance-risk premium is assigned in the current classification.

Probability: n/a

Severity: n/a

Compensation: 0%

BGB has governance relevance within Morph, but the dominant risk is not decentralized governance failure. The relevant issue is Bitget/Morph sponsor dependency, token-utility policy, and ecosystem execution, which is already captured under counterparty and ecosystem dependency. No separate governance-risk premium is assigned to avoid double-counting.

### Legal Risk: n/a

Description: No separate legal-risk premium is assigned in the current classification.

Probability: n/a

Severity: n/a

Compensation: 0%

BGB is not a tokenized security, custodial wrapper, or redeemable off-chain claim. Regulatory or legal pressure on Bitget could affect BGB indirectly, but this is captured through the Bitget / Morph ecosystem dependency risk rather than as a separate legal-risk premium.

### Liquidity Risk: Exchange-concentrated liquidity

Description: BGB liquidity is meaningful in normal markets, but highly concentrated on Bitget and therefore vulnerable to exchange-specific stress.

Probability: Low

Severity: Severe

Compensation: 0.50%

Current BGB liquidity is sufficient for the proposed initial allocation, but it is not venue-neutral. Most trading volume is concentrated on Bitget, while alternative centralized venues and on-chain liquidity are smaller.

If Bitget were impaired or trading were disrupted, BGB liquidity could deteriorate at the same time as the token price falls. This concentration justifies a separate 0.50% liquidity-risk premium.

### Contagion Risk: Crypto exchange and market contagion

Description: BGB may be affected by broader crypto-market stress, exchange-token repricing, and loss of confidence in centralized exchange tokens.

Probability: Medium

Severity: Moderate

Compensation: 1.25%

BGB is exposed to broader crypto-market sentiment and to contagion across centralized exchange tokens. In a sector-wide exchange-stress event, BGB could reprice more sharply than ordinary market volatility suggests.

The 40% retained reserve reduces the expected system impact of this contagion risk. A 1.25% compensation is assigned for residual contagion risk beyond the ordinary market-risk buffer.

## Conclusion

BGB is an acceptable but higher-risk collateral candidate for Frankencoin.

The proposed retained reserve of 40% is appropriate relative to the observed 22.07% worst 48h close-to-close drawdown and leaves a substantial buffer for liquidation execution. The target interest rate of 5.0% is justified by the selected risk premia: 3.00% for Bitget / Morph ecosystem dependency, 0.25% for smart-contract risk, 0.50% for liquidity concentration, and 1.25% for crypto exchange and market contagion risk.

The proposed 2,000,000 ZCHF global minting limit is the primary safeguard against an extreme Bitget-related tail event. The Association therefore views a one-year maturity as a reasonable starting point, allowing the collateral and its minting parameters to be reassessed within a clear timeframe.
