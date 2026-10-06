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
      "liquidity_risks": [
        {
          "name": "Secondary Market Liquidity & Minting/Redemption Impairment",
          "probability": "Low",
          "severity": "Severe",
          "compensation": "0.5%"
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
    "minimum_collateral": 10
  }
}
---

# Collateral Risk Assessment: Herculis Gold Coin

## Summary

XAUH is a tokenized gold product issued by Herculis Tokens SA. Each XAUH token represents exposure to one gram of Swiss-stored LBMA 999.9 physical gold. Herculis describes the asset as backed by Swiss-stored, insured, and audited gold, with regular custody attestation by KPMG Switzerland. XAUH also exists on other networks, including TON and TRON. From a minimum of 500 XAUH, physical redemptions are possible for KYC-ed holders at a 3% redemption fee plus applicable transportation and insurance costs.

The underlying exposure is high-quality and relatively low-volatility, but XAUH is still a small tokenized wrapper with issuer, custody, admin-control, and liquidity tail risks. Herculis Tokens SA is incorporated in Panama as a subsidiary of Herculis Group, a Swiss Wealth Management & Asset Protection boutique founded in 2009.

The proposed 25% retained reserve addresses ordinary gold-price volatility and liquidation execution risk. The proposed 250,000 ZCHF global minting limit and 2.5% target interest rate are the main safeguards against the wrapper-specific tail risks.

## Free Float

Classification: Sufficient

XAUH currently has a highly concentrated holder distribution on Ethereum: around 78% of supply is held in a single issuer-controlled address, while roughly 17% sits in the Uniswap pool. Over the coming weeks, Herculis plans to expand Uniswap liquidity, add Ethereum XAUH support to the existing Biconomy and BTSE listings, and promote the Ethereum version with its merchant integrations such as ChangeNOW, Changelly and Wert. The holder distribution is expected to improve as these listings and integrations progress.

Importantly, XAUH also has a documented primary-market minting mechanism. KYC-approved customers can request new issuance either by contributing eligible physical gold or by transferring FIAT for newly issued XAUH.

Based on these characteristics, a 250,000 ZCHF minting limit is reasonable.

## Public Information

Classification: Strong

XAUH references a highly liquid and observable gold market, and the issuer provides regular attestations for the underlying reserves.

Challengers should therefore be able to estimate likely auction outcomes by referencing the gold price, applying any redemption and liquidity discount, and accounting for the stated redemption process and fees.

## Market Risk

99%-VaR, 96h close-to-close: 8.46%

Maximum Drawdown, 96h close-to-close: 12.00%

To account for ordinary gold-price volatility over 96h, the 2% challenger reward, and applying an additional haircut for liquidation costs and potential time delays, a 25% minter reserve appears appropriate.

## Tail Risks

### Counterparty Risk: Herculis Group

Likelihood: Medium

Severity: Severe

Compensation: 1.00%

Assessment: XAUH is a tokenized wrapper whose value depends on Herculis as issuer, the custody of the underlying gold, the redemption process, and market confidence. A failure in any of these components could impair the token relative to the underlying gold price. This risk is higher than for larger tokenized-gold products with longer operating histories, and the token could depeg more significantly from the underlying gold price in such a scenario. A 1.00% compensation is therefore assigned for issuer, custody, and redemption dependency.

### Smart Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

Assessment: XAUH depends on an upgradeable Ethereum token contract with issuer-admin functionality. Reviewed functionality indicates controls such as freeze, unfreeze, wipe of frozen addresses, pause, unpause, supply adjustment, supply-controller assignment, asset-protection role assignment, and fee-controller functions. Such controls are common for centrally issued RWA tokens, but they introduce dependency on correct administration, secure key management, and predictable issuer behaviour. A contract-level issue, malicious upgrade, compromised admin key, pause, freeze, wipe, or supply-control error could impair transferability, settlement, or liquidation proceeds. A 0.50% compensation is assigned for smart-contract risk.

### Governance Risk: Issuer/admin-control and custody intervention risk

Likelihood: Low

Severity: Severe

Compensation: 0.50%

Assessment: XAUH is issued by Herculis Tokens SA, while the underlying physical gold is held in custody in Switzerland. Herculis Tokens SA is incorporated in Panama and reports to the local regulator. This creates a governance/admin-control risk because the regulator in Panama could potentially require the issuer to freeze or restrict operations.

The token contract also includes address-level blocking controls, including functions to add or remove addresses from a blocked list, check whether an address is blocked, and destroy funds held by a blocked address. These controls are not unusual for centrally issued RWA tokens, but they create a residual governance/admin-control risk for Frankencoin liquidations. A 0.50% compensation is assigned for this risk.

### Liquidity Risk: Secondary Market Liquidity & Minting/Redemption Impairment

Likelihood: Low

Severity: Severe

Compensation: 0.50%

Assessment: Ethereum XAUH liquidity is limited and holder concentration is high. In a liquidation, challengers may struggle to acquire sufficient XAUH quickly if the Uniswap pool or direct minting/redemption path is unavailable or costly.

The exit path could also be impaired because secondary-market depth is limited and primary redemption involves KYC, minimum sizes, fees, delivery costs, and timing frictions. Arbitrageurs would therefore likely apply a haircut for delayed exit and redemption uncertainty. A 0.50% compensation is assigned for this risk.

## Conclusion

The proposed retained reserve of 25% is appropriate relative to expected market volatilty of the underlying gold exposure, and leaves a substantial buffer for liquidation execution. It should not be interpreted as protection against issuer, custody, redemption, admin-control, or liquidity tail risks. Those risks are addressed primarily through the proposed 250,000 ZCHF global minting limit and the 2.5% target interest rate.

The target interest rate of 2.5% is justified by the selected risk premia: 1.00% for counterparty risk, 0.5% for smart-contract, 0.5% for governance risks, and 0.5% for liquidity risk as described.

The proposed 250,000 ZCHF global minting limit is the primary safeguard as long as the free float and liquidity of the token are limited. The issuer has however indicated plans of growing the Ethereum version with additional integrations and CEX listings. A higher global minting limit should then be possible.
