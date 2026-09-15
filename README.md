# SpeakTheWord — Bible databases

The SQLite databases the **SpeakTheWord** app downloads on request. Nothing here
is application code; this repository exists only so the app can fetch these
files from a plain, unauthenticated URL.

The app ships with two Bibles so that it works on first launch with no network.
Everything else lives here, because together these files are larger than the
rest of the app put together.

## Releases

Each release carries the databases as assets. The app requests them by version,
so a rebuilt database can be offered to devices already holding an older copy.

## Sources and licences

| file | text | source | licence |
|---|---|---|---|
| `wlc.db` | Westminster Leningrad Codex, with Strong's tagging | [Open Scriptures](https://github.com/openscriptures/morphhb) | CC BY 4.0 |
| `tagnt.db` | Translators Amalgamated Greek New Testament | [STEPBible](https://github.com/STEPBible/STEPBible-Data), Tyndale House Cambridge | CC BY 4.0 |
| `strongs.db` | Strong's Concordance (1890) | [Open Scriptures](https://github.com/openscriptures/HebrewLexicon) | public domain; packaging CC BY 4.0 |
| `lxx.db` | Septuagint (Brenton, 1851), with Strong's tagging | text public domain; tagging from [LXX-Rahlfs-1935](https://github.com/eliranwong/LXX-Rahlfs-1935) by Eliran Wong, derived from CATSS (R. Kraft and E. Tov, University of Pennsylvania) | tagging **CC BY-NC-SA 4.0** |

### A note on the Septuagint tagging

Strong's numbers for the Septuagint exist only as a word-position index into
**Rahlfs 1935**. The text here is **Brenton 1851** — a different edition, 53,169
words apart. The numbers are therefore attached by matching **letters**, not
positions: a word carries a number only where both editions print the same word.
Roughly 86% of words are tagged and the rest carry nothing. Ten books whose
editions diverge too far carry no tagging at all.

The CATSS materials this derives from are distributed under terms requiring
non-commercial use and acknowledgement of the copyright holder, the encoder and
the source. Both are observed here and in the app.
