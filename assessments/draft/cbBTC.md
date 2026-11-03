---
{
  "asset_name": "Coinbase Wrapped Bitcoin",
  "asset_ticker": "cbBTC",
  "contract_address": "0xcbB7C0000aB88B473b1f5aFd9ef808440eed33Bf",
  "assessment_date": "2026-11-03",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/address/0xcbB7C0000aB88B473b1f5aFd9ef808440eed33Bf",
    "coingecko": "https://www.coingecko.com/en/coins/coinbase-wrapped-btc",
    "website": "https://www.coinbase.com/cbbtc",
    "docs": "https://resources.cryptocompare.com/asset-management/16852/1726235547660.pdf",
    "other": "https://www.coinbase.com/cbbtc/proof-of-reserves"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "16.24%",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "Coinbase",
          "probability": "Very Low",
          "severity": "Severe",
          "compensation": "0.25%"
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
          "name": "Admin-Control",
          "probability": "Very Low",
          "severity": "Critical",
          "compensation": "0.50%"
        }
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.20,
    "target_interest_rate": 0.01,
    "global_minting_limit": "no limit",
    "maturity": "3 years",
    "auction_duration": 24,
    "minimum_collateral": 0.10
  }
}
---

# Collateral Risk Assessment: Coinbase Wrapped Bitcoin

## Summary

cbBTC is Coinbase's ERC-20 representation of Bitcoin. It is a strong collateral candidate because it provides liquid BTC exposure on Ethereum, while the proposed 20% retained reserve exceeds the observed worst 48-hour close-to-close drawdown.

The residual risks arise from Coinbase's custody, issuance and redemption role, the token-contract architecture, and Coinbase-controlled admin functions.

## Asset Overview

cbBTC represents BTC held in Coinbase custody and is issued for use across Ethereum-compatible applications. The collateral exposure is therefore primarily Bitcoin market risk, with an additional centralised-wrapper layer: Coinbase controls issuance and redemption and the Ethereum token is implemented through an upgradeable FiatToken proxy architecture.

## Free Float

Classification: Strong

cbBTC has broad market access through Coinbase and established decentralised-exchange liquidity. Independent challengers and auction buyers can acquire and sell the token without relying on a single bilateral counterparty.

## Public Information

Classification: Strong

BTC has deep and transparent global markets, while cbBTC has public contract information, observable secondary-market pricing and Coinbase reserve disclosures. Challengers can reasonably estimate auction outcomes.

## Market Risk

99%-VaR, 48h close-to-close: 8.11%

Worst historical 48h close-to-close drawdown: 16.24%

The metrics use two years of daily close data. A 20% retained reserve exceeds the observed worst 48-hour drawdown and provides additional room for challenger reward and auction execution.

## Tail Risks

### Counterparty Risk: Coinbase

Likelihood: Very Low

Severity: Severe

Compensation: 0.25%

cbBTC depends on Coinbase for BTC custody, issuance and redemption. A Coinbase operational, custody or redemption disruption could impair recoverable value even if BTC itself remains valuable.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Severe

Compensation: 0.25%

cbBTC uses an upgradeable FiatToken proxy and a FiatTokenV2_1 implementation. The implementation includes standard ERC-20 functions, permit and authorisation functions, and privileged minting, burning, pausing and blacklisting functionality. These controls are expected for a centrally issued BTC wrapper; the technical premium covers an exploit, proxy or implementation failure that independently impairs token balances or transferability.

### Governance Risk: Admin-Control

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

Privileged roles can blacklist and unblacklist addresses, pause and unpause the token, configure or remove minters, update role holders, and upgrade the proxy implementation. A realised address-level blacklist, transfer restriction or malicious/compromised upgrade could make collateral unrecoverable.

## Conclusion

The 20% retained reserve provides a reasonable buffer against the 16.24% worst historical 48h close-to-close drawdown. The 1.0% effective interest rate compensates the assessed tail risks. The framework does not require a cap on the global minting limit based on the tail risk analysis; cbBTC’s high liquidity supports a 24-hour auction duration, and its established market position makes a maturity of 3 years reasonable before the collateral needs to be reassessed.
