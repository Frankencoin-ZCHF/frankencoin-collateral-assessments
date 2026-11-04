---
{
  "asset_name": "Wrapped Staked ETH",
  "asset_ticker": "wstETH",
  "contract_address": "0x7f39c581f595b53c5cb19bd0b3f8da6c935e2ca0",
  "assessment_date": "2026-11-03",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x7f39c581f595b53c5cb19bd0b3f8da6c935e2ca0",
    "coingecko": "https://www.coingecko.com/en/coins/wrapped-steth",
    "website": "https://lido.fi/",
    "docs": "https://docs.lido.fi/contracts/wsteth/",
    "other": "https://stake.lido.fi/wrap"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "16.98%",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "Lido Node Operators",
          "probability": "Very Low",
          "severity": "Severe",
          "compensation": "0.25%"
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
          "name": "Lido DAO",
          "probability": "Negligible",
          "severity": "n/a",
          "compensation": "0%"
        }
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.20,
    "target_interest_rate": 0.005,
    "global_minting_limit": "no limit",
    "maturity": "3 years",
    "auction_duration": 24
  }
}
---

# Collateral Risk Assessment: Wrapped Staked ETH

## Summary

wstETH is Lido's non-rebasing ERC-20 representation of stETH. It provides liquid staked ETH exposure on Ethereum, and the proposed 20% retained reserve provides a reasonable buffer above the 16.98% worst 48-hour close-to-close drawdown observed over the two-year assessment window.

Residual tail risks arise from the Lido validator set and underlying stETH contract stack; the wstETH wrapper itself is simple and non-upgradeable.

## Asset Overview

wstETH wraps stETH, Lido's liquid staking token representing ETH staked through the Lido protocol. Wrapping and unwrapping are permissionless. Unlike rebasing stETH, a holder's wstETH balance remains fixed while its stETH value increases as staking rewards accrue.

The collateral exposure is staked ETH, with additional dependence on Lido's validators and the stETH/wstETH contracts.

## Free Float

Classification: Strong

wstETH has deep secondary-market liquidity and broad integration across centralised and decentralised venues. Independent challengers and auction buyers can acquire and sell the token without relying on a single marketplace.

## Public Information

Classification: Strong

wstETH trades in deep and efficient secondary markets against ETH and stETH. These observable prices give challengers a reliable basis to estimate expected auction outcomes. Lido's contract and staking information supplement this assessment.

## Market Risk

99%-VaR, 48h close-to-close: 13.68%

Worst 48h close-to-close drawdown observed over the two-year assessment window: 16.98%

The 20% retained reserve exceeds the observed drawdown and provides additional room for challenger reward and auction execution.

## Tail Risks

### Counterparty Risk: Lido Node Operators

Likelihood: Very Low

Severity: Severe

Compensation: 0.25%

wstETH ultimately represents ETH delegated through Lido's node-operator set. A material validator failure, slashing event or disruption to validator operations could impair stETH and therefore wstETH relative to ETH.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Severe

Compensation: 0.25%

The wstETH contract provides standard ERC-20, permit, wrap and unwrap functions. Like WETH, it is a simple, non-upgradeable wrapper with no owner, pause, freeze, blacklist, mint, burn or role-management functions; its standalone wrapper risk is negligible. The 0.25% technical premium instead reflects the underlying stETH accounting and withdrawal stack, whose failure could independently impair recoverability.

### Governance Risk: Lido DAO

Likelihood: Negligible

Severity: n/a

Compensation: 0%

Lido DAO governs protocol parameters and node-operator management. The wstETH wrapper itself has no admin-control functions, and no separate governance premium is assigned.

## Conclusion

The 20% retained reserve provides a reasonable buffer against the 16.98% worst 48h close-to-close drawdown observed over the two-year assessment window. The 0.5% effective interest rate compensates the assessed tail risks. The framework does not require a cap on the global minting limit based on the tail risk analysis; wstETH’s high liquidity supports a 24-hour auction duration, and its established market position makes a maturity of 3 years reasonable before the collateral needs to be reassessed.
