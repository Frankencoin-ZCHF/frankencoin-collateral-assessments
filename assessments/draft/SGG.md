---
{
  "asset_name": "Swissgrams Gold",
  "asset_ticker": "SGG",
  "contract_address": "0x2Bd214946806DbEE88Dd3b44b26A21759723d8A2",
  "assessment_date": "2026-10-06",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x2Bd214946806DbEE88Dd3b44b26A21759723d8A2",
    "coingecko": "n/a",
    "website": "https://swissgrams.com/",
    "docs": "https://swissgrams.com/token-terms/",
    "other": "https://swissgrams.com/token-backing/"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Sufficient",
    "market_risk": "12.00%",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "Swissgrams AG",
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
          "compensation": "0.50%"
        }
      ],
      "governance_risks": [
        {
          "name": "Swiss-law issuer/admin-control risk",
          "probability": "Negligible",
          "severity": "Moderate",
          "compensation": "0.00%"
        }
      ],
      "liquidity_risks": [
        {
          "name": "Secondary Market Liquidity & Physical Redemption",
          "probability": "Low",
          "severity": "Severe",
          "compensation": "0.50%"
        }
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.25,
    "target_interest_rate": 0.020,
    "global_minting_limit": 250000,
    "liquidation_price": 3000,
    "maturity": null,
    "auction_duration": 48,
    "minimum_collateral": 2.5
  }
}
---

# Collateral Risk Assessment: Swissgrams Gold

## Summary

SGG is a tokenized gold product issued by Swissgrams AG in Zug, Switzerland. Each SGG represents one troy ounce of gold content in physical sovereign coins stored in Switzerland. Eligible reserve coins include 1 oz American Gold Eagles, Maple Leafs, Vienna Philharmonics, Britannias and Kangaroos. Tokens are only released into circulation against a matching deposit of coins into the reserve.

The underlying exposure is high-quality and relatively low-volatility. Compared with other tokenized gold products, SGG has a strong Swiss-law structure and a direct physical redemption path from a single ounce. The main risks are issuer/custody execution, smart-contract/admin functionality, and limited initial liquidity.

The proposed 25% retained reserve addresses ordinary gold-price volatility and liquidation execution risk. The proposed 250,000 ZCHF global minting limit and 2.0% target interest rate are the main safeguards against the wrapper-specific tail risks.

## Free Float

Classification: Sufficient

SGG is freely transferable as an ERC-20 token and has no allowlist, so anyone can hold it and participate in Frankencoin challenges and auctions. SGG can also be physically redeemed from a single ounce through Swissgrams and its first dealer partner, pro aurum, according to the Token Terms.

The current on-chain supply is still small, but SGG has a documented primary-market minting and redemption mechanism. Tokens are released only against matching physical coins deposited into the reserve, and redeemed tokens can be exchanged for whole coins. This creates a credible expansion and exit path, although it depends on Swissgrams, dealer operations, and the availability of eligible coins.

The proposed 250,000 ZCHF global minting limit is reasonable as an initial cap because it limits Frankencoin's exposure while the SGG market develops. At a 3,000 ZCHF liquidation price, the full limit would require roughly 84 SGG of collateral exposure. This is modest in relation to the physical gold market, but should remain linked to the actual circulating SGG supply and available redemption/minting capacity. If supply and liquidity do not expand, the limit should not be increased.

## Public Information

Classification: Strong

Public information is strong because SGG references a highly liquid and observable gold market. The underlying collateral consists of standard 1 oz investment gold coins, and Swissgrams publishes daily inventory reporting for the reserve.

Challengers should therefore be able to estimate likely auction outcomes by referencing the gold price, applying any redemption and liquidity discount, and accounting for the stated redemption process, minting/redemption fees, VAT, shipping, insurance, and timing frictions.

## Market Risk

99%-VaR, 96h close-to-close: 8.46%

Maximum Drawdown, 96h close-to-close: 12.00%

