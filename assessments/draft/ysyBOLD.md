---
{
  "asset_name": "Staked yBOLD",
  "asset_ticker": "ysyBOLD",
  "contract_address": "0x23346B04a7f55b8760E5860AA5A77383D63491cD",
  "assessment_date": "2026-11-05",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x23346B04a7f55b8760E5860AA5A77383D63491cD",
    "coingecko": "",
    "website": "https://yearn.fi/vaults/1/0x23346B04a7f55b8760E5860AA5A77383D63491cD",
    "docs": "https://docs.yearn.fi/getting-started/products/yvaults/yBold",
    "other": "https://github.com/yearn/yBOLD"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "4.37%",
    "tail_risks": {
      "counterparty_risks": [
        {"name": "Yearn", "probability": "Low", "severity": "Severe", "compensation": "0.50%"}
      ],
      "smart_contract_risks": [
        {"name": "Liquity V2 / yBOLD", "probability": "Low", "severity": "Critical", "compensation": "1.00%"},
        {"name": "Yearn Vault", "probability": "Very Low", "severity": "Critical", "compensation": "0.50%"}
      ],
      "governance_risks": []
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.10,
    "target_interest_rate": 0.02,
    "global_minting_limit": 1000000,
    "maturity": "2 years",
    "auction_duration": 24
  }
}
---

# Collateral Risk Assessment: Staked yBOLD

## Summary

ysyBOLD is Yearn's auto-compounding vault token for yBOLD. yBOLD allocates BOLD across Liquity V2 Stability Pool strategies, while ysyBOLD holds yBOLD and compounds the resulting rewards through Yearn's tokenised-strategy infrastructure.

The 10% retained reserve provides a reasonable buffer above the 4.37% worst 48-hour close-to-close drawdown observed over the two-year assessment window. The residual risks are Yearn's central strategy controls and the layered Liquity V2, yBOLD and Yearn smart-contract stack that governs the collateral's value and exit path.

## Asset Overview

Staked yBOLD is an ERC-4626-style Yearn TokenizedStrategy vault. It represents a staked position in yBOLD, whose value increases relative to yBOLD as Stability Pool rewards and interest income are harvested and compounded.

yBOLD is a Yearn vault over BOLD and currently allocates across Liquity V2 WETH, rETH and wstETH Stability Pool strategies. The relevant collateral exposure is therefore a layered position consisting of BOLD, Liquity V2 Stability Pool mechanics, yBOLD allocation logic and the ysyBOLD Yearn wrapper.

## Free Float

Classification: Strong

ysyBOLD has a permissionless on-chain exit path. Holders can redeem ysyBOLD for yBOLD through the Yearn vault, and yBOLD can be converted through its BOLD and Liquity strategy path. No centralised issuer, custodian, whitelist or single secondary-market operator is required for this conversion.

Exit value and speed nevertheless depend on the yBOLD/Liquity strategy stack and available BOLD withdrawal liquidity. The 10% retained reserve reflects this layered exit path.

## Public Information

Classification: Strong

yBOLD and ysyBOLD are publicly visible through Yearn's interface and APIs, while the strategy code is public. BOLD also has observable pricing across on-chain markets. These sources give challengers a reliable basis to estimate expected auction outcomes.

## Market Risk

Worst 48h close-to-close drawdown observed over the two-year assessment window: 4.37%

ysyBOLD is a yield-bearing vault share whose value is intended to increase relative to yBOLD as rewards compound. The 10% retained reserve provides a reasonable buffer above the observed drawdown and for the layered exit path.

## Tail Risks

### Counterparty Risk: Yearn

Likelihood: Low

Severity: Severe

Compensation: 0.50%

The current `management` and `emergencyAdmin` roles are held by the Yearn Strategist MultiSig, a 3-of-6 Safe. Management can change the keeper, emergency administrator, pending management, performance-fee terms and strategy health-check configuration. It can also permanently shut the strategy, preventing new deposits and mints.

A compromised or malicious controller could disrupt strategy operations, impede reward harvesting or divert up to 50% of future profits through performance fees. It cannot directly confiscate yBOLD principal, freeze holders, pause transfers, upgrade the strategy at will, or use shutdown to block existing withdrawals or redemptions. This is therefore a centralised operational-control and future-yield risk, rather than a direct collateral-seizure or redemption-blocking risk.

### Smart-Contract Risk: Liquity V2 / yBOLD

Likelihood: Low

Severity: Critical

Compensation: 1.00%

A defect or exploit in Liquity V2 Stability Pool accounting, liquidation-offset mechanics, collateral-reward handling, oracle-dependent auctioning or yBOLD's multi-strategy allocation logic could impair yBOLD's BOLD value or delay conversion into BOLD. This risk passes directly through to ysyBOLD, whose only asset is yBOLD.

### Smart-Contract Risk: Yearn Vault

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

A defect in Yearn's ERC-4626 accounting, share conversion, fee or profit-unlock logic, or ysyBOLD's reward-distribution path could misstate ysyBOLD's claim on yBOLD or impair normal wrapping and redemption. ysyBOLD holds yBOLD directly and receives distributed yBOLD rewards from the yBOLD accountant; it does not deploy yBOLD into a separate yield source.

## Conclusion

The 10% retained reserve provides a reasonable buffer against the 4.37% worst 48h close-to-close drawdown observed over the two-year assessment window. The 2.00% effective interest rate compensates the Yearn Strategist MultiSig control path and the Liquity V2/yBOLD and Yearn wrapper smart-contract risks. The 1,000,000 ZCHF global minting limit restricts the maximum withdrawable amount to 900,000 ZCHF. ysyBOLD's Strong Free Float supports a 24-hour auction duration, and a maturity of 2 years is reasonable before the collateral needs to be reassessed.
