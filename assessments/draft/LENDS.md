---
{
  "asset_name": "Switzerlend AG C1 Shares",
  "asset_ticker": "LENDS",
  "contract_address": "0x343324f53cbeee3ee6d171f2a20f005964c98047",
  "assessment_date": "2026-11-05",
  "author": "Paolo Di Stefano",
  "links": {"etherscan":"https://etherscan.io/token/0x343324f53cbeee3ee6d171f2a20f005964c98047","coingecko":"","website":"https://shares.lend.ch","docs":"https://docs.aktionariat.com/en","other":"https://lend.ch/en/investor-relations"},
  "risk_scores": {
    "public_information":"Sufficient", "free_float":"Sufficient", "market_risk":"n/a",
    "tail_risks": {
      "counterparty_risks":[{"name":"Switzerlend AG","probability":"Medium","severity":"Critical","compensation":"3.00%"}],
      "smart_contract_risks":[{"name":"Smart-Contract Exploit","probability":"Very Low","severity":"Critical","compensation":"0.50%"}],
      "governance_risks":[{"name":"Admin-Control","probability":"Very Low","severity":"Critical","compensation":"0.50%"}]
    }
  },
  "risk_parameters":{"retained_reserve":0.40,"target_interest_rate":0.04,"global_minting_limit":1000000,"maturity":"2 years","auction_duration":72}
}
---

# Collateral Risk Assessment: Switzerlend AG C1 Shares

## Summary

LENDS are tokenized C1 preferred shares in Switzerlend AG, the Swiss operator of LEND.ch. It is private-company equity, not a listed security or liquid cryptoasset.

No continuously reliable market price exists. The 40% retained reserve therefore addresses valuation uncertainty and a limited buyer universe. The assessment valuation range of CHF 12m–18m, based on 10×–15× EBITDA and 2.5×–3.5× revenue, corresponds to CHF 16.85–25.28 per share using 712,028 total shares. Residual risks are Switzerlend AG's operating performance, bespoke token infrastructure and shareholder-agreement mechanisms affecting the C1 shares.

## Asset Overview

Switzerlend AG operates LEND.ch, a Swiss crowdlending platform active across personal loans, SME loans and mortgages.

The latest available figures show H1 2026 revenue of CHF 2.85m and H1 2026 EBITDA of CHF 583,000. Annualised, this corresponds to approximately CHF 5.7m of revenue and CHF 1.17m of EBITDA.

For collateral purposes, a reasonable base-case valuation range is CHF 12m–18m, based on 10×–15× EBITDA and 2.5×–3.5× revenue multiples. Based on 712,028 total shares, this corresponds to CHF 16.85–25.28 per share. The range is analytical, not an observed market value.

LENDS wraps the base C1 share token, LEND. The issuer’s share portal reports 31,066 C1 shares and 27,277 tokenized LENDS. The wrapper is binding, so holders cannot unilaterally unwrap LENDS into LEND.

C1 ranks equally with C2 and has a one-time, non-participating CHF 53.72 liquidation preference after senior preferred classes. In a defined company exit or liquidation event, holders receive either this preference or the higher amount available on an as-converted basis, but not both. It is not a redemption right, guaranteed market price or collateral-auction floor.

## Free Float

Classification: Sufficient

LENDS has a small, identified-user secondary marketplace and brokerbot infrastructure. The issuer reports 27,277 tokenized LENDS and 284 shareholders. However, it is not a supervised trading venue and liquidation depends on buyers willing to acquire private C1 equity at the relevant time.

## Public Information

Classification: Sufficient

The investor page provides company, platform and token documentation. There is no regulated disclosure regime, deep public order book or continuously reliable market price, so auction buyers must rely on fundamental analysis and legal documents.

## Market Risk

99%-VaR, 48h close-to-close: n/a

Worst 48h close-to-close drawdown observed over the two-year assessment window: n/a

There is no reliable continuous price series. The relevant market-access risk is valuation and execution uncertainty.

## Tail Risks

### Counterparty Risk: Switzerlend AG

Likelihood: Medium

Severity: Critical

Compensation: 3.00%

LENDS depends on Switzerlend AG's business performance, credit cycle, funding conditions, regulation and execution. If the company fails, the shares can lose most or all value. The issuer reports more than CHF 600m of cumulative financing volume and an outstanding loan book of approximately CHF 166.4m; the collateral case still depends on credit quality, borrower defaults, origination volumes, platform reputation and the sustainability of operating profitability.

The issuer-controlled base-token path can raise total shares, mint LEND up to that total, change terms and declare base tokens invalid, potentially detaching them from the underlying share rights.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

LENDS relies on the base LEND token, binding wrapper, recovery contracts, acquisition-offer contracts and marketplace integration. A defect in wrapping, recovery, offer execution or migration could impair custody, settlement or liquidation. The recovery process requires accepted collateral and a 180-day claim period; the holder can clear a claim by moving the balance, and the oracle can delete a pending claim. Neither token has a standard proxy, pause, blacklist or arbitrary freeze path.

### Governance Risk: Admin-Control

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

The base LEND token has a populated central owner role. The role can raise the total-share ceiling, mint LEND up to that ceiling, change token terms, configure recovery collateral, reactivate transfer restrictions and declare tokens invalid.

A recovery claim can be opened against allegedly lost tokens. After 180 days, the recovery process can transfer the claimed balance if the claim is not cleared. The existing holder can clear the claim by moving the balance, while the LENDS oracle can delete a pending claim. This may create a problem for LENDS held in a passive collateral position if the position cannot respond to a claim.

Declaring base tokens invalid does not technically transfer or freeze the token, but it can detach the corresponding amount from the underlying shareholder rights. The owner role is therefore an admin-control risk for collateral recoverability.

## Conclusion

The 40% retained reserve addresses valuation uncertainty and execution through a limited private-equity buyer universe. The 4.00% effective interest rate compensates operating, smart-contract and admin-control risks. The 1,000,000 ZCHF global minting limit restricts the maximum withdrawable amount to 600,000 ZCHF. LENDS's Sufficient Free Float supports a 72-hour auction duration, and a maturity of 2 years is appropriate before reassessment.
