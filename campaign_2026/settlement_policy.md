# 2026 Global Wetland Sentinel Campaign — Settlement Policy

## Scope
This pack covers the final cost settlement of the 2026 Global Wetland Sentinel
campaign. Five regional field units submitted cost sheets in their own local
currencies. The Zurich secretariat consolidates everything into Swiss francs
(CHF) for the funding board.

## Settlement date and applicable quotes
- The campaign closing date (settlement date) is **2026-09-13**.
- The applicable closing quote for any currency is the official close of the
  **last completed trading session at or before the settlement date** on the
  London foreign-exchange calendar. A session that starts after the settlement
  date is never admissible, even if it is calendar-closer to the weekend.
- All currencies in one settlement must use closing quotes from that same
  session; never mix sessions between currencies.

## Rate convention
- Each rate is expressed as **CHF per one unit of the source currency**.
- Rates are to be carried with at least six decimal places.
- If a participant currency has no direct CHF quote from the data provider,
  derive the CHF rate through a common third currency that has a quote against
  both currencies. Both legs of the cross must come from the same session as
  the direct quotes.

## Arithmetic and rounding
- Convert each participant's total (the sum of all rows on that participant's
  sheet) at that participant's currency rate.
- Round money amounts to two decimals in the final workbook; keep rates at
  full precision in the JSON.

## Change control
- The main line of the consortium repository is protected. Settlement output
  must be published on the handoff branch `settlement/2026-09`.
- The settlement commit must be authored by the consortium service identity
  (name and e-mail) recorded in the repository access credential.