To account for ordinary gold-price volatility over 96h, the 2% challenger reward, and applying an additional haircut for liquidation costs and potential time delays, a 25% minter reserve appears appropriate.

The proposed liquidation price of 3,000 ZCHF per SGG is conservative relative to the current value of one troy ounce of gold and leaves a substantial buffer for liquidation execution.

## Tail Risks

### Counterparty Risk: Swissgrams AG

Likelihood: Medium

Severity: Severe

Compensation: 1.00%

Assessment: SGG is a tokenized wrapper whose value depends on Swissgrams AG as issuer and administrator, Helveticor AG as vaulting provider, the integrity of the reserve, and the redemption process. The co-ownership structure materially reduces issuer insolvency risk, because holders are not merely unsecured creditors of Swissgrams AG. However, operational execution still matters: reserve management, inventory reporting, redemption processing, dealer availability, and custody operations must continue to function as expected.

A failure in any of these components could impair the token relative to the underlying gold price, even if the legal structure is stronger than many issuer-claim models. A 1.00% compensation is therefore assigned for issuer, custody, and redemption dependency.

### Smart Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

Assessment: SGG is an ERC-20 token built on CMTA's audited CMTAT Light framework. The contract is upgradeable through Swissgrams' multisig and includes administrative functionality, including the ability to freeze tokens where sanctions law or a competent authority requires it.

These controls are common for regulated RWA tokens and are not unusual in this category. However, they introduce dependency on correct administration, secure key management, predictable upgrade behaviour, and the absence of contract-level issues. A contract-level exploit, malicious upgrade, compromised admin key, or implementation error could impair transferability, settlement, or liquidation proceeds. A 0.50% compensation is assigned for smart-contract risk.

### Governance Risk: Swiss-law issuer/admin-control risk

Likelihood: Negligible

Compensation: 0.00%

Assessment: SGG is issued by a Swiss company, governed by Swiss law, backed by gold stored in Switzerland, and structured as a co-ownership title in the physical coin reserve. This materially reduces the governance and admin-control risk compared with structures where the issuer, custodian, regulator, and legal claim sit across different jurisdictions.

The contract and Token Terms allow freezing where sanctions law or a competent authority requires it. This is a residual control feature, but it is narrow and embedded in a Swiss legal and operational framework. Given the Swiss issuer, Swiss custody, Swiss-law structure, and co-ownership claim, no separate governance-risk premium is assigned.

### Liquidity Risk: Secondary Market Liquidity & Physical Redemption

Likelihood: Low

Severity: Severe

Compensation: 0.50%

Assessment: SGG is currently an early-stage tokenized gold product with limited secondary-market depth. In a liquidation, challengers may struggle to acquire or recycle sufficient SGG quickly if on-chain liquidity is thin or if primary minting/redemption requires operational coordination.

The exit path is stronger than for many tokenized gold products because SGG can be redeemed from a single ounce. However, physical redemption still involves process risk, timing frictions, minting/redemption fees, VAT where applicable, and third-party costs such as shipping and insurance. Arbitrageurs would therefore likely apply a haircut for delayed exit and redemption uncertainty. A 0.50% compensation is assigned for this risk.

## Conclusion

The proposed retained reserve of 25% is appropriate relative to expected market volatility of the underlying gold exposure and leaves a substantial buffer for liquidation execution. It should not be interpreted as full protection against issuer, custody, redemption, smart-contract, or liquidity tail risks. Those risks are addressed primarily through the proposed 250,000 ZCHF global minting limit and the 2.0% target interest rate.

The target interest rate of 2.0% is justified by the selected risk premia: 1.00% for counterparty risk, 0.50% for smart-contract risk, 0.00% for governance risk, and 0.50% for liquidity risk.

The proposed 250,000 ZCHF global minting limit is the primary safeguard as long as the free float and secondary-market liquidity of SGG remain limited. The Swiss-law structure, Swiss custody, daily inventory reporting, and one-ounce physical redemption path make SGG a credible collateral candidate, provided onboarding starts with a conservative initial limit.
