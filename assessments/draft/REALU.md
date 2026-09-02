---
{
  "asset_name": "RealUnit Schweiz AG",
  "asset_ticker": "REALU",
  "contract_address": "0x553C7f9C780316FC1D34b8e14ac2465Ab22a090B",
  "assessment_date": "2026-08-01",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x553C7f9C780316FC1D34b8e14ac2465Ab22a090B",
    "coingecko": "",
    "website": "https://realunit.ch/loesung/aktie-und-finanzdaten/",
    "docs": "https://realunit.ch/loesung/aktientoken/",
    "other": "https://realunit.ch/wp-content/uploads/dlm_uploads/2026/03/Geschaeftsbericht-RealUnit-2025_compressed.pdf"
  },
  "risk_scores": {
    "public_information": "Sufficient",
    "free_float": "Sufficient",
    "market_risk": "11.56%",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "RealUnit Schweiz AG",
          "probability": "Medium",
          "severity": "Severe",
          "compensation": "1.00%"
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
          "name": "Company Governance",
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
    "retained_reserve": 0.15,
    "target_interest_rate": 0.02,
    "global_minting_limit": 8000000,
    "liquidation_price": 1.2,
    "maturity": null,
    "auction_duration": 36,
    "minimum_collateral": 5000
  }
}
---

# Collateral Risk Assessment: RealUnit Schweiz AG

## Summary

REALU is the tokenized equity token of RealUnit Schweiz AG, a Swiss investment company. The token is issued using Aktionariat AG technology and represents tokenized registered shares on Ethereum.

The relevant collateral value is primarily the company's reported net asset value (NAV), supported by a portfolio of equities, physical precious metals, cash, and some crypto assets.

Per the 2025 annual report, RealUnit reported net assets of CHF 52.6 million and 39,093,976 shares outstanding, corresponding to a NAV of CHF 1.35 per share. The RealUnit website currently reports a live NAV of CHF 1.32 per share.

## Introduction

RealUnit Schweiz AG is a Swiss investment company founded in 2017 and domiciled in Baar. Its stated strategy is real capital preservation through investments in physical precious metals, Swiss and international equities, cash, nominal assets, alternative investments, and a small crypto allocation.

REALU should therefore be assessed differently from ordinary equity tokens. RealUnit does not have an operating business where enterprise value must be estimated from earnings, revenue multiples, or DCF assumptions.

Besides the regularly updated (indicative) NAV value on their website, the company is also listed on BX Swiss. This improves public information and gives an observable reference price on the secondary market. However, BX Swiss is a small trading venue and should not be treated as equivalent to a deep listed-equity market.

From a collateral perspective, the NAV remains the main valuation anchor. Real Unit however declares that the self-reported NAV on their website might be incorrect, incomplete or temporarily unavailable. That means only the NAV reported with the officially prepared quarterly report should be considered a reliable source of truth.

The 2025 balance sheet shows total assets of CHF 53.9 million, total liabilities of CHF 1.3 million, and total equity of CHF 52.6 million. Portfolio allocation at year-end was dominated by physical precious metals at 46.9%, equities at 32.4%, physical CHF cash at 8.5%, nominal assets at 5.2%, alternative investments at 3.9%, and crypto assets at 3.2%. RealUnit classified 87% of the portfolio as very liquid, 7% as liquid, and 6% as illiquid.

## Free Float/Liquidity

Classification: Sufficient

REALU has two relevant liquidity channels. First, the traditional shares trade on BX Swiss. Second, the tokenized shares issued on Ethereum, which can be bought or sold through the RealUnit / Aktionariat marketplace.

According to the financial report, the management committee also has the right to increase/decrease the number of outstanding shares within a pre-defined range, meaning that large new investments or  sales would likely be solved through primary market transactions (increasing/decreasing the number of shares & the NAV), instead of making the share price fluctuate on the secondary market.

However, liquidity is weaker than for large listed equities or major crypto assets. BX Swiss is a small trading venue, the tokenized share float is limited, and liquidators should not assume that large primary market transactions can always be fulfilled swiftly, as the pre-defined band of number of shares might be reached within a certain period.

