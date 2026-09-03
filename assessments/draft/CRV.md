---
{
  "asset_name": "Curve DAO Token",
  "asset_ticker": "CRV",
  "contract_address": "0xD533a949740bb3306d119CC777fa900bA034cd52",
  "assessment_date": "2026-08-01",
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
      "counterparty_risks": [
        {
          "name": "Curve ecosystem",
          "probability": "Very Low",
          "severity": "Severe",
          "compensation": "0.25%"
        }
      ],
      "smart_contract_risks": [
        {
          "name": "Curve smart-contract risk",
          "probability": "Low",
          "severity": "Critical",
          "compensation": "1.00%"
        }
      ],
      "governance_risks": [
        {
          "name": "Curve DAO risk",
          "probability": "Very Low",
          "severity": "Severe",
          "compensation": "0.25%"
        }
      ],
      "legal_risks": [
        {
          "name": "n/a",
          "probability": "n/a",
          "severity": "n/a",
          "compensation": "0%"
        }
      ],
      "liquidity_risks": [
        {
          "name": "n/a",
          "probability": "Negligible",
          "severity": "n/a",
          "compensation": "0%"
        }
      ],
      "contagion_risks": [
        {
          "name": "DeFi contagion risk",
          "probability": "Medium",
          "severity": "Severe",
          "compensation": "2.50%"
        }
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.40,
    "target_interest_rate": 0.04,
    "global_minting_limit": 2000000,
    "liquidation_price": null,
    "maturity": null,
    "auction_duration": 24,
    "minimum_collateral": 20000
  }
}
---

# Collateral Risk Assessment: Curve DAO Token

## Summary

Curve DAO Token (CRV) is the governance and incentive token of the Curve Finance ecosystem.

CRV is a higher-risk collateral candidate. The token has strong public information and secondary-market availability, but no hard redemption floor. The main tail risks are Curve protocol risk, key-person and large-holder concentration risk, and DeFi contagion during market stress.

## Introduction

CRV is the native governance token of Curve Finance. It is used in the Curve DAO and veCRV system, where locked CRV influences gauge weights, liquidity incentives, and protocol governance.

The relevant collateral exposure is therefore not a claim on an issuer or a redeemable asset. It is exposure to the market value of a DeFi governance token whose value depends on the functioning of the Curve protocol.

## Free Float/Liquidity

Classification: Strong

CRV is widely traded across centralized exchanges and DeFi venues, and has a long public trading history.

## Public Information

Classification: Strong

Public information is strong, as CRV is traded on secondary markets and liquidation outcomes can be estimated easily.

## Market Risk

MDD 48h: 33.81%

99% VaR (48h): 16.13%

CRV has had relatively high volatility in the past, such that a retained reserve of 40% is necessary to covers the observed 48h drawdown with an additional buffer for the challenger reward.

## Tail Risks

### Counterparty Risk: Curve ecosystem and key-person concentration risk

Description: CRV is not a legal claim on an issuer, custodian, or redemption agent, but it is exposed to Curve ecosystem confidence and key-person or large-holder concentration risk.

Probability: Very Low

Severity: Severe

Compensation: 0.25%

The main concern is not classic issuer counterparty risk. The relevant risk is that large ecosystem figures (for example Michael Egorov) or concentrated holders can create material impact on CRV.

The historic founder borrowing episode, where large CRV holdings were pledged across DeFi lending venues, illustrates how concentrated positions can create forced-liquidation risk, impair market confidence, and amplify downside pressure in CRV.

### Smart Contract Risk: Curve ecosystem

Description: CRV depends on the functioning of the Curve protocol and related token contracts.

Probability: Low

Severity: Critical

Compensation: 1.00%

Curve has a long operating history, but its technical surface is large and systemically relevant across DeFi.

A material exploit, accounting issue, governance-contract failure, or failure in key Curve infrastructure could sharply impair CRV value and liquidity. Given the potential for severe loss of confidence, a 1.00% smart-contract risk premium is appropriate.

### Governance Risk: Curve DAO risk

Description: CRV value depends on Curve DAO governance, veCRV locking, emissions policy, and the incentive structure that supports Curve liquidity.

Probability: Very Low

Severity: Severe

Compensation: 0.25%

CRV's economic value is closely linked to governance utility and emissions control. Stakeholders should generally be aligned with maximizing CRV value, but wrong governance decisions could reduce the token's utility and market value. This risk is distinct from smart-contract failure and supports a separate governance premium.

### Legal Risk: n/a

Description: No separate legal-risk premium is assigned.

Probability: n/a

Severity: n/a

Compensation: 0%

CRV is a decentralized governance token rather than a tokenized security, custodial wrapper, or direct legal claim.

### Liquidity Risk: n/a

Description: No separate liquidity-risk premium is assigned.

Probability: Negligible

Severity: n/a

Compensation: 0%

CRV has strong secondary-market availability, such that it is not necessary to charge an additional premium for liquidity.

### Contagion Risk: DeFi contagion risk

Description: CRV is exposed to broader DeFi stress, lending-market liquidations, stablecoin-pool confidence, and forced selling by leveraged holders.

Probability: Medium

Severity: Severe

Compensation: 2.50%

This is the dominant tail-risk premium for CRV. Curve is deeply connected with other DeFi protocols, and CRV has historically been sensitive to ecosystem confidence and leverage cycles (for example on 10/10/25).

## Conclusion

CRV is an acceptable but higher-risk collateral candidate for Frankencoin.

The proposed retained reserve of 40% is appropriate relative to the observed 33.81% worst 48h close-to-close drawdown. The target interest rate of 4.0% is justified by the selected risk premia: 0.25% for Curve ecosystem and key-person concentration risk, 1.00% for smart-contract and protocol risk, 0.25% for governance and emissions risk, and 2.50% for crypto market & DeFi contagion risk.
