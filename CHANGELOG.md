# Tools Hub – Changelog

## v1.2.2 – CI & Deploy Automation

- Added **GitHub Actions CI** with Prettier formatting and internal link checks.
- Configured **FTP deploy** to automatically publish changes to `public_html/jithin/tools` on FastShoes.
- Ensured deploy only runs **after CI passes** (no broken builds live).
- Tweaked CI to skip flaky external link checks (only internal links checked).

## v1.2.1 – Title/Heading Sync

- Updated `<title>` and `<h1>` for SQL IN() Generator for consistency.

## v1.2 – SQL Support Added

- Added SQL IN() Generator (CSV/XLSX/XLS → SQL IN() lists).
- Options for String (quoted) or Integer (no quotes).
- Deduplication + Copy-to-Clipboard.

## v1.1 – Expanded with Time Conversion

- Added Timezone Converter (GMT → selectable timezone).
- Static IANA timezone list with abbreviations.

## v1.0 – Initial Release

- CSV Splitter Tool (chunk CSV files, ZIP download).
