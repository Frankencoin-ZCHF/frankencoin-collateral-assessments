---
{
  "asset_name": "Space Exploration Technologies Corp. (Ondo Tokenized)",
  "asset_ticker": "SPCXon",
  "contract_address": "0xc9eef266834730340A55B6CC24621B31BAF55581",
  "assessment_date": "2026-11-06",
  "author": "Paolo Di Stefano",
  "links": {"etherscan":"https://etherscan.io/address/0xc9eef266834730340a55b6cc24621b31baf55581","coingecko":"https://www.coingecko.com/en/coins/spacex-ondo-tokenized-stock","website":"https://app.ondo.finance/assets/spcxon","docs":"https://docs.ondo.finance/ondo-stocks/overview","other":"https://ondo.finance/ondo-stocks"},
  "risk_scores": {
    "public_information":"Strong", "free_float":"Strong", "market_risk":"19.40%",
    "tail_risks": {
      "counterparty_risks":[
        {"name":"SpaceX","probability":"Medium","severity":"Moderate","compensation":"0.75%"},
        {"name":"Ondo Finance","probability":"Very Low","severity":"Severe","compensation":"0.25%"}
      ],
      "smart_contract_risks":[{"name":"Smart-Contract Exploit","probability":"Very Low","severity":"Critical","compensation":"0.50%"}],
      "governance_risks":[{"name":"Admin-Control","probability":"Very Low","severity":"Critical","compensation":"0.50%"}]
    }
  },
  "risk_parameters":{"retained_reserve":0.30,"target_interest_rate":0.020,"global_minting_limit":2000000,"maturity":"2 years","auction_duration":24}
}
---

# Collateral Risk Assessment: Space Exploration Technologies Corp. (Ondo Tokenized)

## Summary

SPCXon is an Ondo tokenized-security product referencing Space Exploration Technologies Corp. Class A common stock, listed as SPCX. It is an open-ended structured note issued by Ondo Global Markets (BVI) Limited, not a direct shareholding. Holders receive no voting, information or in-kind delivery rights in SpaceX.

The 30% retained reserve addresses the short post-listing price history of SPCX. The main residual risks arise from the issuer and redemption structure, the broker and custody chain, the smart-contract stack and central compliance and administrative controls.

## Asset Overview

SpaceX is a space-infrastructure company focused on reusable rockets, satellite connectivity, crew and cargo spacecraft, and government and commercial launch services. Its Class A common stock trades as SPCX on Nasdaq Global Select Market and Nasdaq Texas. As a single-name equity exposure, it remains sensitive to company-specific events including major operational disruption, failed launches, regulatory intervention and changes in investor confidence.

SPCXon is designed to track the total return of SPCX. It initially tracks one share per token, but net dividend reinvestment can result in one token tracking more than one share. The issuer is Ondo Global Markets (BVI) Limited, a BVI bankruptcy-remote special-purpose vehicle. Ondo Finance Inc. provides tokenization and platform services.

Alpaca Securities LLC acts as broker and custodian, together with BitGo Trust Company, Inc. Ankura Trust Company, LLC acts as security and verification agent. The notes are stated to be fully backed with an additional collateral buffer, and tokenholders have a first-priority security interest over the relevant collateral through Ankura. Redemption is a cash or stablecoin claim against Ondo Global Markets, subject to KYC and compliance. Approved institutions may have access to an Alpaca in-kind conversion route, but this is not a general tokenholder right.

## Free Float

Classification: Strong

SPCXon can be minted and redeemed through Ondo’s highly liquid primary market. It trades directly as SPCXON/USDON and has verified SPCXON/USDT markets on MEXC and Gate. It also has markets on Uniswap on Ethereum and BNB Chain, with further venues on Solana. Ondo supports off-hours trading on Ethereum, BNB Chain and Solana.

These routes give independent challengers and auction buyers several ways to acquire and sell SPCXon. Ondo does not guarantee a secondary market or sufficient liquidity at all times, but the available trading and redemption routes support a Strong Free Float classification.

## Public Information

Classification: Strong

SPCX is a publicly listed equity with Nasdaq as the principal reference source in the SPCXon final terms. SPCXon has published final terms, base prospectus and token documentation covering the issuer, backing, custody, redemption and transfer restrictions.

Challengers can estimate expected auction outcomes from Nasdaq reference prices and SPCXon secondary-market prices, applying the relevant token-market and redemption discount.

## Market Risk

Worst 48h close-to-close drawdown observed: 19.40%

SPCX began trading on 12 June 2026 and the observed worst decline occurred shortly after listing, when price discovery was still limited.

The short history supports a 30% retained reserve, which is above the observed drawdown and provides additional room for challenger reward and tokenized-equity execution.

## Tail Risks

### Counterparty Risk: SpaceX

Likelihood: Medium

Severity: Moderate

Compensation: 0.75%

SPCXon ultimately references the equity value of Space Exploration Technologies Corp. The collateral is therefore exposed to company-specific tail events affecting SpaceX, including fraud, major operational disruption, failed launches, regulatory intervention and a material deterioration in investor confidence.

These risks are not captured by ordinary short-term price volatility alone and can impair the underlying share value beyond the reserve buffer.

### Counterparty Risk: Ondo Finance

Likelihood: Very Low

Severity: Severe

Compensation: 0.25%

SPCXon depends on Ondo’s tokenized-asset issuance, redemption, operational and custody structure. Ondo Global Markets (BVI) Limited is the legal issuer and redemption obligor; Ondo Finance Inc. provides tokenization and platform services.

Even if the underlying SpaceX exposure remains valuable, liquidation efficiency may be impaired if the Ondo structure fails to process minting or redemption, maintain the collateral arrangement or make the issuer claim recoverable.

### Smart-Contract Risk: Smart-Contract Exploit

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

SPCXon is an EIP-1967 BeaconProxy using the GMToken implementation. A defect or exploit in the token, beacon, compliance stack, pause-manager or material issuance and redemption integration could impair balances, supply, transfers or settlement.

### Governance Risk: Admin-Control

Likelihood: Very Low

Severity: Critical

Compensation: 0.50%

The token’s default admin owns the shared beacon and can replace the implementation. It can grant and revoke minting, burning and configuration roles. The active pause-manager can pause the token or all associated tokens. The live compliance stack uses global-markets and sanctions blocklists, and every mint, burn, transfer and transferFrom operation checks compliance and token-pause state.

A blocked address cannot send, receive or use delegated transfers. The default admin can grant a burner role, replace the compliance contract or pause-manager, or upgrade the shared beacon. These powers can make pledged SPCXon untransferable or change the token’s behaviour during a liquidation.

## Conclusion

The 30% retained reserve is above the 19.40% worst 48h close-to-close drawdown observed for SPCX and provides a buffer for challenger reward and tokenized-equity execution. The 2.00% effective interest rate compensates SpaceX counterparty risk, Ondo Finance issuer and redemption risk, smart-contract risk and admin-control risk. The 2,000,000 ZCHF global minting limit restricts the maximum withdrawable amount to 1,400,000 ZCHF and contains the Medium SpaceX counterparty risk. SPCXon’s Strong Free Float supports a 24 hour auction duration, and a maturity of 2 years is appropriate before reassessment.