The free-float classification is therefore sufficient rather than strong.

## Public Information

Classification: Sufficient

RealUnit publishes financial reports, ongoing NAV information, shareholder and corporate-governance disclosures, and BX Swiss as well as the token market place have regular trading activity.

## Market Risk

99%-VaR, 48h close-to-close: -7.54%

Worst 48h close-to-close drawdown: -11.56%

REALU is listed on BX Swiss, which shows that the worst 48h close-to-close drawdown was -11.56% over the last 2 years of price history.

This means a 15% reserve remains above the observed worst 48h close-to-close drawdown and provides an additional buffer for the challenger reward and auction execution risk.

## Tail Risks

### Counterparty Risk: RealUnit Schweiz AG

Description: The portfolio is managed by RealUnit Schweiz AG, including storage of physical cash and gold, and custody of Bitcoin & ETH. Mismanagement, wrong NAV reporting, or fraud by the company could lead to a sudden NAV impairment.

Probability: Medium

Severity: Severe

Compensation: 1.00%

This is the dominant economic risk. The risk is that the portfolio NAV falls materially, is restated, or cannot be realized at the reported value during stress.

However, the portfolio is diversified and mostly liquid, with substantial exposure to physical precious metals, cash, listed equities, and other financial assets. This supports a lower structural risk profile, and a drawdown beyond the retained reserve would likely not wipe out the entire value of the underlying assets.

A 1.00% compensation is therefore assigned for this counterparty risk.

Global Minting Limit: 5,000,000 ZCHF

Since the classification of this risk is medium, this warrants a cap on the global minting limit. With a 85% reserve requirement, 4,250,000 ZCHF could maximally be withdrawn. Assuming a tail event could lead to a severe but not critical impairment beyond the 15% buffer, this would still be absorbable by the system equity.

### Smart Contract Risk: Smart-Contract Exploit

Description: REALU is implemented as a tokenized equity instrument using Aktionariat AG technology and therefore carries residual smart-contract and token-infrastructure risk.

Probability: Very Low

Severity: Critical

Compensation: 0.50%

REALU is not a vanilla ERC-20 from a collateral perspective. It is a tokenized registered share with related shareholder-registration, and lost-key recovery mechanics. These features are appropriate for a Swiss tokenized-share instrument, but they expand the attack surface relative to a simple ERC-20 token.

A 0.50% compensation is assigned for residual smart-contract and token-infrastructure risk.

### Governance Risk: Company Governance

Description: RealUnit's NAV depends on board, management, and investment-committee decisions regarding asset allocation, capital increases, treasury shares, and investment policy.

Probability: Negligible

Severity: n/a

Compensation: 0%

There is no operating business to manage, but the board, management, and investment committee control the investment strategy and asset allocation.

This is however already addressed by the counterparty risk, therefore no additional premium is assigned.

### Legal Risk: n/a

Description: No separate legal-risk premium is assigned.

Probability: n/a

Severity: n/a

Compensation: 0%

### Liquidity Risk: Secondary Market Liquidity

Description: REALU has better secondary-market liquiditz than other tokenized shares, but liquidity remains limited relative to major listed equities or crypto collateral.

Probability: Low

Severity: Severe

Compensation: 0.50%

The BX Swiss listing and RealUnit's Brokerbot/token infrastructure provide useful secondary market liquidity. They do however not guarantee that a Frankencoin challenger can challenge a large position quickly enough.

In stress, the auction buyer universe may be limited to investors who understand RealUnit, and are willing to hold such a share.

A 0.50% compensation is assigned for residual secondary-market liquidity risk.

### Contagion Risk: n/a

Description: REALU is (intentionally) uncorrelated with crypto markets, and would not be affected by defi/crypto market contagion.

Probability: Negligible

Severity: n/a

Compensation: 0%

No separate contagion-risk premium is assigned.

## Conclusion

REALU is a high-quality collateral . It is materially stronger than other tokenized shares on public information and valuation basis because RealUnit is a BX Swiss-listed investment company and its value is primarily NAV-based, leaving much less room for valuation uncertainty.
