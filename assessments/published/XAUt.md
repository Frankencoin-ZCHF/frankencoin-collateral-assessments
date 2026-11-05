---
{
  "asset_name": "Tether Gold",
  "asset_ticker": "XAUt",
  "contract_address": "0x68749665FF8D2d112Fa859AA293F07A622782F38",
  "assessment_date": "2026-11-05",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x68749665ff8d2d112fa859aa293f07a622782f38",
    "coingecko": "https://www.coingecko.com/en/coins/tether-gold",
    "website": "https://gold.tether.to/",
    "docs": "https://gold.tether.to/",
    "other": "https://tether.to/en/transparency/"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "11.66%",
    "tail_risks": {
      "counterparty_risks": [
        {"name": "Tether", "probability": "Very Low", "severity": "Severe", "compensation": "0.25%"}
      ],
      "smart_contract_risks": [
        {"name": "Smart-Contract Exploit", "probability": "Very Low", "severity": "Critical", "compensation": "0.50%"}
      ],
      "governance_risks": [
        {"name": "Admin-Control", "probability": "Very Low", "severity": "Critical", "compensation": "0.50%"}
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.15,
    "target_interest_rate": 0.0125,
    "global_minting_limit": "no limit",
    "maturity": "3 years",
    "auction_duration": 24
  }
}
---

# Collateral Risk Assessment: Tether Gold

## Summary

XAUt is Tether Gold's tokenized gold product. TG Commodities, S.A. de C.V., a Tether Gold entity, issues and redeems the token. Each token represents exposure to one fine troy ounce of allocated physical gold.

The 15% retained reserve provides a reasonable buffer above the 11.66% worst 48-hour close-to-close drawdown observed over the two-year assessment window. The main residual risks are Tether Gold's issuer and custody chain, the upgradeable token contract stack, and Tether-controlled powers to block, burn and alter token logic.

## Asset Overview

TG Commodities, S.A. de C.V. is the issuer and customer-facing entity for XAUt issuance and redemption. Alpha Group Commodities Limited S.A. de C.V. (AGCL), a wholly owned Tether Holdings subsidiary, purchases the gold and supplies XAUt inventory after the gold is deposited with the custodian.

The gold reserves are held in Switzerland by an unnamed Swiss custodian related to Tether Gold but stated to operate separately from the Tether Group. TG Commodities states that it does not hold legal title to the reserves and that the custodian holds them on behalf of XAUt holders.

Primary-market redemption is contractual and KYC-gated. It is limited to full bars in Switzerland, or a requested attempted Swiss-market sale of a bar; Tether Gold and its affiliates have no standing obligation to repurchase XAUt or gold bars.

## Free Float

Classification: Strong

XAUt has meaningful circulating supply, a long operating history and secondary-market liquidity across centralised and decentralised venues.

Independent challengers and auction buyers can acquire and sell XAUt without relying on a single marketplace. The direct physical-redemption route is restricted to eligible primary-market customers and full bars, but does not prevent secondary-market liquidation.

## Public Information

Classification: Strong

XAUt has observable secondary-market pricing and a transparent gold-price reference, giving challengers a reliable basis to estimate expected auction outcomes. The underlying gold market is one of the deepest global commodity markets, supporting price discovery and valuation. Tether Gold's public reserve, custody and token-contract information supplements that assessment.

## Market Risk

99%-VaR, 48h close-to-close: 4.72%

Worst 48h close-to-close drawdown observed over the two-year assessment window: 11.66%

The 15% retained reserve provides a reasonable buffer above the observed drawdown.

## Tail Risks

### Counterparty Risk: Tether

Likelihood: Very Low

Severity: Severe

Compensation: 0.25%

XAUt depends on Tether's subsidiary, the unnamed Swiss custodian and the contractual redemption process. A failure, insolvency, operational disruption or legal restriction affecting the issuer, gold-sourcing entity, custodian or redemption process could impair reserve access, redemption or liquidation recovery.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

XAUt is an ERC-20 implementation behind a TransparentUpgradeableProxy. The current implementation uses upgradeable ERC-20, permit and ownership components together with a blocked-list module. It has no current pause function. A technical failure in the proxy, implementation, ownership controls or blocked-list logic could impair transfers, balances or collateral recovery.

### Governance Risk: Admin-Control

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

The live token owner and the owner of the ProxyAdmin are the same 3-of-6 multisig. The token owner can block or unblock any address, preventing a blocked address from moving its balance. After blocking an address, the owner can permanently burn its entire XAUt balance through `destroyBlockedFunds`. The owner can also mint XAUt without a code-level supply cap.

The ProxyAdmin owner can replace the token implementation through `upgrade` or `upgradeAndCall`, changing the token's transfer, supply, blocklist or redemption logic. A correctly exercised compliance action can therefore make pledged XAUt unavailable for liquidation; the collateral can also be destroyed after it is blocked.

## Conclusion

The 15% retained reserve provides a reasonable buffer against the 11.66% worst 48h close-to-close drawdown observed over the two-year assessment window. The 1.25% effective interest rate compensates the assessed tail risks. The framework does not require a cap on the global minting limit based on the tail risk analysis; XAUt's Strong Free Float supports a 24-hour auction duration, and its established market position makes a maturity of 3 years reasonable before the collateral needs to be reassessed.
