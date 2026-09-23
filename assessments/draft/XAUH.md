---
{
  "asset_name": "Herculis Gold Coin",
  "asset_ticker": "XAUH",
  "contract_address": "0xa9b17f572341219703bc951725bdb3ca756b1a65",
  "assessment_date": "2026-09-23",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0xa9b17f572341219703bc951725bdb3ca756b1a65",
    "coingecko": "https://www.coingecko.com/en/coins/herculis-gold-coin",
    "website": "https://xauh.gold/",
    "docs": "https://xauh.gold/whitepaper.pdf",
    "other": "https://dexscreener.com/ethereum/0x03852AE3df6DE29ea7B9E4077cD63A3E3e14832C"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Sufficient",
    "market_risk": "12.00%",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "Issuer, custody and redemption dependency",
          "probability": "Medium",
          "severity": "Severe",
          "compensation": "1.00%"
        }
      ],
      "smart_contract_risks": [
        {
          "name": "Admin-control risk",
          "probability": "Very Low",
          "severity": "Critical",
          "compensation": "0.5%"
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
          "name": "Thin Ethereum liquidity and concentrated holder base",
          "probability": "Medium",
          "severity": "Severe",
          "compensation": "1.00%"
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
    "retained_reserve": 0.20,
    "target_interest_rate": 0.025,
    "global_minting_limit": 100000,
    "liquidation_price": 100.00,
    "maturity": null,
    "auction_duration": 48,
    "minimum_collateral": null
  }
}
---

# Collateral Risk Assessment: Herculis Gold Coin

## Summary

XAUH is a tokenized gold product issued by Herculis Tokens SA. Each XAUH token represents exposure to one gram of Swiss-stored LBMA 999.9 physical gold.

The underlying RWA exposure is gold, which is a high-quality collateral asset with low expected market volatility.

A conservative global minting limit of ZCHF 250,000 and an interest rate of 2.5% are however required to address XAUH's nature as a tokenized-gold wrapper with issuer, custody, redemption, admin-control risk, and limited liquidity.

## Introduction

XAUH is an ERC-20 token that gives holders exposure to physical gold. The issuer describes the asset as backed by Swiss-stored, insured, and audited LBMA 999.9 gold, with regular audit reports by KPMG. XAUH also exists on other networks, including TON and TRON.

The relevant collateral exposure for Frankencoin is the Ethereum version of XAUH. Liquidity, redemption, transferability, and liquidation feasibility must therefore be assessed on the Ethereum token itself. Liquidity on TON, TRON, or other networks should not currently be counted toward Ethereum liquidation depth unless reliable cross-chain conversion is available to ordinary market participants.

The primary liquidity therefore arises from the XAUH/USDT Uniswap pool, until the listings on BTSE and Biconomy also include the Ethereum token version (currently, only TON & TRON are available).

## Free Float/Liquidity

Classification: Sufficient

XAUH has a limited free float, 86% of tokens are held on a single address, while about 9% is available in the Uniswap pool. A test transaction of 2,500 USDT worth of XAUH already incurs a 5% slippage, and a 10,000 USDT transaction a 17% slippage. The liquidity is therefore deemed to be very thin, and a challenge would require multiple rounds to liquidate a large position.

This means a global minting limit of 100,000 ZCHF seems reasonable for the start given the limited free float available.

At the full 100,000 ZCHF minting limit, up to 80,000 ZCHF could be withdrawn at a 20% reserve requirement.

## Public Information

Classification: Strong

Public information is strong. XAUH has a public website, whitepaper, Ethereum token contract, CoinGecko listing, and public market data.

Since the underlying is Gold, other gold markets can be used as a reference to derive the XAUH token price with applying a potential discount for the physical redemption and delivery process.

## Market Risk

99%-VaR, 96h close-to-close: 8.46%

Maximum Drawdown, 96h close-to-close: 12.00%

A 20% reserve is therefore defensible against historical 96h close-to-close gold-price moves and leaves an additional buffer for challenger rewards, and a potential liquidation delay.

The underlying exposure is one gram of gold. Gold is materially less volatile than most crypto-native collateral, which supports a lower ordinary market-risk reserve than would be appropriate for crypto-native assets.

