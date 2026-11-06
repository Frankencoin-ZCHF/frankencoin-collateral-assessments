---
{
  "asset_name": "Swissgrams Gold",
  "asset_ticker": "SGG",
  "contract_address": "0x2Bd214946806DbEE88Dd3b44b26A21759723d8A2",
  "assessment_date": "2026-11-06",
  "author": "Paolo Di Stefano",
  "links": {"etherscan": "https://etherscan.io/token/0x2Bd214946806DbEE88Dd3b44b26A21759723d8A2", "coingecko": "n/a", "website": "https://swissgrams.com/", "docs": "https://swissgrams.com/token-terms/", "other": "https://swissgrams.com/token-backing/"},
  "risk_scores": {
    "public_information": "Strong", "free_float": "Sufficient", "market_risk": "12.52%",
    "tail_risks": {
      "counterparty_risks": [{"name": "Swissgrams AG", "probability": "Medium", "severity": "Severe", "compensation": "1.00%"}],
      "smart_contract_risks": [{"name": "Smart-Contract Exploit", "probability": "Very Low", "severity": "Critical", "compensation": "0.50%"}],
      "governance_risks": [{"name": "Admin-Control", "probability": "Very Low", "severity": "Critical", "compensation": "0.50%"}]
    }
  },
  "risk_parameters": {"retained_reserve": 0.25, "target_interest_rate": 0.020, "global_minting_limit": 250000, "maturity": "1 year", "auction_duration": 48}
}
---

# Collateral Risk Assessment: Swissgrams Gold

## Summary

SGG is a tokenized gold product issued by Swissgrams AG in Zug, Switzerland. Each SGG represents a proportional co-ownership interest in a reserve of physical sovereign coins stored in Switzerland. Eligible reserve coins include 1 oz American Gold Eagles, Maple Leafs, Vienna Philharmonics, Britannias and Kangaroos. Tokens are released into circulation only against matching coins deposited into the reserve.

The underlying exposure is high-quality and relatively low-volatility. SGG has a strong Swiss-law structure and a direct physical-redemption path from a single ounce. The 25% retained reserve addresses ordinary gold-price volatility and liquidation execution risk. The main residual risks are Swissgrams AG’s custody and redemption operations, a failure of the token’s smart-contract stack, and central administrative controls.

## Asset Overview

SGG is a six-decimal ERC-20 token. Under the Token Terms, each token represents a proportional co-ownership interest in the eligible-coin reserve under Swiss law. The Ethereum token is the register and proof of that co-ownership interest. Holders waive partition and dissolution rights, but retain a redemption claim for their proportional reserve share. The Terms state that holders have a segregation claim in the event of issuer insolvency.

Swissgrams AG is the issuer and contractual custodian. It may appoint and replace Swiss sub-custodians. The white paper identifies Helveticor AG in Zurich as the high-security vaulting and redemption-handling provider.

SGG can be redeemed as whole eligible one-ounce coins. Redemption requires at least 72 hours’ notice, KYC and lawful-acquisition checks. The issuer selects the coin type unless otherwise agreed. The published retail process states a 0.5% redemption fee plus shipping. Swiss redemptions below CHF 20,000 can use the redemption widget with insured Planzer delivery or collection at Pro Aurum in Kilchberg. International and higher-value redemptions require a bespoke offer.

## Free Float

Classification: Sufficient

SGG can be purchased through Mt Pelerin, or minted and redeemed from a single ounce through Swissgrams and its first dealer partner, Pro Aurum.

The on-chain supply is currently still small, but SGG has a documented primary issuance and redemption mechanism. Tokens are released only against matching physical coins deposited into the reserve, and tokens can be redeemed for whole eligible coins. This provides a credible acquisition and exit path, although challengers would primarily depend on Mt Pelerin availability as the primary venue for secondary market liquidity.

The 250,000 ZCHF global minting limit is appropriate while supply and liquidity remain limited.

## Public Information

Classification: Strong

SGG references a highly liquid and observable gold market. The underlying collateral consists of standard one-ounce investment coins, and Swissgrams publishes daily inventory reporting for the reserve.

Challengers can estimate likely auction outcomes from the gold price, applying the 0.5% redemption fee, shipping, insurance, VAT where applicable, and the timing and operational requirements of physical redemption.

## Market Risk

99%-VaR, 96h close-to-close: 8.46%

Worst 48h close-to-close drawdown observed: 12.52%

The 25% retained reserve is above the observed gold-market decline and provides an additional buffer for the challenger reward as well as redemption, delivery and auction execution costs.

## Tail Risks

### Counterparty Risk: Swissgrams AG

Likelihood: Medium

Severity: Severe

Compensation: 1.00%

SGG depends on Swissgrams AG to administer the reserve, custody arrangements, inventory reporting and redemption process. It also depends on Helveticor AG or a replacement Swiss sub-custodian for vaulting and redemption operations. A failure in custody, inventory management, dealer or transport operations or redemption execution could impair the token relative to the underlying gold price.

The co-ownership structure and stated segregation claim materially reduce issuer-insolvency exposure. They do however not remove the operational dependency on Swissgrams AG, its appointed sub-custodian and the physical redemption process.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

SGG is an ERC-20 token implemented through an EIP-1967 TransparentUpgradeableProxy and the CMTATUpgradeableLight implementation. A technical defect, exploit, proxy or storage failure could impair balances, transfers, minting, burning or the token record used to evidence the associated co-ownership interest.

### Governance Risk: Admin-Control

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

A Safe controlled through Swissgrams’ multisignature governance process holds the default-admin role and controls the ProxyAdmin. It can mint and burn, pause transfers, freeze addresses, grant and revoke roles, deactivate the contract and replace the proxy implementation.

A frozen address cannot transfer SGG. The default admin can then force-burn the frozen balance. The ProxyAdmin can also replace the token logic through an upgrade. The Token Terms describe freezing as a sanctions or competent-authority measure and state that the issuer otherwise has no confiscation or appropriation right. The on-chain controls can nevertheless make pledged SGG untransferable or destroy its on-chain balance.

## Conclusion

The 25% retained reserve is above the 12.52% worst 48h close-to-close drawdown observed for the underlying gold market. It also provides a buffer for the 0.5% redemption fee, delivery, insurance and auction execution costs. The 2.00% effective interest rate compensates Swissgrams AG counterparty risk, smart-contract exploit risk and admin-control risk. The 250,000 ZCHF global minting limit restricts the maximum withdrawable amount to 187,500 ZCHF and contains exposure to the Medium counterparty risk. SGG’s Sufficient Free Float supports a 48 hour auction duration, and a maturity of 1 year is appropriate before reassessment.
