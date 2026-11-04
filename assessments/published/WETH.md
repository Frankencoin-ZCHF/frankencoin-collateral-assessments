---
{
  "asset_name": "Wrapped Ether",
  "asset_ticker": "WETH",
  "contract_address": "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2",
  "assessment_date": "2026-11-03",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
    "coingecko": "https://www.coingecko.com/en/coins/weth",
    "website": "https://weth.io/",
    "docs": "https://github.com/gnosis/canonical-weth/blob/master/contracts/WETH9.sol",
    "other": "https://sourcify.dev/#/lookup/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "17.43%",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "n/a",
          "probability": "n/a",
          "severity": "n/a",
          "compensation": "0%"
        }
      ],
      "smart_contract_risks": [
        {
          "name": "Smart-Contract Exploit",
          "probability": "Negligible",
          "severity": "n/a",
          "compensation": "0%"
        }
      ],
      "governance_risks": [
        {
          "name": "n/a",
          "probability": "n/a",
          "severity": "n/a",
          "compensation": "0%"
        }
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.20,
    "target_interest_rate": 0,
    "global_minting_limit": "no limit",
    "maturity": "3 years",
    "auction_duration": 24
  }
}
---

# Collateral Risk Assessment: Wrapped Ether

## Summary

WETH is the canonical ERC-20 representation of ETH. It provides liquid ETH exposure on Ethereum, and the proposed 20% retained reserve provides a reasonable buffer above the 17.43% worst 48-hour close-to-close drawdown observed over the two-year assessment window.

Residual tail risks are negligible. WETH is a minimal, widely used Ethereum core contract.

## Asset Overview

WETH is a permissionless 1:1 wrapper for native ETH. Users deposit ETH into the WETH contract to receive WETH and can withdraw ETH by returning WETH to the same contract. The collateral exposure is therefore ETH market risk in ERC-20 form, without an external issuer, custodian, bridge operator or redemption agent.

## Free Float

Classification: Strong

WETH has deep secondary-market liquidity and broad integration across centralised and decentralised venues. Independent challengers and auction buyers can acquire and sell the token without relying on a single marketplace.

## Public Information

Classification: Strong

WETH has a long operating history, verified contract code and extensive public market data. Challengers can reasonably assess the token and expected auction outcomes.

## Market Risk

99%-VaR, 48h close-to-close: 13.39%

Worst historical 48h close-to-close drawdown: 17.43%

The metrics use two years of daily close data. A 20% retained reserve exceeds the observed worst 48-hour drawdown and provides additional room for challenger reward and auction execution.

## Tail Risks

### Counterparty Risk: n/a

Likelihood: n/a

Severity: n/a

Compensation: 0%

WETH is not a claim on an issuer, custodian, bridge operator or redemption agent. ETH can be wrapped and unwrapped permissionlessly through the WETH contract.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Negligible

Severity: n/a

Compensation: 0%

The canonical WETH9 contract is a minimal, non-upgradeable contract with deposit, withdraw and standard ERC-20 transfer and approval functions. Deposit and withdrawal provide permissionless 1:1 wrapping and unwrapping; the contract has no privileged mint, burn, pause, freeze, blacklist, role-management or upgrade functions. These properties are expected for a canonical ETH wrapper.

### Governance Risk: n/a

Likelihood: n/a

Severity: n/a

Compensation: 0%

WETH has no owner, admin, pause, blacklist, freeze, seizure, upgrade or discretionary redemption function. There is no governance body with token-level control over holder balances or transfers.

## Conclusion

The 20% retained reserve provides a reasonable buffer against the 17.43% worst 48h close-to-close drawdown observed over the two-year assessment window. No effective interest rate is required because no tail-risk premium is assigned. The framework does not require a cap on the global minting limit based on the tail risk analysis; WETH’s high liquidity supports a 24-hour auction duration, and its established market position makes a maturity of 3 years reasonable before the collateral needs to be reassessed.