## Tail Risks

### Counterparty Risk: Issuer, custody and redemption dependency

Description: XAUH depends on Herculis as issuer, the custody of the underlying gold, and the operational process linking the token to the physical gold.

Probability: Low

Severity: Severe

Compensation: 1.00%

XAUH is a tokenized wrapper whose value depends on the issuer, custody structure, reserve documentation, redemption process, and market confidence.

A failure in any of these components could impair the token relative to the underlying gold price. This risk is materially higher than for larger tokenized-gold products with longer operating histories and deeper liquidity. A 1.00% compensation is therefore assigned for issuer, custody, and redemption dependency.

### Smart Contract Risk: Admin-control risk

Description: XAUH depends on an upgradeable Ethereum token contract with issuer-admin functionality.

Probability: Low

Severity: Critical

Compensation: 0.50%

The Ethereum token contract is an upgradeable proxy and includes administrative controls. Reviewed functionality indicates controls such as freeze, unfreeze, wipe of frozen addresses, pause, unpause, supply adjustment, supply-controller assignment, asset-protection role assignment, and fee-controller functions.

Such controls are common for centrally issued RWA tokens, but they introduce dependency on correct administration, secure key management, and predictable issuer behaviour. A contract-level issue, malicious upgrade, compromised admin key, pause, freeze, wipe, or supply-control error could impair transferability, settlement, or liquidation proceeds. A 0.75% compensation is assigned for smart-contract and admin-control risk.

### Governance Risk: n/a

Description: No separate governance-risk premium is assigned.

Probability: n/a

Severity: n/a

Compensation: 0%

XAUH is centrally issued rather than governed by a decentralized protocol. The relevant control risks are captured under counterparty, smart-contract/admin-control, and liquidity risk. No separate governance-risk premium is assigned to avoid double-counting.

### Legal Risk: n/a

Description: No separate legal-risk premium is assigned in the current classification.

Probability: n/a

Severity: n/a

Compensation: 0%

Legal and redemption enforceability are relevant for XAUH, especially around holder eligibility, redemption rights, transfer restrictions, custody claims, and whether an auction buyer can reliably receive, hold, transfer, or redeem XAUH.

For the current parameter set, this risk is treated as part of the issuer, custody, and redemption dependency rather than as a separate premium. If the legal terms create additional restrictions for ordinary auction buyers, the parameters should be reassessed.

### Liquidity Risk: Thin Ethereum liquidity and concentrated holder base

Description: Ethereum XAUH liquidity is limited, and the holder base currently very concentrated.

Probability: Medium

Severity: Severe

Compensation: 1.00%

The practical Ethereum liquidity source is currently the Uniswap pool. TON and TRON liquidity cannot currently be treated as immediately available for Ethereum liquidations. The issuer has also indicated that bridging is not yet possible for users and primarily available to the issuer.

This means that a Frankencoin liquidation could face meaningful slippage, execution delay, or dependence on a small buyer universe. The 48h auction duration is therefore appropriate. A 1.00% compensation is assigned for liquidity risk.

### Contagion Risk: n/a

Description: No separate contagion-risk premium is assigned.

Probability: Negligible

Severity: n/a

Compensation: 0%

No separate contagion-risk premium is assigned as XAUH does not depend on crypto markets and has no other Defi integrations.

## Conclusion

The proposed retained reserve of 20% is appropriate relative to the observed 12.00% worst 96h close-to-close gold drawdown and leaves a substantial buffer for liquidation execution. It should not be interpreted as protection against issuer, custody, redemption, admin-control, or liquidity tail risks. Those risks are addressed primarily through the proposed 100,000 ZCHF global minting limit and the 2.75% target interest rate.

The target interest rate of 2.5% is justified by the selected risk premia: 1.00% for issuer, custody, and redemption dependency, 0.5% for smart-contract and admin-control risk, and 1.00% for thin Ethereum liquidity and holder concentration.

The proposed 100,000 ZCHF global minting limit is the primary safeguard as long as the free float of the token is so limited. The issuer has however indicated plans of growing the Ethereum version with additional integrations and CEX listings. A higher global minting limit should then be possible.
