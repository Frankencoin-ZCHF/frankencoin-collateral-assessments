---
{
  "asset_name": "SPDR S&P 500 ETF (Ondo Tokenized)",
  "asset_ticker": "SPYon",
  "contract_address": "0xFeDC5f4a6c38211c1338aa411018DFAf26612c08",
  "assessment_date": "2026-11-04",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0xFeDC5f4a6c38211c1338aa411018DFAf26612c08",
    "coingecko": "https://www.coingecko.com/en/coins/spdr-s-p-500-etf-ondo-tokenized-etf",
    "website": "https://app.ondo.finance/assets/spyon",
    "docs": "https://docs.ondo.finance/ondo-stocks/overview",
    "other": "https://docs.ondo.finance/ondo-stocks/trust-and-transparency"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Strong",
    "market_risk": "10.49%",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "Ondo Finance",
          "probability": "Very Low",
          "severity": "Severe",
          "compensation": "0.25%"
        }
      ],
      "smart_contract_risks": [
        {
          "name": "Smart-Contract Exploit",
          "probability": "Very Low",
          "severity": "Critical",
          "compensation": "0.50%"
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
    "retained_reserve": 0.15,
    "target_interest_rate": 0.0125,
    "global_minting_limit": "no limit",
    "maturity": "3 years",
    "auction_duration": 24
  }
}
---

# Collateral Risk Assessment: SPDR S&P 500 ETF (Ondo Tokenized)

## Summary

SPYon is Ondo Global Markets' tokenized exposure to the SPDR S&P 500 ETF. It provides ERC-20 exposure to SPY, while the 15% retained reserve provides a reasonable buffer above the 10.49% worst 48-hour close-to-close drawdown observed over the two-year assessment window.

Residual tail risks arise from the issuer and custody structure, the token contract stack, and issuer-controlled compliance and admin functions.

## Asset Overview

SPYon is a structured note issued by Ondo Global Markets (BVI) Limited, rather than direct ownership of SPY shares. Ondo states that corresponding underlying securities and cash in transit are held through one or more US-registered custodial broker-dealers. Ankura Trust Company performs daily holdings attestations and holds a first-priority security interest in the collateral for tokenholders.

The token tracks SPY. Standard platform redemption is into USDon, or into USDC where the USDon/USDC swapper has sufficient liquidity. Redemption into underlying SPY shares is available through Alpaca's Instant Tokenization Network only to enabled authorised participants with linked Ondo and Alpaca accounts.

## Free Float

Classification: Strong

SPY has deep, multi-venue liquidity and an established market. Ondo's issuance and redemption infrastructure connects SPYon economically to that underlying traditional-market liquidity. This does not give every holder direct access to SPY markets: standard redemption is into USDon or USDC, while delivery of SPY shares requires enabled authorised-participant status through Alpaca's Instant Tokenization Network. SPYon is transferable outside the United States subject to jurisdictional and other restrictions. Independent challengers and auction buyers can acquire and sell exposure without relying on a single marketplace, provided they satisfy Ondo's transfer and compliance requirements.

## Public Information

Classification: Strong

SPY has deep, efficient and continuously observable secondary-market pricing. This provides challengers with a reliable basis to estimate expected auction outcomes for SPYon. Ondo's public information on the issuer, collateral, redemption process and token contracts supplements that assessment.

## Market Risk

99%-VaR, 48h close-to-close: 3.38%

Worst 48h close-to-close drawdown observed over the two-year assessment window: 10.49%

A 15% retained reserve provides a reasonable buffer above the observed drawdown and leaves room for the challenger reward.

## Tail Risks

### Counterparty Risk: Ondo Finance

Likelihood: Very Low

Severity: Severe

Compensation: 0.25%

SPYon depends on the issuer's continued performance of its structured-note obligations, custody arrangement and redemption process. Although Ankura verifies collateral daily and holds a security interest for tokenholders, an issuer, custody or redemption disruption could impair the recoverable value of SPYon relative to SPY.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

SPYon is a BeaconProxy using Ondo's upgradeable GMToken implementation. Its transfer hook applies pause and compliance checks to transfers, mints and burns. A technical failure in the token, compliance or pause-manager stack could independently impair balances, transferability or recoverability.

### Governance Risk: Admin-Control

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

Ondo-controlled admin and compliance functions can upgrade the token, pause transfers, and block sanctioned or blocklisted addresses. An assigned burner can burn tokens from an address. The SPYon used as collateral can therefore be frozen, effectively seized or destroyed, which could materially impair Frankencoin’s liquidation mechanism.

## Conclusion

The 15% retained reserve provides a reasonable buffer against the 10.49% worst 48h close-to-close drawdown observed over the two-year assessment window. The 1.25% effective interest rate compensates the assessed tail risks. The framework does not require a cap on the global minting limit based on the tail risk analysis; SPYon's Free Float supports a 24-hour auction duration, subject to buyers satisfying the applicable transfer and compliance requirements, and its established underlying market makes a maturity of 3 years reasonable before the collateral needs to be reassessed.
