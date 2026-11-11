# The Great Comet of 1811 in Metropolitan Serial Print: A Bibliographical Corpus, 1811–1812

**Creator:** Deguang Li  
**Version:** 1.0 release candidate (not yet deposited; 11 November 2026)  
**Scope:** 289 publication instances in 13 London/metropolitan serial titles, 30 July 1811–1 December 1812.  
**Contents:** bibliographical metadata only; no OCR transcriptions or page images.

## Files
- `corpus.csv` — one row per historical publication appearance (289 records).
- `serials.csv` — one row per serial title, with *source-attributed and date-qualified* contextual information from the researcher's directory notes.
- `README.md` — methodology, corpus profile, field definitions, limitations and citation guidance.
- `LICENSE` — CC BY 4.0 scope and third-party rights qualifications.

## Collection and selection
The researcher used an extensive search strategy intended to recover all relevant items discoverable through accessible digitised holdings, principally the British Newspaper Archive, Gale and Google Books. Search queries centred on fuzzy variants of **comet**, rather than on interpretive terms such as **superstition**. Results were manually screened to eliminate OCR false positives; inspection of related newspaper columns identified some items missed by keyword retrieval. The target is the Great Comet first observed in March 1811 (C/1811 F1), **not** the distinct comet discovered by Flaugergues in December 1811. Any mention of the target comet was eligible, including observation, correspondence, satire, religious commentary, advertising, entertainment and retrospective notices. Multiple digital records of the same appearance in the same issue were consolidated; genuine appearances in different issues or publications were retained.

The corpus is **not** claimed as a census of all surviving metropolitan serial print. Uneven digitisation, OCR performance, database access and the absence of a page-by-page coverage audit limit completeness claims. The 1811–1812 dates describe *the collected records*, not a verified historical first/last mention or a documented exhaustive chronological search window.

## Corpus profile

| Serial title | Instances | Share |
| --- | ---: | ---: |
| Morning Chronicle | 50 | 17.3% |
| Globe | 48 | 16.6% |
| Morning Post | 43 | 14.9% |
| London Chronicle | 34 | 11.8% |
| Monthly Magazine | 26 | 9.0% |
| London Courier and Evening Gazette | 24 | 8.3% |
| Bell's Weekly Messenger | 23 | 8.0% |
| General Chronicle and Literary Magazine | 11 | 3.8% |
| Evening Mail | 9 | 3.1% |
| Examiner | 9 | 3.1% |
| La Belle Assemblée, or, Bell's Court and Fashionable Magazine Addressed Particularly to the Ladies | 5 | 1.7% |
| National Register Sunday And Monday Newspaper | 4 | 1.4% |
| Anti-Gallican Monitor | 3 | 1.0% |
| **Total** | **289** | **100%** |

- Publication year: 1811 = 240; 1812 = 49.
- Discovery/source platform recorded: Google Books = 75, British Newspaper Archive = 116, Gale = 98.
- **196 records** have page locators; **93** have no recorded page number (all Gale). This does not establish that the original issues lacked pagination.
- `heading_as_recorded` is an identifying label that may reproduce a printed heading, column heading or researcher-supplied opening words; it should not automatically be treated as a verbatim article title.
- The number of corpus hits per serial is **not** an exposure-adjusted publication rate. Issue frequency, digitised coverage, search recall, genre and publication duration vary across serials. Do not infer audience size or relative public interest from these counts.

### Historical serial context
`serials.csv` uses the researcher's `Workbook2.xlsx`, which compiles entries from *The Waterloo Directory of English Newspapers and Periodicals, 1800–1900* (WDEND) and the *Dictionary of Nineteenth-Century Journalism in Great Britain and Ireland* (DNJ). It reports short, paraphrased, date-qualified descriptors rather than reproducing the reference works' extensive entries. The historical descriptors are derived from the researcher’s compiled directory notes; they are not a systematic independent re-verification of every directory entry. Two publication frequencies have been separately verified by the researcher against dated issues: *La Belle Assemblée* (monthly) and *London Chronicle* (thrice weekly). The monthly frequency of *La Belle Assemblée* is also supported by the Wellcome Collection catalogue. Other ambiguous or historically varying frequencies remain qualified. Political descriptions reflect directory terminology and do not imply uniformity of all articles, writers or readers. Intended readership and observed readership are distinct; blanks indicate insufficient evidence. Circulation numbers are omitted because comparable, securely dated 1811 figures have not been established across the 13 titles.

## Data dictionary

### `corpus.csv`
- `instance_id`: Stable local record identifier (not a repository DOI).
- `publication_title`: Researcher-normalised serial title; link to `serials.csv` on this field.
- `publication_date`: Date of this recorded publication appearance (ISO YYYY-MM-DD).
- `heading_as_recorded`: Identifying heading or opening words as entered by the researcher; not necessarily a printed article title.
- `byline_as_recorded`: Byline as recorded in source workbook.
- `byline_descriptor_verbatim`: Unclassified suffix printed with the byline (may denote occupation, location, institution, etc.).
- `page_as_recorded`: Page locator where recorded.
- `source_platform`: Digital platform through which the item was recorded.
- `source_url`: Original recorded link; not necessarily a permanent article-level URL.

