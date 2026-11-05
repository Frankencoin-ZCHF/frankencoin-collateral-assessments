---
{
  "asset_name": "Pax Gold",
  "asset_ticker": "PAXG",
  "contract_address": "0x45804880De22913dAFE09f4980848ECE6EcbAf78",
  "assessment_date": "2026-11-05",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x45804880de22913dafe09f4980848ece6ecbaf78",
    "coingecko": "https://www.coingecko.com/en/coins/pax-gold",
    "website": "https://www.paxos.com/paxgold/",
    "docs": "https://github.com/paxosglobal/paxos-gold-contract",
    "other": "https://www.paxos.com/terms-and-conditions/pax-gold-terms-conditions"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "11.58%",
    "tail_risks": {
      "counterparty_risks": [
        {"name": "Paxos", "probability": "Very Low", "severity": "Severe", "compensation": "0.25%"}
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

# Collateral Risk Assessment: Pax Gold

## Summary

PAXG is Paxos's tokenized gold product. Each token represents exposure to one fine troy ounce of allocated physical gold.

The 15% retained reserve provides a reasonable buffer above the 11.58% worst 48-hour close-to-close drawdown observed over the two-year assessment window. The main residual risks are Paxos's issuer and custody chain, the upgradeable token and supply-control stack, and Paxos-controlled powers to pause, freeze, wipe and alter token logic.

## Asset Overview

PAXG is issued by Paxos Trust Company, NA. Paxos states that each token represents one fine troy ounce of London Good Delivery gold held on a segregated basis in LBMA-accredited London vaults for PAXG holders. Paxos publishes monthly reserve-composition and third-party attestation reports.

Primary-market redemption requires a Paxos account and a conversion or redemption request. Conversion to unallocated Loco London gold is available through Paxos; delivery of allocated physical bars requires at least 430 PAXG plus applicable fees, may require further due diligence and may take several business days.

## Free Float

Classification: Strong

PAXG has meaningful circulating supply, a long operating history and secondary-market liquidity across centralised and decentralised venues.

Independent challengers and auction buyers can acquire and sell PAXG without relying on a single marketplace.

## Public Information

Classification: Strong

PAXG has observable secondary-market pricing and a transparent gold-price reference, giving challengers a reliable basis to estimate expected auction outcomes. The underlying gold market is one of the deepest global commodity markets, supporting price discovery and valuation. Paxos's public reserve, attestation and token-contract information supplements that assessment.

## Market Risk

99%-VaR, 48h close-to-close: 5.08%

Worst 48h close-to-close drawdown observed over the two-year assessment window: 11.58%

The 15% retained reserve provides a reasonable buffer above the observed drawdown.

## Tail Risks

### Counterparty Risk: Paxos

Likelihood: Very Low

Severity: Severe

Compensation: 0.25%

PAXG depends on Paxos, its gold custody and reserve administration, and the contractual redemption process. A failure, insolvency, operational disruption or legal restriction affecting Paxos, the custodian or the redemption process could impair reserve access, redemption or liquidation recovery.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

PAXG is an upgradeable ZeppelinOS proxy using a PAXG V2 implementation and a separate SupplyControl contract. The technical exposure includes the proxy, implementation, SupplyControl contract and their privileged integration. A technical failure in this stack could independently impair transfers, balances or collateral recovery.

### Governance Risk: Admin-Control

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

PAXG exposes separate pause and asset-protection roles. A pause blocks transfers, `transferFrom` and approvals. An asset-protection role can freeze or unfreeze an address; a frozen address cannot use the ordinary transfer or approval paths. `wipeFrozenAddress` can then burn the entire balance of a frozen address, reducing total supply.

SupplyControl centrally governs minting and burning through configured supply controllers. The token's default admin can replace SupplyControl, while the proxy admin can replace the token implementation. A correctly exercised compliance action can therefore make pledged PAXG unavailable for liquidation or permanently burn it, while an upgrade can change the applicable control surface.

## Conclusion

The 15% retained reserve provides a reasonable buffer against the 11.58% worst 48h close-to-close drawdown observed over the two-year assessment window. The 1.25% effective interest rate compensates the assessed tail risks. The framework does not require a cap on the global minting limit based on the tail risk analysis; PAXG's Strong Free Float supports a 24-hour auction duration, and its established market position makes a maturity of 3 years reasonable before the collateral needs to be reassessed.
