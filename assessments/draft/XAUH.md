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
          "name": "Herculis Group",
          "probability": "Medium",
          "severity": "Severe",
          "compensation": "1.00%"
        }
      ],
      "smart_contract_risks": [
        {
          "name": "Smart-Contract Exploit",
          "probability": "Very Low",
          "severity": "Critical",
          "compensation": "0.5%"
        }
      ],
      "governance_risks": [
        {
          "name": "Issuer/admin-control and custody intervention risk",
          "probability": "Low",
          "severity": "Severe",
          "compensation": "0.5%"
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
          "name": "Secondary Market Liquidity & Minting/Redemption Impairment",
          "probability": "Low",
          "severity": "Severe",
          "compensation": "0.5%"
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
    "retained_reserve": 0.25,
    "target_interest_rate": 0.025,
    "global_minting_limit": 250000,
    "liquidation_price": 80.00,
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

XAUH, however, is a tokenized-gold wrapper with a limited track record. Therefore, an initial global minting limit of ZCHF 250,000 and an interest rate of 2.5% are applied to contain the exposure and compensate FPS holders for the associated tail risks. 

## Introduction

XAUH is an ERC-20 token that gives holders exposure to physical gold. Herculis describes the asset as backed by Swiss-stored, insured, and audited LBMA 999.9 gold, with regular custody attestation by KPMG Switzerland. XAUH also exists on other networks, including TON and TRON. From a minimum of 500 XAUH, physical redemptions are possible for KYC-ed holders at a 3% redemption fee plus applicable transportation and insurance costs.

Herculis Tokens SA is incorporated in Panama as a subsidiary of Herculis Group, a Swiss Wealth Management & Asset Protection boutique founded in 2009, and aims to offer a more transparent and secure way for investors to participate in the gold market without the frictions typically associated with traditional gold investments.

## Free Float/Liquidity

Classification: Sufficient

XAUH currently has a highly concentrated holder distribution on Ethereum: around 86% of supply is held in a single issuer-controlled address, while roughly 9% sits in the Uniswap pool. Over the coming weeks, Herculis plans to expand Uniswap liquidity, add Ethereum XAUH support to the existing Biconomy and BTSE listings, and integrate Ethereum XAUH with its live merchant/on-ramp integrations such as ChangeNOW, Changelly and Wert. The holder distribution is expected to improve as soon as these listings and integrations are finalised.

Importantly, XAUH also has a documented primary-market minting mechanism. KYC-approved customers can request new issuance either by contributing eligible physical gold or by transferring FIAT for newly issued XAUH. The free float is therefore considered sufficient for now, and is expected to become stronger when the planned listings and integrations are finalised.

## Public Information

Classification: Strong

Public information is strong. XAUH has a public website, whitepaper, Ethereum token contract, CoinGecko listing, and public market data.

Since the underlying is Gold, other gold markets can be used as a reference to derive the XAUH token price with applying a potential discount for the physical redemption and delivery process.

## Market Risk

99%-VaR, 96h close-to-close: 8.46%

Maximum Drawdown, 96h close-to-close: 12.00%

To account for ordinary gold-price volatility over 96h, the 2% challenger reward, and applying an additional haircut for liquidation costs and potential time delays, a 25% minter reserve appears appropriate.

## Tail Risks

### Counterparty Risk: Herculis Group

Description: XAUH depends on Herculis as issuer, the custody of the underlying gold, and the operational process linking the token to the physical gold.

Probability: Low

Severity: Severe

Compensation: 1.00%

XAUH is a tokenized wrapper whose value depends on the issuer, custody structure, reserve documentation, redemption process, and market confidence.

A failure in any of these components could impair the token relative to the underlying gold price. This risk is higher than for larger tokenized-gold products with longer operating histories, and the token could depeg more significantly from the underlying gold price in such a scenario. A 1.00% compensation is therefore assigned for issuer, custody, and redemption dependency.

### Smart Contract Risk: Smart-Contract Exploit

Description: XAUH depends on an upgradeable Ethereum token contract with issuer-admin functionality.

Probability: Low

Severity: Critical

Compensation: 0.50%

The Ethereum token contract is an upgradeable proxy and includes administrative controls. Reviewed functionality indicates controls such as freeze, unfreeze, wipe of frozen addresses, pause, unpause, supply adjustment, supply-controller assignment, asset-protection role assignment, and fee-controller functions.

Such controls are common for centrally issued RWA tokens, but they introduce dependency on correct administration, secure key management, and predictable issuer behaviour. A contract-level issue, malicious upgrade, compromised admin key, pause, freeze, wipe, or supply-control error could impair transferability, settlement, or liquidation proceeds. A 0.5% compensation is assigned for smart-contract risk.

### Governance Risk: Issuer/admin-control and custody intervention risk

Description: XAUH is a centrally issued tokenized commodity and thus carries issuer-admin, address-blocking, and government intervention risk.

Probability: Low

Severity: Severe

Compensation: 0%

XAUH is centrally issued and backed by physical gold held in custody. The token contract includes address-level blocking controls, including functions to add or remove addresses from a blocked list, check whether an address is blocked, and destroy funds held by a blocked address.

Because the underlying gold is stored physically in identifiable custody arrangements, legal, regulatory, or administrative intervention could also impair redemption, secondary-market confidence, or the economic link between XAUH and physical gold. This is captured under governance/admin-control risk for consistency with other tokenized off-chain assets. A 0.50% compensation is assigned for this residual risk.

### Legal Risk: n/a

Description: No separate legal-risk premium is assigned in the current classification.

Probability: n/a

Severity: n/a

Compensation: 0%

Legal and operational considerations are mainly captured through counterparty/custody risk and governance/admin-control risk. No additional standalone legal-risk premium is assigned to avoid double-counting.

### Liquidity Risk: Secondary Market Liquidity & Minting/Redemption Impairment

Description: Ethereum XAUH liquidity is limited, and the holder base currently very concentrated.

Probability: Medium

Severity: Severe

Compensation: 0.50%

The practical Ethereum liquidity source is currently the Uniswap pool as well as the direct minting/redemption path.

This means that a Frankencoin liquidation could face a meaningful discount, as arbitrageurs would apply a haircut due to the limited possibility to sell the tokens on Uniswaps for a profit right away, and additional costs and frictions for primary market redemptions. A 0.50% compensation is assigned for liquidity risk.

### Contagion Risk: n/a

Description: No separate contagion-risk premium is assigned.

Probability: Negligible

Severity: n/a

Compensation: 0%

No separate contagion-risk premium is assigned as XAUH does not depend on crypto markets and has no other Defi integrations.

## Conclusion

The proposed retained reserve of 25% is appropriate relative to expected market volatilty of the underlying gold exposure, and leaves a substantial buffer for liquidation execution. It should not be interpreted as protection against issuer, custody, redemption, admin-control, or liquidity tail risks. Those risks are addressed primarily through the proposed 250,000 ZCHF global minting limit and the 2.5% target interest rate.

The target interest rate of 2.5% is justified by the selected risk premia: 1.00% for issuer, custody, and redemption dependency, 0.5% for smart-contract and admin-control risk, 0.5% for governance risks, and 0.5% for liquidity risk as described.

The proposed 250,000 ZCHF global minting limit is the primary safeguard as long as the free float and liquidity of the token are limited. The issuer has however indicated plans of growing the Ethereum version with additional integrations and CEX listings. A higher global minting limit should then be possible.
