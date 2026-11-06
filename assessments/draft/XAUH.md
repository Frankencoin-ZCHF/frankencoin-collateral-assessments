---
{
  "asset_name": "Wrapped Herculis Gold Coin",
  "asset_ticker": "wXAUH",
  "contract_address": "0xC174B12B3195D9887e8dA7aA886EC11c13101060",
  "assessment_date": "2026-11-06",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0xC174B12B3195D9887e8dA7aA886EC11c13101060",
    "coingecko": "",
    "website": "https://xauh.gold/",
    "docs": "https://xauh.gold/whitepaper.pdf",
    "other": "https://github.com/Frankencoin-ZCHF/Frankencoin/discussions/128"
  },
  "risk_scores": {
    "public_information": "Strong",
    "free_float": "Sufficient",
    "market_risk": "12.52%",
    "tail_risks": {
      "counterparty_risks": [{"name": "Herculis Tokens S.A.", "probability": "Medium", "severity": "Severe", "compensation": "1.00%"}],
      "smart_contract_risks": [
        {"name": "XAUH Smart-Contract Exploit", "probability": "Very Low", "severity": "Critical", "compensation": "0.50%"},
        {"name": "wXAUH Smart-Contract Exploit", "probability": "Very Low", "severity": "Critical", "compensation": "0.50%"}
      ],
      "governance_risks": [{"name": "Admin-Control", "probability": "Very Low", "severity": "Critical", "compensation": "0.50%"}]
    }
  },
  "risk_parameters": {"retained_reserve": 0.25, "target_interest_rate": 0.025, "global_minting_limit": 250000, "maturity": "1 year", "auction_duration": 48}
}
---

# Collateral Risk Assessment: Wrapped Herculis Gold Coin

## Summary

wXAUH is a no transfer-fee wrapper of XAUH. Each wXAUH represents one XAUH, and each XAUH represents exposure to one gram of Swiss-stored LBMA 999.9 physical gold. wXAUH was created because XAUH’s fee-on-transfer mechanics are not compatible with the Frankencoin collateral flow.

The underlying exposure is high-quality and relatively low-volatility, but wXAUH remains exposed to issuer, custody, smart-contract and admin-control risk. The 25% retained reserve addresses ordinary gold-price volatility and a potential liquidation discount. The 250,000 ZCHF global minting limit and 2.5% effective interest rate are the main safeguards against these tail risks.

## Asset Overview

wXAUH can be wrapped and unwrapped one-for-one against XAUH. The wrapper does not charge a transfer fee. A 0.02% fee applies when wrapping or unwrapping XAUH, so an auction buyer that unwraps wXAUH receives slightly less than one XAUH per token.

Herculis Tokens S.A., a Panamanian company, is the issuer and primary-market counterparty behind XAUH. It is part of Herculis Group, a Swiss wealth-management and asset-protection boutique established in 2009. The issuer’s terms describe XAUH as a contractual right against Herculis.

The gold is stored in Switzerland and KPMG has verified the gold amount in custody through various reserve reports. The latest report from 28 August 2026 recorded 18 certificates representing 15.5 kg of gold, matching the outstanding token supply.

KYC-verified holders may request physical redemption of underlying XAUH from 500 XAUH. The stated redemption fee is 3% at 500 g and 1% from 1 kg, in addition to delivery, security, insurance, customs and other third-party costs. Redemption may be delayed or refused for compliance, sanctions, legal, logistical or operational reasons.

## Free Float

Classification: Sufficient

wXAUH can be wrapped and unwrapped one-for-one against XAUH. Its relevant liquidity is therefore that of underlying XAUH.

XAUH is listed on Biconomy and BTSE, and Ethereum XAUH has Uniswap liquidity. XAUH on TON has liquidity on Ston.fi and Capital DEX. Changelly, ChangeNOW and Wert provide additional XAUH purchase integrations. A majority of XAUH supply is currently not on Ethereum, and only Herculis can bridge tokens across chains for users. XAUH also has a primary issuance route for KYC-approved customers contributing eligible physical gold or fiat. These routes provide sufficient ways for challengers to acquire XAUH and wrap it into wXAUH.

The current Ethereum market depth and the 500 XAUH physical-redemption process however limit the expected efficiency of an auction. This is addressed by the 25% retained reserve and the 250,000 ZCHF global minting limit.

## Public Information

Classification: Strong

Gold has an observable and liquid underlying market. Herculis publishes token documentation, terms, a white paper and periodic information on the bullion backing. The wXAUH conversion is one-to-one with XAUH. The price source used for the partner venues is Chainlink’s XAU/USD feed converted to a per-gram XAUH price. These inputs allow challengers to estimate a likely auction value by starting from the gold price and applying a discount for redemption delay and costs.

## Market Risk

Worst 48h close-to-close drawdown observed: 12.52%

The 25% retained reserve is above the observed gold-market decline and provides an additional buffer for the challenger reward and the costs of redeeming underlying XAUH.

## Tail Risks

### Counterparty Risk: Herculis Tokens S.A.

Likelihood: Medium

Severity: Severe

Compensation: 1.00%

wXAUH'w value depends on Herculis Tokens S.A. as issuer, the custody of the underlying gold, the redemption process and market confidence. A failure in any of these components could impair wXAUH relative to the underlying gold price.

### Smart-Contract Risk: XAUH Smart-Contract Exploit

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

wXAUH is backed by XAUH. A defect or exploit in the XAUH token accounting or authorisation logic could allow an unauthorised transfer, mint or burn, or prevent the underlying token from settling correctly.

Such a technical failure could impair the value or recoverability of wXAUH even if the wrapper contract itself continues to function.

### Smart-Contract Risk: wXAUH Smart-Contract Exploit

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

wXAUH is a wrapper contract that holds XAUH and issues the corresponding wrapped balance. A defect or exploit in its wrapping, unwrapping, accounting or transfer logic could break the one-to-one relationship with XAUH or prevent collateral from being transferred and auctioned.

The Frankencoin team’s mainnet-fork tests confirmed the intended transfer, approval, position, challenge, bid and forced-sale flows. The residual risk is a failure in the deployed wrapper contract or its integration path.

### Governance Risk: Admin-Control

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

The underlying XAUH token is controlled by a 3-of-4 Safe for token ownership and supply control, while a separate 3-of-4 Safe controls proxy upgrades. The owner Safe can pause transfers, appoint an asset-protection role and replace the supply controller.

An appointed asset-protection role can freeze an address and wipe the balance of a frozen address. The proxy-admin Safe can replace the token logic entirely. These powers can make the XAUH backing held by the wrapper untransferable or destroy it on-chain, impairing wXAUH collateral.

## Conclusion

The 25% retained reserve is appropriate relative to the 12.52% worst 48h close-to-close drawdown observed for the underlying gold market and leaves a substantial buffer for the underlying XAUH execution route, redemption fees and settlement friction. The 2.50% effective interest rate compensates the Herculis Tokens S.A. counterparty risk, XAUH and wXAUH smart-contract risk, and admin-control risk. The 250,000 ZCHF global minting limit restricts the maximum withdrawable amount to 187,500 ZCHF and contains exposure to the issuer, custody and redemption risk. wXAUH’s Sufficient Free Float supports a 48 hour auction duration, and a maturity of 1 year is appropriate before reassessment.
