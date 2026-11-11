# 🧼 Soap Bar Daily Log — PRO v2

The factory's soap log: Shift A / B / C, three lines (Line 1 Savannah, Line 2 Savannah 771,
Line 3 Royal 90-10), the Sheet1 forms with the PNG share, and the 8-hour data tables.

## 📊 Write into your Excel workbook

The shift rows can be written **straight into the original workbook**
(`Daily  Soap bar Analysis  -10.xlsx`) — no more copy → paste:

1. Open the shift you are logging (Shift A / B / C) and fill the tables as usual.
2. Press **📥 Open my file & write into it** in the *8-Hour Data Tables* block.
   (Or **📂 Open my Excel file** first, check the plan, then **✍️ Write into the file**.)
3. Pick which lines to write: *All 3 lines* / *Line 1* / *Line 2* / *Line 3*.

Every line lands on **the first free row of its own sheet** — the last row that has data
plus one, never a hole in the middle of the sheet:

| Line | Sheet in the workbook | Columns |
|---|---|---|
| Line 1 - Savannah | `Line 1 Savannah ` | B–U (8 weights + average) |
| Line 2 - Savannah (771) | `Line 2 Savannah (771)` | B–W (10 weights + average) |
| Line 3 - Royal (90-10) | `Line 3 Royal (90-10)` | B–S (6 weights + average) |

- The values are **exactly** what the *📋 Copy rows* button copies — the app reads its own
  table, nothing is re-invented.
- The date and the time are written as real Excel date/time values, the batch as a number,
  the average as the exact mean of the weights — the way the sheet already keeps them.
- Every new row takes the format the factory rows have: each column uses the **most common**
  look of its own rows, and the block keeps the factory's borders (a thick line on the top of
  the first row and on the bottom of the last one). A broken format in the file — a wrong
  font, a colour, a *text* number format — can never come into the new rows.
- The workbook is re-read right before writing, so edits you made in Excel meanwhile are
  never lost, and the file is updated **in place** (no download) on Chrome / Edge.
- The engine is [ExcelJS](https://github.com/exceljs/exceljs) (vendored in `vendor/`).

## Other things in here

- **📋 Copy rows** — the rows as TSV, exactly as they appear on screen.
- **📊 Export to Excel (.xlsx)** — a native OOXML file, no libraries.
- **🖼 Sheet1 PNG** — share or save the three batch sheets as images.
- **☁️ Cloud** — encrypted sync (Firebase RTDB) of everything, plus a JSON backup.
- **📲 Install app** — install it as a PWA (works offline).

`DEFPIN` (the cloud PIN) defaults to `2780` — change it in the sync settings.
