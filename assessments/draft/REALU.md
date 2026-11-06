---
{
  "asset_name": "RealUnit Schweiz AG", "asset_ticker": "REALU", "contract_address": "0x553C7f9C780316FC1D34b8e14ac2465Ab22a090B", "assessment_date": "2026-11-06", "author": "Paolo Di Stefano",
  "links": {"etherscan":"https://etherscan.io/token/0x553C7f9C780316FC1D34b8e14ac2465Ab22a090B","coingecko":"","website":"https://realunit.ch/loesung/aktie-und-finanzdaten/","docs":"https://realunit.ch/loesung/aktientoken/","other":"https://realunit.ch/wp-content/uploads/dlm_uploads/2026/03/Geschaeftsbericht-RealUnit-2025_compressed.pdf"},
  "risk_scores": {"public_information":"Sufficient","free_float":"Sufficient","market_risk":"11.56%","tail_risks":{"counterparty_risks":[{"name":"RealUnit Schweiz AG","probability":"Medium","severity":"Severe","compensation":"1.50%"}],"smart_contract_risks":[{"name":"Smart-Contract Exploit","probability":"Very Low","severity":"Critical","compensation":"0.50%"}],"governance_risks":[{"name":"Admin-Control","probability":"Very Low","severity":"Critical","compensation":"0.50%"}]}},
  "risk_parameters":{"retained_reserve":0.20,"target_interest_rate":0.025,"global_minting_limit":5000000,"maturity":"2 years","auction_duration":72}
}
---

# Collateral Risk Assessment: RealUnit Schweiz AG

## Summary

REALU is the tokenized Series-B registered share of RealUnit Schweiz AG, a Swiss investment company. It is assessed primarily against reported net asset value rather than operating-company earnings multiples. The 20% retained reserve is above the 11.56% largest price decline observed over 72 hours in the listed Series A bearer shares.

The main residual risks are RealUnit’s integrity, portfolio valuation and custody, the tokenized-share smart-contract stack, and central admin control over token terms, transfer restrictions and invalidation.
 
## Asset Overview

RealUnit Schweiz AG is a Swiss investment company founded in 2017 and domiciled in Baar. Its stated strategy is real capital preservation through physical precious metals, Swiss and international equities, cash, nominal assets, alternative investments and a small crypto allocation.

At 31 December 2025, RealUnit reported total assets of CHF 53.9m, total liabilities of CHF 1.3m and total equity of CHF 52.6m. It reported 39,093,976 shares outstanding and a NAV of CHF 1.35 per share. The portfolio allocation was 46.9% physical precious metals, 32.4% equities, 8.5% physical CHF cash, 5.2% nominal assets, 3.9% alternative investments and 3.2% crypto assets. RealUnit classified 87% of the portfolio as very liquid, 7% as liquid and 6% as illiquid.

The 2025 structure comprised listed Series-A bearer shares and tokenized Series-B registered shares. Following the September 2026 capital increase, RealUnit reported 44,462,121 listed Series-A bearer shares and 7,000,000 unlisted Series-B registered shares. REALU represents the unlisted Series-B registered share class, which has a different transfer and settlement path from the listed Series-A shares.

RealUnit publishes an indicative NAV. The figure is useful as a valuation reference, but the issuer notes that it may differ from actual value because of valuation assumptions, stale pricing of illiquid investments or technical-feed errors. The officially prepared financial reports remain the principal valuation reference.

## Free Float

Classification: Sufficient

REALU can be transferred and traded through RealUnit’s issuer-operated token market and Brokerbot infrastructure. These are secondary-market channels, not a contractual issuer redemption at NAV.

The BX Swiss listing does not provide a direct exit route for REALU because it applies to the separate Series-A bearer-share class. Conversion into another legal share form requires a shareholder request and board approval; it is not an assured or immediate auction exit.

The tokenized share float and buyer universe remain limited, and liquidation depends on buyers willing to acquire the unlisted Series-B shares in token form. The Free Float classification is therefore Sufficient.

## Public Information

Classification: Sufficient

RealUnit publishes annual reports, ongoing NAV information, shareholder and corporate-governance disclosures, tokenized-share documentation and information about the listed Series-A bearer shares. This supports a transparent NAV-based assessment of the underlying portfolio.

The tokenized Series-B shares lack a deep, continuously observable market price. The listed Series-A market and published NAV provide reference points for estimating auction outcomes, but do not establish direct executable depth for REALU.

## Market Risk

99%-VaR, 72h close-to-close: 7.64%

Worst 72h close-to-close drawdown observed from 18 August 2025 to 5 November 2026: 11.56%

The listed Series A bearer shares show the 11.56% largest price decline over 72 hours. These figures do not represent direct trading conditions for the tokenized Series B shares. The 20% retained reserve remains above this decline and provides an additional buffer for the distinct execution risk of the tokenized shares.

## Tail Risks

### Counterparty Risk: RealUnit Schweiz AG

Likelihood: Medium

Severity: Severe

Compensation: 1.50%

RealUnit manages the investment portfolio, including portfolio valuation, custody and realisation of physical precious metals, cash and crypto assets. Mismanagement, fraud, a material valuation restatement or impaired asset realisation could reduce NAV materially.

RealUnit also operates the off-chain share register and the Brokerbot-based token-market route. Only registered shareholders can exercise voting and dividend rights. The issuer can refuse or remove registration in specified false or incomplete-information circumstances.

The populated owner role can mint within the declared share ceiling, alter that ceiling, change token terms and recovery collateral, reactivate transfer restrictions, assign address types and declare tokens invalid. Declaring tokens invalid does not technically freeze or transfer them, but can detach them from the underlying shareholder rights.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

REALU is a tokenized registered share using a bespoke smart-contract stack, including the REALU token, RecoveryHub and related settlement infrastructure.

A smart-contract failure or exploit could make the token inaccessible, cause an incorrect transfer or disrupt settlement. In that case, Frankencoin could be unable to move or liquidate pledged REALU even if the underlying RealUnit shares remain economically intact.

### Governance Risk: Admin-Control

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

The REALU owner can declare tokens invalid. Invalidating a token does not technically freeze, burn or transfer it, but it detaches the affected amount from the underlying shareholder rights.

This power is relevant where tokens are treated as lost or stolen and the issuer follows the applicable recovery or legal process. If REALU pledged to Frankencoin were declared invalid, the position could still hold tokens on-chain but no longer hold the corresponding RealUnit shares.

## Conclusion

The 20% retained reserve is above the 11.56% largest price decline observed over 72 hours in the listed Series A bearer shares. It also provides a buffer for the execution risk of the tokenized Series B shares. The 2.50% effective interest rate compensates RealUnit Schweiz AG counterparty risk, tokenized share smart contract risk and admin control risk. The 2,500,000 ZCHF global minting limit restricts the maximum withdrawable amount to 2,000,000 ZCHF and contains exposure to the Medium / Severe RealUnit Schweiz AG counterparty risk. REALU’s Sufficient Free Float supports a 72 hour auction duration, and a maturity of 2 years is appropriate before reassessment.
