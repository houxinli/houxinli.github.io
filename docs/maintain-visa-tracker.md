# Maintain Visa Tracker (Monthly)

## Data file
- Path: `data/visa_bulletin_cn_eb.json`
- Update `updated_at` each month.
- Append new `records` rows for both categories (`EB2`, `EB3`) and both chart types (`FAD`, `DOF`).

## Cutoff value format
- `YYYY-MM-DD`: regular cutoff date
- `C`: Current
- `U`: Unavailable

## Monthly update checklist
1. Open the latest U.S. Department of State Visa Bulletin.
2. Locate Employment-Based table values for China-mainland born.
3. Update the JSON rows for the new bulletin month.
4. Verify with local preview: `python3 -m http.server 8000` and open `/visa-tracker/`.
5. Commit and publish.

## Notes
- The current JSON is sample data for MVP visualization.
- Keep a source URL trail in commit messages or future fields if auditability becomes important.
