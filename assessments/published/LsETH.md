---
{
  "asset_name": "Liquid Staked ETH",
  "asset_ticker": "LsETH",
  "contract_address": "0x8c1BEd5b9a0928467c9B1341Da1D7BD5e10b6549",
  "assessment_date": "2026-11-03",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x8c1bed5b9a0928467c9b1341da1d7bd5e10b6549",
    "coingecko": "https://www.coingecko.com/en/coins/liquid-staked-ethereum",
    "website": "https://liquidcollective.io/",
    "docs": "https://docs.liquidcollective.io/v1",
    "other": "https://liquidcollective.io/what-is-lseth/"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Sufficient",
    "market_risk": "16.84%",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "Liquid Collective",
          "probability": "Low",
          "severity": "Severe",
          "compensation": "0.50%"
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
    "retained_reserve": 0.25,
    "target_interest_rate": 0.0125,
    "global_minting_limit": "no limit",
    "maturity": "2 years",
    "auction_duration": 24
  }
}
---

# Collateral Risk Assessment: Liquid Staked ETH

## Summary

LsETH is Liquid Collective's ERC-20 receipt token for staked ETH. It provides liquid staked ETH exposure on Ethereum, and the 25% retained reserve provides a reasonable buffer above the 16.84% worst 48-hour close-to-close drawdown observed over the two-year assessment window.

Residual tail risks arise from Liquid Collective's staking and withdrawal operations, the LsETH contract stack, and protocol admin controls.

## Asset Overview

LsETH represents ETH staked through Liquid Collective. It uses an exchange-rate model under which each token represents an increasing claim on staked ETH as rewards accrue. Liquid Collective is an institutionally oriented liquid staking protocol with a distributed operator set and public documentation. The collateral exposure is staked ETH, with additional dependence on Liquid Collective's validator operations, withdrawal process, contract stack and allowlist/denylist controls.

## Free Float

Classification: Sufficient

LsETH has meaningful circulating supply and observable secondary-market liquidity, but its market depth is materially lower than wstETH's. Access at scale relies more heavily on a limited set of markets and the Liquid Collective redemption route; transfers and redemptions are also subject to protocol allowlist/denylist controls. Large auctions may therefore face greater slippage or withdrawal delays in stressed conditions.

## Public Information

Classification: Strong

LsETH has observable secondary-market prices against ETH, giving challengers a basis to estimate expected auction outcomes. Liquid Collective's contract, validator and staking information supplements this assessment.

## Market Risk

99%-VaR, 48h close-to-close: 13.73%

Worst 48h close-to-close drawdown observed over the two-year assessment window: 16.84%

The 25% retained reserve exceeds the observed drawdown. The additional 5 percentage points above a 20% reserve reflect the Sufficient Free Float classification and the potential for execution slippage or withdrawal delays during stress.

## Tail Risks

### Counterparty Risk: Liquid Collective

Likelihood: Low

Severity: Severe

Compensation: 0.50%

LsETH depends on Liquid Collective's validator operations, withdrawal process and protocol operations. A material operator failure, slashing event or withdrawal disruption could impair LsETH relative to ETH.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Severe

Compensation: 0.25%

LsETH is issued through a TUPProxy pointing to the RiverV1 implementation. The verified, public contract stack supports deposits, redemption requests and claims, validator deposits and exchange-rate accounting. A technical failure in the implementation or its accounting and withdrawal logic could independently impair recoverability.

### Governance Risk: Admin-Control

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

The proxy admin can pause or unpause the system, change the proxy admin and upgrade the implementation. A pause blocks normal proxy calls, including transfers, approvals, deposits and redemption actions. RiverV1's allowlist rejects transfers to or from denied addresses; redemption requires an allowed requester and a non-denied recipient. The admin can replace the allowlist and set daily limits, fees and protocol addresses. A compromised or misused admin path could block transfers or redemptions, or change protocol logic and accounting.

## Conclusion

The 25% retained reserve provides a reasonable buffer against the 16.84% worst 48h close-to-close drawdown observed over the two-year assessment window. The 1.25% effective interest rate compensates the assessed tail risks. The framework does not require a cap on the global minting limit based on the tail risk analysis. This liquidity profile supports a 24-hour auction duration, and a maturity of 2 years is reasonable before the collateral needs to be reassessed.