### `serials.csv`
- `publication_id`: Local serial ID.
- `publication_title`: Normalised title matching `corpus.csv`.
- `instance_count`: Count of publication appearances in this corpus.
- `directory_entry_title`: Directory headword/title (short form, as compiled by researcher).
- `frequency_c1811`: Publication frequency near 1811 where source supports it; uncertainty explicitly noted.
- `editorial_orientation_c1811`: Source-attributed editorial or political descriptor, not an inferred uniform party identity.
- `intended_readership_evidence`: Only explicit intended-audience evidence; not actual audience measurement.
- `editor_or_proprietor_c1811`: Named person only where directory note provides support.
- `directory_source`: Reference works used by the researcher.
- `directory_reference`: Pointer to workbook row and DNJ page where available; not a substitute for a verified bibliographical citation.
- `context_note`: Limitations and reading guidance.

## Rights, reuse and future releases
This is a metadata-only research release. The underlying historic works may be public domain, but database access agreements and the rights in database-derived content must be assessed separately. Do not treat the present file as permission to reproduce BNA, Gale or Google Books full-text OCR or facsimiles. The source directory entries in WDEND and DNJ are **not** republished; only limited source-attributed paraphrases are supplied. A separate rights review is underway for full-text transcriptions.

## Citation
**Before DOI assignment:** Li, Deguang. *The Great Comet of 1811 in Metropolitan Serial Print: A Bibliographical Corpus, 1811–1812*. Version 1.0 (2026), release candidate. Upon publication, cite the Zenodo version DOI. The directory reference works should also be consulted and cited for specific contextual claims.

## Bibliographical verification notes
- The *Monthly Magazine* entry “Power, A Political Essay” (COM1811-0248) now records p. 568, supplied and verified by the researcher; the page has not been independently checked against the digitised volume.
- Google Books volume URLs with an accidental trailing full stop were normalised (15 records); this is a URL syntax correction, not independent confirmation of live access.
- A link may legitimately recur across multiple records: Google Books often links to a whole bound volume, and BNA links may identify a shared newspaper page. Identical URLs do not establish duplicate historical items.
- *London Chronicle* issues were dated over ranges, and individual pages could display dates within those ranges, as confirmed by the researcher from bound volumes. Consequently, recorded dates need not coincide with the usual Tuesday/Thursday/Saturday publication days. The corpus retains the researcher-recorded dates without normalising them to issue publication days; individual date provenance (page heading versus issue range versus article dateline) has not been verified for all records.

- *La Belle Assemblée* is monthly in 1811: verified by the researcher from the 1811 monthly issues, and consistent with the Wellcome Collection catalogue (https://preview.wellcomecollection.org/works/mhayfztk).
- *London Chronicle* is thrice weekly in 1811: verified by the researcher from Google Books digitised bound volumes. The directory entry lists other frequencies for different periods, which must not be projected onto 1811.
- The catalogue retains separate historical appearances even where publication, date and generic headings match. Such matches alone do not establish duplicate records.

### Date and locator audit (internal consistency; not source-image verification)
- 289 unique instance identifiers, 289 non-empty source links, and 13 matching serial titles.
- 196 page locators are recorded, including p. 568 for “Power, A Political Essay” (supplied by the researcher); 93 Gale records lack page locators.
- The 34 *London Chronicle* records include 11 dates falling on Mondays (5), Wednesdays (2) or Fridays (4). These are **not classified as errors**: the newspaper used multi-day issue ranges and individually dated pages. The stored date field is not guaranteed to represent a nominal issue-publication day. Any finer distinction requires inspection of the particular page.
- Several same-title/same-date records and shared BNA page URLs require item-level verification; none were automatically merged.
- Links are supplied as recorded source pointers; some identify bound volumes or newspaper pages rather than individual articles. Link presence is not a claim that every destination has been independently tested.

## Zenodo deposit preparation
- Recommended record type: Dataset; creator: Deguang Li; version: 1.0 for the first public release (this package is a release candidate, not a published deposit).
- Deposit the four files individually, not only a ZIP, to enable inspection. Reserve a DOI while preparing the draft, then insert the assigned DOI into the README before publication.
- Select CC BY 4.0 only after confirming that it is appropriate for the original compilation and documentation, while retaining third-party rights qualifications in LICENSE. The repository license selection does not override third-party rights.
- A Zenodo draft is not yet a published, citable deposit. Future material changes should normally be released as a new version with its own version DOI.

## Known limitations and future improvements
Possible future improvements include additional page references for Gale records, closer identification of printed headings versus opening words, and item-level checks of dates and source locators. These are limitations of bibliographical precision, not indications that the 289 publication appearances were accepted without manual relevance screening.

## Publication status
This is a **pre-deposit release candidate**. No DOI has been assigned and no repository publication has occurred. The researcher should check any embedded access tokens in source URLs before public release and confirm that the platform terms permit public redistribution of the compiled metadata.
