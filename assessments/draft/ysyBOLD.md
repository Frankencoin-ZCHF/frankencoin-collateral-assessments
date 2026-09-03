---
{
  "asset_name": "Staked yBOLD",
  "asset_ticker": "ysyBOLD",
  "contract_address": "0x23346B04a7f55b8760E5860AA5A77383D63491cD",
  "assessment_date": "2026-08-01",
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
    "market_risk": "3.69%",
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
          "name": "Liquity V2",
          "probability": "Low",
          "severity": "Critical",
          "compensation": "1.00%"
        },
        {
          "name": "Yearn Vault contracts",
          "probability": "Very Low",
          "severity": "Critical",
          "compensation": "0.50%"
        }
      ],
      "governance_risks": [
        {
          "name": "Yearn governance/admin-control risk",
          "probability": "Low",
          "severity": "Severe",
          "compensation": "0.50%"
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
          "name": "Exit liquidity and unwind risk",
          "probability": "Low",
          "severity": "Severe",
          "compensation": "0.50%"
        }
      ],
      "contagion_risks": [
        {
          "name": "n/a",
          "probability": "Negligible",
          "severity": "n/a",
          "compensation": "0%"
        }
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.10,
    "target_interest_rate": 0.025,
    "global_minting_limit": null,
    "liquidation_price": null,
    "maturity": null,
    "auction_duration": 24,
    "minimum_collateral": 7500
  }
}
---

# Collateral Risk Assessment: Staked yBOLD

## Summary

ysyBOLD is the Yearn auto-compounding vault token for yBOLD. yBOLD tokenizes a BOLD position across Liquity V2 Stability Pools, while ysyBOLD compounds the resulting rewards through Yearn's ERC-4626 vault and strategy infrastructure.

ysyBOLD is an acceptable collateral candidate. The main risks are Liquity/BOLD smart-contract and protocol risk, Yearn vault/strategy smart-contract risk, Yearn governance and admin-control risk, and exit-liquidity risk through the ysyBOLD/yBOLD/BOLD unwind path.

## Introduction

Staked yBOLD (ysyBOLD) is an ERC-4626 Yearn vault token. It represents a staked position in yBOLD, whose value increases relative to yBOLD as Stability Pool rewards and interest income are harvested and compounded.

yBOLD itself represents BOLD deposited across Liquity V2 Stability Pools. The relevant collateral exposure is therefore not a simple stablecoin wrapper. It is a layered position consisting of BOLD, Liquity V2 Stability Pool mechanics, Yearn vault/strategy contracts, and the operational process required to unwind the position.

## Free Float/Liquidity

Classification: Strong

ysyBOLD is live on Ethereum and available through Yearn's interface. The underlying yBOLD exposure is designed to be redeemable for BOLD without a withdrawal fee or waiting period, and ysyBOLD can be redeemed for yBOLD through the Yearn vault mechanics under normal operating conditions.

From a Frankencoin liquidation perspective, the relevant exit path is ysyBOLD into yBOLD, then yBOLD/BOLD or the underlying Liquity Stability Pool position. As long as this redemption path works reliably, liquidity is strong thanks to BOLD's multiple on-chain DEX pools.

## Public Information

Classification: Strong

Public information is strong. The ysyBOLD price is always public as the vault is visible on yearn.fi, and the yBOLD strategy repository is public. The underlying BOLD stablecoin is listed across multiple DEXes.

## Market Risk

MDD 48h / 99%-VaR 48h: <1% for BOLD/USD, 3.69% for USD/CHF

Besides the FX risk between USD/CHF, the 48h market-risk metric is not the most relevant measure for ysyBOLD. The token is a yield-bearing ERC-4626 vault share whose price is expected to grow relative to yBOLD as rewards compound. BOLD has so far been able to maintain its peg to USD very well.

The main collateral risk is therefore not ordinary spot-price volatility, but various tail risk scenarios discussed in the next section.

A retained reserve of 10% is therefore sufficient to cover for expected market volatility of both BOLD and the underlying USD/CHF rate.

## Tail Risks

### Counterparty Risk: n/a

Description: No separate classic counterparty-risk premium is assigned.

Probability: n/a

Severity: n/a

Compensation: 0%

ysyBOLD does not have a direct issuer or custodian, in the same way a centralized BTC, gold, or security-token wrapper would have.

### Smart Contract Risk: Liquity V2

Description: ysyBOLD depends on Liquity V2, BOLD Stability Pools, liquidation mechanics, and indirectly of the soundness of the underlying liquid staking tokens wstETH and rETH.

Probability: Low

Severity: Critical

Compensation: 1.00%

This is the dominant technical risk layer. A severe issue in the BOLD or Liquity V2 Stability Pool stack could impair the underlying asset value, interrupt withdrawals, or create losses in the strategy's position. A 1.00% compensation is appropriate.

### Smart Contract Risk: Yearn vault contracts

Description: ysyBOLD relies on Yearn's ERC-4626 vault infrastructure, tokenized strategy logic, reporting, harvesting, and auto-compounding mechanics.

Probability: Very Low

Severity: Critical

Compensation: 0.50%

Yearn's vault infrastructure is mature, but ysyBOLD still adds a separate wrapper and strategy layer above yBOLD. A contract-level issue could impair wrapping, unwrapping, share-price accounting, or the strategy's ability to manage the underlying position. A 0.50% compensation is therefore appropriate.

### Governance Risk: Yearn governance/admin-control risk

Description: Yearn management or emergency-admin controls can affect the operation of the ysyBOLD wrapper.

Probability: Low

Severity: Severe

Compensation: 0.50%

The Yearn TokenizedStrategy framework includes emergency and management controls. Deposits can be shut down, the strategy can be paused, and emergency withdrawal functions can be used after pause or shutdown. Shutdown primarily blocks new deposits, while a full pause can interrupt user-facing ERC-4626 functions, including deposits, mints, withdrawals, and redeems. This is not classic issuer counterparty risk, but it is a real admin-control and governance dependency for Frankencoin liquidations.

### Legal Risk: n/a

Description: No separate legal-risk premium is assigned.

Probability: n/a

Severity: n/a

Compensation: 0%

No separate legal-risk premium is assigned in the current classification.

### Liquidity Risk: Exit liquidity and unwind risk

Description: Liquidation depends on the practical exit path from ysyBOLD into yBOLD and then into BOLD.

Probability: Low

Severity: Severe

Compensation: 0.50%

Yearn governance actions could become a trigger for exit impairment. The relevant path is ysyBOLD to yBOLD, then yBOLD/BOLD liquidity or unwinding the underlying Stability Pool exposure. A 0.50% premium is appropriate for the current classification.

### Contagion Risk: n/a

Description: No separate contagion-risk premium is assigned.

Probability: Negligible

Severity: n/a

Compensation: 0%

ysyBOLD can be affected by broader stress in DeFi, BOLD liquidity, Liquity V2, or ETH collateral markets, but these risks are already captured through the smart-contract risk and liquidity risk premia.

## Conclusion

ysyBOLD is an acceptable collateral candidate for Frankencoin.

The proposed retained reserve is 10%. The target interest rate is 2.5%, driven by the layered protocol and wrapper risk profile: 1.0% for Liquity/BOLD smart-contract and protocol risk, 0.5% for Yearn smart-contract risk, 0.5% for Yearn governance/admin-control risk, and 0.5% for exit-liquidity risk.
