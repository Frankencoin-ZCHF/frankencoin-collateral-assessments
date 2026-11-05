---
{
  "asset_name": "Curve DAO Token",
  "asset_ticker": "CRV",
  "contract_address": "0xD533a949740bb3306d119CC777fa900bA034cd52",
  "assessment_date": "2026-11-05",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0xD533a949740bb3306d119CC777fa900bA034cd52",
    "coingecko": "https://www.coingecko.com/en/coins/curve-dao-token",
    "website": "https://curve.fi/",
    "docs": "https://resources.curve.fi/",
    "other": "https://dao.curve.fi/"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "33.81%",
    "tail_risks": {
      "counterparty_risks": [],
      "smart_contract_risks": [
        {"name": "Smart-Contract Exploit", "probability": "Low", "severity": "Critical", "compensation": "1.00%"}
      ],
      "governance_risks": [
        {"name": "Curve DAO", "probability": "Medium", "severity": "Severe", "compensation": "2.50%"}
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.40,
    "target_interest_rate": 0.035,
    "global_minting_limit": 2000000,
    "maturity": "2 years",
    "auction_duration": 24
  }
}
---

# Collateral Risk Assessment: Curve DAO Token

## Summary

CRV is the governance and incentive token of Curve Finance. It has strong public information and broad secondary-market availability, but no redemption floor: its value depends on Curve DAO's governance, the protocol's continued utility and the functioning of the Curve emissions and liquidity-incentive system.

The 40% retained reserve provides a reasonable buffer above the 33.81% worst 48-hour close-to-close drawdown observed over the two-year assessment window. The principal residual risks are Curve DAO's stewardship of CRV's governance and economic system, and an exploit or failure anywhere in Curve's wider smart-contract ecosystem. Such an event could damage protocol activity, liquidity incentives and demand for CRV, even if the CRV token contract itself continued to function.

## Asset Overview

CRV is the native governance token of Curve Finance. It is locked into veCRV for voting power, which directs gauge weights, liquidity incentives and protocol governance. Gauge voting changes emissions allocation on weekly epochs, while the Minter distributes accrued CRV rewards to eligible gauge participants under the token's programmed issuance schedule.

CRV is not a claim on an issuer, custodian or redeemable off-chain asset. Its value depends on the relevance, security and adoption of Curve Finance and on the economic utility of veCRV governance and emissions.

The canonical Ethereum CRV token is a directly deployed Vyper ERC-20, not a proxy. It has no upgrade, pause, blacklist, seizure or privileged burn function. Its `burn` function is self-burn only. The current Curve Ownership Agent is the token's admin; it can change the token's admin and metadata, but cannot pause, upgrade, seize or arbitrarily mint CRV. The designated Curve Minter is fixed and can mint only accrued gauge rewards within the programmed issuance schedule.

## Free Float

Classification: Strong

CRV is widely traded across centralised exchanges and DeFi venues, with a long public trading history. Independent challengers and auction buyers can acquire and sell CRV without relying on a single marketplace.

## Public Information

Classification: Strong

CRV has observable secondary-market pricing and extensive public documentation on Curve governance, gauges and emissions. These efficient, observable prices give challengers a reliable basis to estimate expected auction outcomes.

## Market Risk

99%-VaR, 48h close-to-close: 16.13%

Worst 48h close-to-close drawdown observed over the two-year assessment window: 33.81%

The 40% retained reserve provides a reasonable buffer above the observed drawdown. Historical concentration and leveraged-holder episodes show that CRV can experience rapid price dislocation when large positions are stressed; this is a market-structure consideration rather than a separate named counterparty risk.

## Tail Risks

### Governance Risk: Curve DAO

Likelihood: Medium

Severity: Severe

Compensation: 2.50%

CRV has no issuer redemption promise, custodian or external obligor. Its economic value is nevertheless materially dependent on Curve DAO, acting through veCRV governance and the Curve Ownership Agent. This governance system determines administrative succession and materially influences CRV's emissions allocation, gauge incentives and protocol-economic utility.

Adverse governance decisions, a failure to maintain incentive alignment or deterioration in Curve's protocol relevance can materially impair CRV's value and liquidity. The token admin cannot pause, upgrade, seize, arbitrarily mint or reset the already-fixed Minter; the risk is Curve DAO and protocol-economic dependency, not direct control over pledged token balances.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Low

Severity: Critical

Compensation: 1.00%

Smart-contract risk does not relate only to the CRV token. It covers the entire Curve smart-contract ecosystem, including the contracts that run pools, distribute CRV rewards, govern liquidity incentives and operate the veCRV system. An exploit or failure in any material part of that ecosystem could reduce Curve activity, liquidity and the economic value of CRV, even if the CRV token itself continued to function. The 1.00% compensation covers this wider protocol risk.

## Conclusion

The 40% retained reserve provides a reasonable buffer against the 33.81% worst 48h close-to-close drawdown observed over the two-year assessment window. The 3.50% effective interest rate compensates the assessed Curve DAO and smart-contract tail risks. The 2,000,000 ZCHF global minting limit restricts the maximum withdrawable amount to 1,200,000 ZCHF and limits exposure to Curve-specific governance or technical stress. CRV's Strong Free Float supports a 24-hour auction duration, and a maturity of 2 years is reasonable before the collateral needs to be reassessed.
