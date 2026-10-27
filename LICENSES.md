# Licenses and attribution

Each pack records its license in `meta.license` / `meta.attribution` and in
`manifest.json` (`license`). The app's 数据来源与许可 page should show the text below.

## Build scripts (this repository's code)

MIT License. Copyright (c) 2026 DAOSI contributors.

## ECDICT — packs `vocab-en-cet4`, `vocab-en-cet6`, `vocab-en-ielts`, `vocab-en-toefl`, `vocab-en-basic`, `vocab-en-tem4`, `vocab-en-tem8`

* Source: <https://github.com/skywind3000/ECDICT> (`ecdict.csv`)
* Author: skywind3000 (Lin Wei)
* License: MIT

Attribution text:

> English vocabulary data from ECDICT by skywind3000 (https://github.com/skywind3000/ECDICT),
> used under the MIT License. Word lists were filtered and cleaned by DAOSI.
> 专四 / 专八 lists are DAOSI reference lists derived from ECDICT tags and frequencies,
> not official syllabi.

MIT License text (as distributed with ECDICT):

```
MIT License

Copyright (c) 2017 Linwei

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

Note: verify the copyright line against the LICENSE file in the ECDICT repository
before the first public release (it was written here from the published MIT template).

## Hand-written samples — packs `vocab-ja-sample`, `vocab-yue-sample`

* Source: `samples/ja.json`, `samples/yue.json` in this repository
* License: CC0 1.0 (public domain dedication), "CC0 (hand-written by DAOSI)"
* No attribution required.

## Hand-written scenarios and tone drills — packs `scenes-en`, `scenes-ja`, `scenes-yue`, `tones-yue`

* Source: `scenes/<lang>/*.json` and `tones/yue.json` in this repository, written by DAOSI
  (no external text was copied or downloaded)
* License: CC0 1.0 (public domain dedication), "CC0 (written by DAOSI)"
* No attribution required. The packs carry `meta.review_needed = 1` until a native speaker
  has checked them (see README "Scenario packs").

## Tatoeba — packs `sentences-en`, `sentences-ja`, `sentences-yue`

* Source: <https://tatoeba.org>, exports of 2026-10-17 (<https://downloads.tatoeba.org/exports/>)
* Authors: the Tatoeba contributors (each sentence's author is listed on
  `https://tatoeba.org/sentences/show/<id>`; pack ids are `tatoeba:<id>`)
* License: sentences CC BY 2.0 FR (<https://creativecommons.org/licenses/by/2.0/fr/>);
  some sentences are also CC0, but the packs treat all of them as CC BY 2.0 FR.
* Changes: filtered, whitespace-normalised, deduplicated, paired with one Chinese
  translation and linked to vocab ids. The packs are distributed under CC BY 2.0 FR.

Attribution text (required):

> Sentences from Tatoeba (https://tatoeba.org), CC BY 2.0 FR

Audio: the packs only store a link (`https://tatoeba.org/audio/download/<audio id>`) plus
`audio_license` and `audio_author` per sentence; this repo redistributes no audio. Only
CC BY 4.0 and CC BY-SA 4.0 (CC0 would also qualify) audio is linked; NC, ND and unlicensed
audio is skipped. When the app plays a clip it must credit it, e.g.
"Audio: <audio_author>, <audio_license>, via Tatoeba".

## JLPT vocabulary — packs `vocab-ja-n5`, `vocab-ja-n4`, `vocab-ja-n3`, `vocab-ja-n2`, `vocab-ja-n1`

Pack license: **CC BY-SA 4.0** (<https://creativecommons.org/licenses/by-sa/4.0/>), because the
packs contain JMdict data. `meta.license` = "CC BY-SA 4.0 (JMdict/EDRDG; JLPT lists CC BY J. Waller)".

* **JLPT level lists** — Jonathan Waller, <https://www.tanos.co.uk/jlpt/>. License verified on
  the site's "Use my data!" page (<https://www.tanos.co.uk/jlpt/sharing/>, read via the Internet
  Archive copy because the site's TLS did not answer): everything on the site that is not for sale
  "is licenced under Creative Commons "BY"" — commercial use allowed, credit the site. (No CC version
  number is stated.)
* **open-anki-jlpt-decks** — Jamie Sinclair, <https://github.com/jamsinclair/open-anki-jlpt-decks>
  (commit `1ad66734417aca9dbcca6b2d5ee440cb13ab3ba0`), MIT License, "Copyright (c) 2020 Jamie
  Sinclair" (LICENSE file read 2026-10-27). Its CSVs (`src/n1.csv` … `n5.csv`) are based on the
  tanos lists; used for headword, kana reading, level, and as fallback English meaning.
* **JMdict** — Electronic Dictionary Research and Development Group (EDRDG), `JMdict_e.gz` of
  2026-10-26 (<http://ftp.edrdg.org/pub/Nihongo/JMdict_e.gz>). License: CC BY-SA 4.0, per
  <https://www.edrdg.org/edrdg/licence.html> (text checked 2026-10-27). Used for English glosses,
  part of speech and frequency markers. EDRDG requires apps to acknowledge the source in their
  documentation / about page and link to the licence page.
* **Chinese glosses** (`glosses/ja-zh/*.json`) were written by DAOSI from the above and are
  released under CC BY-SA 4.0 with the packs. Rank uses counts from Tatoeba sentences (CC BY 2.0 FR).

Attribution text (required; show on 数据来源与许可):

> JLPT word lists © Jonathan Waller (tanos.co.uk), CC BY, via open-anki-jlpt-decks (MIT).
> This pack uses the JMdict dictionary files, the property of the Electronic Dictionary Research
> and Development Group, used in conformance with the Group's licence
> (https://www.edrdg.org/edrdg/licence.html), CC BY-SA 4.0. Chinese glosses by DAOSI.
> Pack distributed under CC BY-SA 4.0.

## Cantonese core vocabulary — pack `vocab-yue-core`

Pack license: **CC BY-SA 4.0**. `meta.license` = "CC BY-SA 4.0 (CC-Canto, CC-CEDICT; HKCanCor CC BY 4.0)".

* **HKCanCor** (Hong Kong Cantonese Corpus) — K. K. Luke; transcriptions published at
  <https://github.com/fcbond/hkcancor> (commit `39aeadf9…`, `data/hkcancor-utf8.zip`), license
  file `data/LICENSE` = Creative Commons Attribution 4.0 International. Used for word frequency,
  part of speech and in-context Jyutping. Please cite: K. K. Luke and May L.Y. Wong (2015), The
  Hong Kong Cantonese Corpus: Design and Uses, Journal of Chinese Linguistics Monograph Series 25.
* **CC-Canto** (version 2017-02-02) and **CC-CEDICT Cantonese readings** (2015-09-23) — Pleco
  Inc., <https://cantonese.org/download.html>; file headers say "Distributed under a Creative Commons
  Attribution-Share Alike 3.0 license". BY-SA 3.0 allows adaptations under a later version with the
  same elements, so the derived pack is CC BY-SA 4.0.
* **CC-CEDICT** — MDBG, <https://www.mdbg.net/chinese/dictionary?page=cc-cedict>, file of
  2026-10-26, CC BY-SA 4.0 (stated in the file header). Used for simplified forms and English.
* **Mandarin equivalents** (`glosses/yue-zh/*.json`) were written by DAOSI, CC BY-SA 4.0. Extra
  frequency evidence from Tatoeba Cantonese sentences (CC BY 2.0 FR).

Attribution text (required):

> Cantonese word frequencies and readings from the Hong Kong Cantonese Corpus (HKCanCor) by
> K. K. Luke, CC BY 4.0. Dictionary data from CC-Canto and CC-CEDICT Cantonese readings
> (Pleco Inc., cantonese.org, CC BY-SA 3.0) and CC-CEDICT (MDBG, CC BY-SA 4.0). Mandarin
> equivalents by DAOSI. Pack distributed under CC BY-SA 4.0.

## ECDICT basic list — pack `vocab-en-basic`

Same source and license as the other English packs (ECDICT, MIT; see above). Selection uses
ECDICT's `oxford` (Oxford 3000 core flag) and `zk`/`gk` tags plus `frq`/`bnc` ranks.
