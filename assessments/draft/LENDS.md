---
{
  "asset_name": "Switzerlend AG C1 Shares",
  "asset_ticker": "LENDS",
  "contract_address": "0x343324f53cbeee3ee6d171f2a20f005964c98047",
  "assessment_date": "2026-08-01",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x343324f53cbeee3ee6d171f2a20f005964c98047",
    "coingecko": "",
    "website": "https://shares.lend.ch",
    "docs": "https://docs.aktionariat.com/en",
    "other": "https://lend.ch/en/investor-relations"
  },
  "risk_scores": {
    "public_information": "Sufficient",
    "free_float": "Sufficient",
    "market_risk": "n/a",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "Switzerlend AG",
          "probability": "Medium",
          "severity": "Critical",
          "compensation": "3.00%"
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
          "name": "n/a",
          "probability": "Negligible",
          "severity": "n/a",
          "compensation": "0%"
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
          "name": "Secondary Market Liquidity",
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
    "retained_reserve": 0.40,
    "target_interest_rate": 0.04,
    "global_minting_limit": 500000,
    "liquidation_price": 20.00,
    "maturity": null,
    "auction_duration": 72,
    "minimum_collateral": 500
  }
}
---

# Collateral Risk Assessment: Switzerlend AG C1 Shares

## Summary

LENDS is the tokenized equity token of Switzerlend AG, the Swiss company operating LEND.ch. The token represents registered shares of Switzerlend AG under Swiss law and is issued using Aktionariat AG’s tokenization infrastructure. It represents private-company equity exposure rather than a liquid crypto asset or listed security.

LENDS is a complex collateral because there is no continuously observable public-market price that can be used as a reliable liquidation reference. The relevant collateral value must therefore be derived from company valuation and warrants conservative buffers.

For collateral purposes, a reasonable base-case valuation range is CHF 12 million–18 million. Based on 712,028 total shares outstanding, this corresponds to a stock price of approximately CHF 16.85–25.28 per share.

The 4.00% target interest rate reflects the counterparty, liquidity, and residual smart-contract risk, while the 1,000,000 ZCHF global minting limit keeps the exposure contained. The position should be reassessed as updated financial statements become available.

## Introduction

Switzerlend AG operates LEND.ch, a Swiss crowdlending platform active across personal loans, SME loans, and mortgages.

The latest available figures show positive operating momentum, with H1 2026 revenue of CHF 2.85 million and H1 2026 EBITDA of CHF 583,000. Annualised, this corresponds to approximately CHF 5.7 million of revenue and CHF 1.17 million of EBITDA.

For collateral purposes, a reasonable base-case valuation range is CHF 12 million–18 million, based on a 10-15x EBITDA multiple and a 2.5-3.5x revenue-multiple. Based on 712,028 total shares outstanding, this corresponds to a stock price of approximately CHF 16.85–25.28 per share.

A liquidation price of CHF 20.00 per share is therefore supported by the company’s current revenue and EBITDA profile.

With a 40% retained reserve, the Frankencoin system would only incur a loss if the shares are sold below CHF 12.00 per share.

Given the company’s current operating performance and the valuation support from both EBITDA and revenue multiples, this should be a reasonable floor price potential auction bidders should be open to paying in a liquidation scenario.

## Free Float/Liquidity

Classification: Sufficient

LENDS has a tokenized shareholder base and is issued using Aktionariat technology, with a small internally operated secondary marketplace available for identified users.

The investor page reports 27,277 tokenized LENDS and 284 shareholders. The token is therefore not purely privately held, and there is at least some existing shareholder and trading infrastructure.

However, LENDS remains private-company equity. Liquidity is structurally weaker than for listed equities and major crypto assets. Even if the token is technically transferable, liquidation depends on the availability of buyers for Switzerlend AG equity at the relevant time.

The secondary market is not a supervised trading venue and may not provide sufficient liquidity in a stressed liquidation scenario. The free-float classification is therefore sufficient, not strong.

## Public Information

Classification: Sufficient

Public information is not high, but sufficient. The LEND.ch investor-relations page provides company information, platform metrics, loan-book data, and explanations of the tokenized-share structure.

Public information is however materially weaker than for a listed company. There is no regulated public-market disclosure regime, no liquid exchange order book, and no continuously reliable trading price. Potential challengers must therefore estimate auction outcomes using fundamental data, which makes a projected auction outcome inherently less certain.

## Market Risk

99%-VaR, 48h close-to-close: n/a

Maximum Drawdown, 48h close-to-close: n/a

There is no reliable continuous secondary-market price series for LENDS.

## Tail Risks

