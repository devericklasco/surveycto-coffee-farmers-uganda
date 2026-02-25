# Testing Notes

## Checklist and outcomes

- [x] Consent no path ends main modules
  - Outcome: When `consent_given = no`, modules C-F are skipped and only Visit Outcome is completed.
- [x] Skip logic branches behave correctly
  - Outcome: Conditional fields open only when triggered (`fertilizer_type`, `avg_price_ugxkg`, follow-up phone, other-specify fields).
- [x] Constraints trigger correct messages
  - Outcome: Bilingual constraint messages display for age, acreage, yield, price, ID, and phone format errors.
- [x] Other/specify flow works
  - Outcome: Text details become required when `other` is selected in configured multiple/single select questions.
- [x] Calculation safety for acres = 0 or blank
  - Outcome: `yield_per_acre_kg` remains blank when `coffee_acreage` is zero; no divide-by-zero failure.
- [x] Incomplete interview reasons captured
  - Outcome: `incomplete_reason` appears when consent is refused or when interview is not completed.
- [x] GPS capture flow
  - Outcome: `farm_gps` optional; `gps_accuracy_m` computes when GPS is captured and remains blank when missing.

## Known limitations

- District list is a compact demo list, not a full Uganda admin coding frame.
- Luganda text is simplified and should be reviewed by local language specialists before production use.
- No external lookup tables (e.g., dynamic admin hierarchy) are included in this sample.
- Interview start/end duration depends on device time accuracy.

## Next improvements

- Add full district-subcounty-parish coded rosters with cascading select logic.
- Add enumerator roster validation with preloaded IDs.
- Add audit trail configuration and monitor fields for supervision.
- Add numeric outlier flags for yield and price for real-time QA dashboards.
