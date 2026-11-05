---
{
  "asset_name": "draggable quitt.shares",
  "asset_ticker": "DQTS",
  "contract_address": "0x8747a3114ef7f0eebd3eb337f745e31dbf81a952",
  "assessment_date": "2026-11-05",
  "author": "Paolo Di Stefano",
  "links": {
    "etherscan": "https://etherscan.io/token/0x8747a3114ef7f0eebd3eb337f745e31dbf81a952",
    "coingecko": "",
    "website": "https://shares.quitt.ch",
    "docs": "https://docs.aktionariat.com/en",
    "other": "https://github.com/Frankencoin-ZCHF/Frankencoin/discussions/24"
  },
  "risk_scores": {
    "public_information": "Sufficient",
    "free_float": "Sufficient",
    "market_risk": "n/a",
    "tail_risks": {
      "counterparty_risks": [
        {
          "name": "ServiceHunter AG",
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
          "name": "Admin-Control",
          "probability": "Very Low",
          "severity": "Critical",
          "compensation": "0.50%"
        }
      ]
    }
  },
  "risk_parameters": {
    "retained_reserve": 0.40,
    "target_interest_rate": 0.04,
    "global_minting_limit": 5000000,
    "maturity": "2 years",
    "auction_duration": 72
  }
}
---

# Collateral Risk Assessment: draggable quitt.shares

## Summary

DQTS is the tokenized equity of ServiceHunter AG, the Swiss operator of quitt, a SaaS platform for household-employment administration. It represents private-company equity rather than a liquid crypto asset or listed security.

There is no continuously observable secondary-market price for DQTS. Collateral value must therefore be assessed from the company's financial performance and a fundamental equity valuation, while liquidation depends on a narrower buyer universe than for listed shares.

The main residual risks are ServiceHunter AG's operating and group-financial performance, and DQTS's bespoke token mechanics, including a 180-day lost-key-recovery procedure through which a recoverable DQTS balance can be claimed.

## Asset Overview

ServiceHunter AG's Swiss core business generated CHF 5.5 million of revenue in 2025 and was profitable. The German and UK entities were still loss-making while the group pursued international expansion. The assessment uses a CHF 16 million equity reference value, or CHF 8.00 per share based on 2,000,000 total shares, supported by the consolidated financial analysis and the planned share transaction at that price.

The valuation considers four methods:

- Adjusted net asset value: CHF 0.2 million–4.0 million. This has limited relevance for a SaaS company because intellectual property and the customer base are not fully captured on the balance sheet.
- Earnings value: CHF 8.6 million–16.6 million. This is highly relevant because it reflects the current sustainable profit base.
- Comparable-company multiples: CHF 19.8 million–30.7 million. This is highly relevant because it reflects observed market transactions.
- Discounted cash flow: CHF 26 million–37 million. This captures growth potential but is less suitable for collateral purposes because future growth remains uncertain.

For a SaaS business, the earnings-value and multiples approaches are the most relevant. A 10× multiple of the Swiss core's CHF 1.6 million EBITDA also supports the CHF 16 million reference. The equity reference should be reassessed against updated financial statements and net debt before each maturity extension.

DQTS is issued using Aktionariat's draggable-share infrastructure. Non-tokenized shares are of the same share class and can be tokenized, which can expand the potential on-chain supply available to challengers and auction buyers.

## Free Float

Classification: Sufficient

DQTS has a tokenized shareholder base and a small, identified-user marketplace operated through quitt.shares. Non-tokenized shares of the same class can also be tokenized, so independent challengers are not limited to the existing on-chain float.

However, DQTS remains private-company equity. Auction outcomes depend on buyers' willingness to acquire ServiceHunter AG shares at a fundamental valuation rather than on a deep, continuously quoted market. This supports a Sufficient, rather than Strong, Free Float classification.

## Public Information

Classification: Sufficient

ServiceHunter's financial information, the token contract and company information are available to assess the equity value. This provides a basis for challengers to estimate auction outcomes.

Public information remains weaker than for a listed company. There is no continuously observable secondary-market price, and company value must be estimated from financial statements, comparable-company evidence and the capital structure.

## Market Risk

99%-VaR, 48h close-to-close: n/a

Worst 48h close-to-close drawdown observed over the assessment window: n/a

DQTS has no reliable continuous secondary-market price series. The retained reserve is therefore calibrated to valuation uncertainty and the expected discount required to sell private-company equity through an auction.

## Tail Risks

### Counterparty Risk: ServiceHunter AG

Likelihood: Medium

Severity: Critical

Compensation: 3.00%

DQTS represents equity in a private operating company. The Swiss core business is profitable, but the German and UK entities remain less mature and have required continued investment. A deterioration in operating performance, group financial position or execution could materially impair the value of the equity.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

DQTS is a verified, direct and non-upgradeable DraggableShares contract. It has no owner, proxy upgrade, pause, blacklist, freeze or unilateral forced-transfer function. It nevertheless uses bespoke acquisition-offer, migration, wrapping and lost-key-recovery mechanics. Anyone can declare a balance lost by posting eligible collateral and, after 180 days, recover that balance if recovery remains enabled. A technical failure or an unresolved recovery claim could impair transferability, backing or recoverability.

### Governance Risk: Admin-Control

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

DQTS is currently binding to its QTS backing. The QTS owner is a four-signer Aktionariat multichain-wallet clone. It cannot transfer DQTS from a collateral position, but it can issue additional QTS, increase the total-share cap before minting and declare QTS detached from shareholder rights. These actions could dilute or impair the economic claim backing DQTS.

DQTS also includes a 75%-quorum acquisition-offer process, an 80%-holder migration path and a 180-day lost-key-recovery mechanism. An accepted offer or completed migration changes the backing asset into a currency claim or successor token, which can affect the asset that Frankencoin must liquidate.

## Conclusion

The 40% retained reserve provides a substantial buffer against valuation uncertainty and the auction discount required for private-company equity. The 4.00% effective interest rate compensates the assessed tail risks. The framework requires a cap on the global minting limit because ServiceHunter AG carries a Medium-probability counterparty risk; the 5,000,000 ZCHF global minting limit restricts the maximum withdrawable amount to 3,000,000 ZCHF. DQTS's Sufficient Free Float supports a 72-hour auction duration, and a maturity of 2 years is reasonable before the collateral needs to be reassessed.
