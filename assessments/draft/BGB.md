---
{
  "asset_name": "Bitget Token",
  "asset_ticker": "BGB",
  "contract_address": "0x54D2252757e1672EEaD234D27B1270728fF90581",
  "assessment_date": "2026-11-05",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x54D2252757e1672EEaD234D27B1270728fF90581",
    "coingecko": "https://www.coingecko.com/en/coins/bitget-token",
    "website": "https://www.bitget.com/",
    "docs": "https://www.morphl2.io/",
    "other": "https://github.com/Frankencoin-ZCHF/Frankencoin/discussions/112"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "22.28%",
    "tail_risks": {
      "counterparty_risks": [
        {"name": "Bitget", "probability": "Medium", "severity": "Critical", "compensation": "5.00%"}
      ],
      "smart_contract_risks": [],
      "governance_risks": []
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.40,
    "target_interest_rate": 0.05,
    "global_minting_limit": 2000000,
    "maturity": "2 years",
    "auction_duration": 24
  }
}
---

# Collateral Risk Assessment: Bitget Token

## Summary

BGB is Bitget's exchange-utility token and, since the 2025 Bitget–Morph partnership, the gas and governance token of Morph. It has strong public information and broad secondary-market availability, but its value remains materially dependent on Bitget's exchange franchise and the Morph Foundation's execution of BGB's ecosystem roadmap.

The 40% retained reserve provides a reasonable buffer above the 22.28% worst 48-hour close-to-close drawdown observed over the two-year assessment window. The main residual risk is one correlated Bitget / Morph Foundation exposure: an adverse event affecting either the exchange or Morph-side adoption can impair BGB utility, market confidence and liquidation conditions at the same time.

## Asset Overview

BGB is used across Bitget for fee discounts, VIP benefits, Launchpool and wallet-gas programmes. Bitget and Morph announced an exclusive strategic partnership in September 2025. Bitget transferred the 440 million BGB controlled by the Bitget team to the Morph Foundation: 220 million were designated for burn and the remaining 220 million were locked for gradual release at 2% per month for Morph liquidity incentives, ecosystem expansion, education and awareness.

Bitget states that the Morph Foundation is responsible for BGB's future development roadmap. BGB is therefore not a neutral cryptoasset or a redeemable claim on either Bitget or the Morph Foundation; its value depends on exchange utility, Morph adoption, distribution policy and continued market confidence.

The canonical Ethereum BGB token is a direct ERC-20 implementation with a 2 billion BGB total supply. It has no owner, upgrade, mint, contract-level burn, pause, freeze, blacklist, seizure or transfer-restriction function. BGB burns described in Bitget materials are holder-controlled transfers to a burn address, not a privileged burn authority in this token contract.

## Free Float

Classification: Strong

BGB has a meaningful market capitalisation, a multi-year trading history and secondary-market availability across Bitget and other centralised venues, including Kraken, MEXC and Bitfinex. Independent challengers and auction buyers can acquire and sell BGB without relying on a single marketplace.

Trading is nevertheless concentrated on Bitget and on-chain liquidity is materially smaller. This concentration is reflected in the 40% retained reserve and the 2,000,000 ZCHF global minting limit.

## Public Information

Classification: Strong

BGB has public exchange pricing, a multi-year trading history, public token information and public documentation from Bitget and Morph. These observable prices give challengers a reliable basis to estimate expected auction outcomes. Bitget's published proof-of-reserve information provides supplementary transparency on the exchange, but does not remove sponsor, operational or solvency risk.

## Market Risk

99%-VaR, 48h close-to-close: 13.27%

Worst 48h close-to-close drawdown observed over the two-year assessment window: 22.28%

The 40% retained reserve provides a reasonable buffer above the observed drawdown and for execution under concentrated venue conditions.

## Tail Risks

### Counterparty Risk: Bitget

Likelihood: Medium

Severity: Critical

Compensation: 5.00%

BGB is not a redeemable claim on Bitget or the Morph Foundation, and the Ethereum token contract has no issuer-admin, mint, pause, freeze, blacklist or upgrade authority. Its value nevertheless remains materially dependent on Bitget's continued operation and BGB utility policies, and on the Morph Foundation's BGB roadmap, gas and governance adoption, and management of the transferred team allocation.

A severe Bitget solvency, security, regulatory or trading-disruption event, or a failure of Morph-side adoption and token-distribution policy, could simultaneously impair BGB utility, market confidence and liquidation conditions. This is one correlated ecosystem-sponsor exposure and is not split into separate smart-contract, liquidity or governance premia.

## Conclusion

The 40% retained reserve provides a reasonable buffer against the 22.28% worst 48h close-to-close drawdown observed over the two-year assessment window. The 5.00% effective interest rate compensates the assessed Bitget / Morph Foundation tail risk. The 2,000,000 ZCHF global minting limit restricts the maximum withdrawable amount to 1,200,000 ZCHF and limits exposure to an extreme ecosystem-sponsor event. BGB's Strong Free Float supports a 24-hour auction duration, and a maturity of 2 years is reasonable before the collateral needs to be reassessed.
