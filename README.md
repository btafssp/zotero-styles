# Zotero citation styles

Two custom CSL citation styles for canon law writing in Zotero.

## The styles

- **[jurist.csl](jurist.csl)**: *The Jurist* (School of Canon Law, The Catholic University of America). Footnote style in US English, with full names, US dates, imprint in parentheses, and bare page numbers. It follows the *Jurist* style guide first, then the CUA School of Canon Law Style Manual (2019), then recent published practice.
- **[studia-canonica.csl](studia-canonica.csl)**: *Studia Canonica* (Saint Paul University, Ottawa). Footnote style in Canadian English, following the journal's instructions to authors and the Saint Paul University faculty guidelines.

## Installing in Zotero

Either:

- Open the raw link in Zotero's browser connector or download it and double-click it:
  - https://raw.githubusercontent.com/btafssp/zotero-styles/main/jurist.csl
  - https://raw.githubusercontent.com/btafssp/zotero-styles/main/studia-canonica.csl
- Or download the `.csl` file, then in Zotero go to **Settings > Cite**, click **+**, and pick the file.

## Library conventions

These styles rely on conventions in the Zotero library they were built for, so they may give odd results with other libraries:

- Extra fields such as `original-date`, `issue`, `chair`, and `citation-label` (the comment at the top of each file lists every key it reads).
- Latin words and titles wrapped as `<i><span class="nocase">…</span></i>`.

## Notes

### Short Title vs citation-label (Jurist and Studia canonica, Book / Manuscript / Article)

**Short Title** (Zotero built-in) is a shortened title, not an abbreviation.

- Printed in subsequent notes in both styles in place of the full title. Never printed in the bibliography.
- Book: italic by default, set by the style. Manuscript: italic by default. Article: formatted like the article title, in quotation marks.
- If the field is empty, the style builds a short form from the full title.
- First-note announcement (`(=X)` in Studia, `(hereafter X)` in Jurist) is built from the Short Title only for book sets and single volumes of a set (`numberOfVolumes` or `volume` present), and only when there is no citation-label.
- Exceptions are tagged in the field. In an italic-default type, wrapping a part in `<i>…</i>` flips it to roman (e.g. `<i>1917</i> CIC`). Zotero drops `font-style:normal` spans, so don't use them.

**citation-label** (custom line in Extra) is an abbreviation the author chooses (e.g. 1917 CIC, COD, XYZ/YEAR).

- Whenever present, on any type, it produces the first-note announcement, with priority over the Short Title.
- Printed exactly as tagged in the data (italic abbreviation where tagged; slash and year roman).
- For magisterium and Corpus items, it is used in later notes in place of a title, so those never fall back to the Short Title.

## Licence

Licensed under [Creative Commons Attribution-ShareAlike 3.0](https://creativecommons.org/licenses/by-sa/3.0/), the standard licence for CSL styles. See [LICENSE](LICENSE).

© 2026 Brian T. Austin
