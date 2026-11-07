# Changelog

Keep this file in the repo. Commit after every update so GitHub's history lets you go back to any earlier version.

## Latest
- Meta refresh after GD06 (ExBurst, Aug 9 - Nov 7, 2026): new top-10 ranking and a Nov 1 Top 8 Char's Zaku II list. GD06 builds are still under 1% of the field.
- Added 103 promotional EX Base, EX Resource, Resource cards and Deck Build Box cards; 6 of the 15 numbers missing from the collection import are now covered. R-020 to R-029 (8 cards) and T-014 are still unknown.
- Deck Import: "Add all to my collection" is now "Add missing copies". It raises each card only up to the deck's quantity instead of adding on top, so pressing it twice no longer inflates counts.
- Backup files are now named gundam-trading-card-game-backup-YYYY-MM-DD.json, using your local date.
- Cleaned printing labels such as "(LR+)", "(R+)", "(SP)" and a card's own number out of about 60 card names (for example "Victory Gundam (LR+)" is now "Victory Gundam"), so name search and name-based import match correctly.
- Refreshed Stardust Trails (GD06) from the release-day TCGCSV file: 130 numbered cards (4 changed since pre-release) plus 8 new Unit Tokens. Removed the pre-release notes.
- Added developer documentation in `docs/`: a developer guide, a build log with every bug and its cause, and a learning path.
- Mobile layout pass 1: tabs wrap into a 3-column grid instead of scrolling sideways, fixed the white strip from page overflow, single-column deck cards, larger tap targets, and 16px inputs so iPhones do not zoom on focus.
- My Collection can import a CSV or Excel collection export (tested design: ExBurst columns Card No / Owned). Choose to keep the higher count, add, or replace; alternate arts count toward the main card.
- Correction: ST07 to ST09 are smaller than 16 cards, so ST07-016, ST08-016 and ST09-011 to ST09-016 do not exist. They were wrongly listed as missing; all starter-deck cards in the source files are loaded.
- Confirmed 78 Units (GD03 to GD06, EB01, ST07 to ST13) have no effect text, so their popups now say "No effect text" instead of "not loaded yet". The 10 Unit Tokens are still unchecked.
- Added effect text and traits for GD04, GD05 and ST11-ST14 from TCGCSV files, filled promo gaps, merged duplicate and alternate-art entries (one entry per card number), and grouped EX Base, EX Resource, Resource and Token cards in the set dropdown. The importer now recognizes EXB-, EXBP-, EXR-, EXRP-, R-, RP- and T- codes.
- Added GD03, EB01, ST07-ST10 and GD06 (pre-release) with full effect text from TCGCSV files. Added credits to the app footer and a SOURCES.md file.
- Added all Phantom Aria (GD04) cards (stats only). Card list now loads 60 at a time with a Show more button, which fixes scroll lag.
- Removed the game counts from the Match Log and New Sets & Backup tabs.
- Fixed the 2-color rule wrongly flagging two-color decks (some cards stored colors as "white" instead of "White", and "-" counted as a color). The color filter now includes those cards too.
- Meta Report now uses ExBurst tournament data (Jul 22 - Oct 20, 2026) with one verified Aile Strike + Strike Freedom list.
- Collection shows art tiles with + / - controls, filtering, sorting, and quick add.
- Card Database can be filtered by set; new sets can be pasted in under New Sets & Backup.
- Match Log entries can be edited; added a deck dropdown, mulligan, and opponent username.
- Legality checker follows the Sept 25, 2026 ban list.
- Renamed the app to Hangar.

## Must keep working (check these after every update)
1. Collection, saved decks, match log, and added cards survive a page reload.
2. Backup > Download / Show as text > Restore works.
3. Deck Import handles `// Main Deck` headers, `4x ID` lines, and flags unknown cards.
4. Legality check flags banned cards, banned pairs, and the vanilla-unit group, but not legal two-color decks.
5. Card Database set, color, type, and search filters all work together.
