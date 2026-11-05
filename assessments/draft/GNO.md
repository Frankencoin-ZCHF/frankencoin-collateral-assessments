---
{
  "asset_name": "Gnosis",
  "asset_ticker": "GNO",
  "contract_address": "0x6810e776880c02933d47db1b9fc05908e5386b96",
  "assessment_date": "2026-11-05",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x6810e776880c02933d47db1b9fc05908e5386b96",
    "coingecko": "https://www.coingecko.com/en/coins/gnosis",
    "website": "https://www.gnosis.io/",
    "docs": "https://docs.gnosischain.com/",
    "other": "https://forum.gnosis.io/"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "17.94%",
    "tail_risks": {
      "counterparty_risks": [],
      "smart_contract_risks": [],
      "governance_risks": [
        {"name": "GnosisDAO", "probability": "Medium", "severity": "Severe", "compensation": "2.50%"}
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.25,
    "target_interest_rate": 0.025,
    "global_minting_limit": 2000000,
    "maturity": "2 years",
    "auction_duration": 24
  }
}
---

# Collateral Risk Assessment: Gnosis

## Summary

GNO is the native token of the Gnosis ecosystem. It is used in relation to GnosisDAO, Gnosis Chain and the broader Gnosis infrastructure stack.

The 25% retained reserve provides a reasonable buffer above the 17.94% worst 48-hour close-to-close drawdown observed over the two-year assessment window. The main residual risk is GnosisDAO governance and ecosystem dependency: GNO has no standing redemption right, and its value depends on treasury stewardship, execution and continued adoption of the Gnosis ecosystem. A one-time pro-rata treasury redemption was completed in 2026, but it does not create an ongoing guarantee.

## Asset Overview

Gnosis is a long-standing Ethereum ecosystem with a broad infrastructure footprint, including GnosisDAO and Gnosis Chain. GNO holders participate in governance over treasury allocations and protocol changes, and GNO is staked to help secure Gnosis Chain.

GNO is not a redeemable claim on an issuer, custodian, borrower or off-chain asset. GnosisDAO's June 2026 GIP-151 redemption proposal described a treasury of approximately $156.4m and was followed by a one-time pro-rata redemption programme. That historic programme does not give holders an ongoing contractual claim on the treasury.

Its value depends on the relevance, activity, governance, treasury strength and perceived long-term viability of the Gnosis ecosystem.

## Free Float

Classification: Strong

GNO has meaningful circulating supply, a long trading history and secondary-market liquidity across centralised and decentralised venues. Independent challengers and auction buyers can acquire and sell GNO without relying on a single marketplace.

## Public Information

Classification: Strong

GNO has a liquid secondary market and extensive public information on GnosisDAO, Gnosis Chain and the broader ecosystem. This gives challengers a reliable basis to estimate expected auction outcomes.

## Market Risk

99%-VaR, 48h close-to-close: 13.72%

Worst 48h close-to-close drawdown observed over the two-year assessment window: 17.94%

The 25% retained reserve provides a reasonable buffer above the observed drawdown.

## Tail Risks

### Governance Risk: GnosisDAO

Likelihood: Medium

Severity: Severe

Compensation: 2.50%

GNO has no issuer, custody or privileged token-administrator dependency. Its collateral value is nevertheless economically dependent on GnosisDAO governance and the continued health of the Gnosis ecosystem. GNO holders govern treasury allocations and protocol changes, while GNO is used to secure Gnosis Chain.

Adverse governance decisions, weak treasury stewardship, execution failures or deterioration in Gnosis Chain and ecosystem adoption can cause material price and liquidity deterioration. GnosisDAO's treasury is a material source of economic support, but it is governed rather than contractually pledged to GNO holders. Treasury assets can be lost through poor capital allocation, an exploit affecting treasury holdings or external protocol positions, or other operational failures. GNO has no standing redemption floor, so the downside in such a scenario can be materially larger than ordinary market volatility.

The canonical Ethereum GNO token is a fixed, non-proxy ERC-20 with a 10 million token supply created at deployment. It has no owner, upgrade, pause, freeze, blacklist, mint or privileged burn function. No separate token-contract or admin-control premium is assigned.

## Conclusion

The 25% retained reserve provides a reasonable buffer against the 17.94% worst 48h close-to-close drawdown observed over the two-year assessment window. The 2.50% effective interest rate compensates the assessed governance and ecosystem-dependency risk. The framework requires a cap on the global minting limit because this risk is classified as Medium probability; the 2,000,000 ZCHF global minting limit restricts the maximum withdrawable amount to 1,500,000 ZCHF. GNO's Strong Free Float supports a 24-hour auction duration, and a maturity of 2 years is reasonable before the collateral needs to be reassessed.
