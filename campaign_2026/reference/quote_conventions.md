# Quote-handling reference notes (treasury desk)

These notes describe how the consortium's market-data provider renders its
daily FX series. They are operational notes, not a substitute for checking the
actual data each time.

- Daily bars are stamped at the **exchange-local start of the session** and the
  vendor renders those timestamps in UTC. During British Summer Time a bar for
  a London session therefore prints with a `T23:00:00.000Z` timestamp on the
  previous calendar day.
- Worked example: a bar printed as `2026-09-06T23:00:00.000Z` is the close of
  the **2026-09-07** London session, not the close of 6 September.
- The date prefix of a printed timestamp is therefore not a reliable session
  date. Convert the timestamp to the exchange calendar before matching it to a
  settlement date.
- The provider's per-date lookup returns both the requested date and the
  session date it actually matched; the matched date is the authoritative
  session date for that quote.
- Some currency pairs are not carried by the provider at all. When a direct
  pair is unavailable, cross through a liquid third currency (the provider
  carries both legs against USD or EUR).