### Counterparty Risk: Switzerlend AG

Description: LENDS represents exposure to Switzerlend AG, a private Swiss lending-platform company with operating, credit-cycle, funding, regulatory, and execution risk.

Probability: Medium

Severity: Critical

Compensation: 3.00%

This is the dominant tail risk. LENDS is the equity of a private operating company. If the company fails, the token could potentially become worthless.

The company has meaningful operating traction, with more than CHF 600 million of cumulative financing volume, an outstanding loan book of approximately CHF 166.4 million, and positive H1 2026 EBITDA. The reported loan-book metrics also indicate acceptable credit performance and diversification.

However, the company remains exposed to the Swiss credit cycle, borrower defaults, origination volumes, platform reputation, funding-market conditions, regulation, and competition from banks and other credit platforms. The valuation is also highly sensitive to whether the latest H1 2026 EBITDA level can be sustained and expanded.

A 3.00% compensation is assigned for this counterparty risk.

Global Minting Limit: 500,000 ZCHF

Since this risk is classified as Medium probability, it triggers a global minting limit requirement based on the framework. The exposure should remain significantly below what the equity pool could theoretically absorb. With a retained reserve of 40%, the 1,000,000 ZCHF global minting limit implies a maximum withdrawable amount of 600,000 ZCHF.

Since only the share class C1 is tokenised, the value of all tokenised shares may only reach 621,320 ZCHF at a liquidation price of 20.00 CHF per share. Therefore, a global minting limit of 500,000 ZCHF is necessary to ensure there is some available free float beyond what can be locked as collateral.

### Smart Contract Risk: Smart-Contract Exploit

Description: LENDS is implemented as a tokenized equity instrument using Aktionariat AG technology and therefore carries residual smart-contract and token-infrastructure risk.

Probability: Very Low

Severity: Critical

Compensation: 0.50%

LENDS uses Aktionariat’s tokenized-share infrastructure. The token represents ledger-based securities under Swiss law and is not a vanilla ERC-20 issued solely for DeFi use.

Residual smart-contract risk remains because the token infrastructure is relatively complex.

The probability for a significant exploit appears very low, but the severity could be critical; a 0.50% compensation is therefore assigned.

### Governance Risk: n/a

Description: No separate governance-risk premium is assigned in the current classification.

Probability: Negligible

Severity: n/a

Compensation: 0%

LENDS is private-company equity and therefore naturally exposed to shareholder, board, and management decisions. These are treated as part of the private-company issuer risk rather than a separate governance-risk premium.

No additional standalone governance-risk premium is assigned to avoid double-counting.

### Legal Risk: n/a

Description: No separate legal-risk premium is assigned in the current classification.

Probability: n/a

Severity: n/a

Compensation: 0%

LENDS is issued through a Swiss tokenized-share framework using Aktionariat technology. LENDS tokens are described as registered shares of Switzerlend AG under Swiss law, structured as ledger-based securities under Art. 973d of the Swiss Code of Obligations.

Therefore, no legal-risk premium is necessary.

### Liquidity Risk: Secondary Market Liquidity

Description: LENDS has limited secondary-market liquidity and no reliable public-market price.

Probability: Low

Severity: Severe

Compensation: 0.50%

This is a material tail risk. Even if the token has fundamental value, concentration is high and liquidators may not be able to realise that value quickly. Private-company equity can require a longer sale process, and a smaller buyer universe.

The internal marketplace and brokerbot infrastructure are useful, but they should not be treated as equivalent to public-market liquidity.

A 0.50% compensation is assigned for residual liquidity and valuation-realisation risk.

### Contagion Risk: n/a

Description: No separate contagion-risk premium is assigned.

Probability: Negligible

Severity: n/a

Compensation: 0%

LENDS is not exposed to DeFi contagion in the same way as crypto-native collateral.

No separate contagion-risk premium is assigned.

## Conclusion

LENDS is a complex collateral because there is no continuously observable public-market price that can be used as a reliable liquidation reference. The relevant collateral value must therefore be derived from company valuation and warrants conservative buffers.

The latest H1 2026 figures support a base-case valuation range of approximately CHF 12 million–18 million, or CHF 16.85–25.28 per share based on 712,028 total shares outstanding. This range is supported by 10×–15× annualised EBITDA and 2.0×–3.0× annualised revenue.

The 40% retained reserve and CHF 20.00 liquidation price are important safeguards. The 4.00% target interest rate reflects the counterparty, liquidity, and residual smart-contract risk, while the 500,000 ZCHF global minting limit keeps the exposure contained while only share class C1 is tokenised.

The position should be reassessed as updated financial statements become available.
