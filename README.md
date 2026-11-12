# The Great Comet of 1811 in Metropolitan Serial Print: A Bibliographical Corpus, 1811–1812

**Dataset DOI:** [10.5281/zenodo.24146585](https://doi.org/10.5281/zenodo.24146585)  
**Version:** 1.0  
**Creator:** Deguang Li, University of Cambridge  
**Scope:** 289 publication instances in 13 London metropolitan serial titles, 30 July 1811–1 December 1812.  
**Contents:** Bibliographical metadata only; no OCR transcriptions or page images.

## Project overview

This dataset accompanies research into the production, circulation and classification of cometary knowledge in early nineteenth-century metropolitan print culture. It provides a source-based foundation for investigating how different forms of knowledge, including those characterised as superstitious, were represented and contested across newspapers and periodicals. The corpus is organised bibliographically rather than according to the interpretative categories of the accompanying research, allowing the records to support other questions and approaches.

## Files

- `corpus.csv` — one row per recorded historical publication instance (289 records).
- `serials.csv` — one row per serial title, with source-attributed and date-qualified historical context.
- `README.md` — methodology, corpus profile, field definitions, bibliographical conventions, limitations and citation guidance.
- `LICENSE` — CC BY 4.0 scope and third-party rights qualifications.

## Collection and selection

The researcher used an extensive search strategy intended to recover relevant items discoverable through accessible digitised holdings, principally the British Newspaper Archive, Gale and Google Books. Searches centred on variant forms of *comet*, rather than on interpretative terms such as *superstition*. Retrieved results were manually screened to exclude OCR false positives, and inspection of related newspaper columns identified additional items missed by keyword retrieval. The corpus therefore reflects an extensive, historically informed retrieval process rather than a mechanically reproducible search protocol.

The target is the Great Comet first observed in March 1811 (C/1811 F1), not the distinct comet discovered by Flaugergues in December 1811. Any reference to the target comet was eligible, including observations, correspondence, satire, religious commentary, advertisements, entertainment notices and retrospective accounts.

A **publication instance** denotes a distinct item or identifiable textual occurrence within a serial publication, not an entire issue or a database search result. Multiple distinct items within the same issue may therefore be recorded separately. Multiple digital records of the same historical appearance in the same issue were consolidated, while appearances in different issues or publications were retained.

The corpus is **not** presented as a census of all surviving metropolitan serial print. Uneven digitisation, OCR performance, database access and the absence of a page-by-page coverage audit limit claims to completeness. The date range describes the records collected, not a verified historical first or last mention or an exhaustive chronological search window.

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

- **Publication year:** 1811: 240 instances; 1812: 49 instances.
- **Recorded source platform:** British Newspaper Archive: 116; Gale: 98; Google Books: 75.
- **Page locators:** 196 records have a recorded page locator; 93 do not (all from Gale). Missing locators do not imply that the original issues were unpaginated.

The number of instances per serial is **not** an exposure-adjusted publication rate. Issue frequency, digitised coverage, search recall, genre and publication duration vary between titles. These counts should not be used on their own to infer audience size or relative public interest.

## Historical serial context

`serials.csv` draws on the researcher's compiled notes from *The Waterloo Directory of English Newspapers and Periodicals, 1800–1900* (WDEND) and the *Dictionary of Nineteenth-Century Journalism in Great Britain and Ireland* (DNJ). It supplies short, source-attributed paraphrases rather than reproducing the reference works' entries. Descriptors retain qualifications where evidence is specific to a particular date or period, or where historical circumstances are ambiguous.

Examination of dated issues establishes that *La Belle Assemblée* appeared monthly and the *London Chronicle* three times weekly in 1811. Other ambiguous or historically changing publication frequencies are qualified in `serials.csv`. Political descriptions reflect the terminology of the reference sources and do not imply uniformity across articles, contributors or readers. Evidence of an intended readership is not evidence of actual readership; blank fields indicate that the compiled sources do not provide sufficient evidence. Circulation figures are omitted because comparable, securely dated figures for 1811 have not been established across the thirteen titles.

## Data dictionary

### `corpus.csv`

- `instance_id`: Stable local identifier for a publication instance (not a repository DOI).
- `publication_title`: Researcher-normalised serial title; joins to `serials.csv` on this field.
- `publication_date`: Date recorded for the historical appearance (ISO `YYYY-MM-DD`).
- `heading_as_recorded`: Identifying heading or opening words entered by the researcher; not necessarily a verbatim printed article title.
- `byline_as_recorded`: Byline as recorded in the researcher's source data.
- `byline_descriptor_verbatim`: Descriptor recorded alongside the byline, without assigning it to a fixed category (it may refer to occupation, location, institution or another attribute).
- `page_as_recorded`: Page locator where available.
- `source_platform`: Digital platform through which the item was consulted or recorded.
- `source_url`: Link to the consulted digital source, which may identify an item, newspaper page, issue or bound volume rather than an individual article.

### `serials.csv`

- `publication_id`: Local identifier for a serial title.
- `publication_title`: Normalised title matching `corpus.csv`.
- `instance_count`: Number of publication instances in this corpus.
- `directory_entry_title`: Directory headword or title, as compiled in the researcher's notes.
- `frequency_c1811`: Publication frequency around 1811 where supported by the available evidence; qualifications retained where necessary.
- `editorial_orientation_c1811`: Source-attributed editorial or political descriptor, not a uniform party classification.
- `intended_readership_evidence`: Evidence concerning intended readership, not a measurement of actual readership.
- `editor_or_proprietor_c1811`: Named editor or proprietor where supported by the compiled directory information.
- `directory_source`: Reference work or works used for the descriptor.
- `directory_reference`: Pointer to the researcher's directory notes and, where available, a DNJ page; consult the underlying reference work for formal citation.
- `context_note`: Historical qualifications and guidance for interpreting the entry.

## Bibliographical conventions and source interpretation

**Headings.** `heading_as_recorded` is an identifying label. Depending on the source, it may reproduce a printed article heading, a column heading or opening words supplied by the researcher. It should not automatically be treated as a verbatim title.

**Dates.** *London Chronicle* issues carried date ranges, while individual pages could display dates within those ranges. The corpus retains dates as recorded rather than normalising them to the newspaper's usual Tuesday, Thursday and Saturday publication days. Researchers needing to distinguish precisely between issue dates, page dates and article datelines should consult the linked source volumes.

**Links and repeated entries.** A source link may legitimately occur in more than one record: Google Books links may identify a bound volume, while BNA links may identify a newspaper page containing several items. Likewise, a publication, date and generic heading may coincide for distinct items. Neither identical URLs nor identical generic headings alone establish that two records are duplicates.

**Page references.** Page numbers are supplied where recorded. The absence of a page locator in the dataset should not be interpreted as evidence that the historical source lacked pagination.

## Rights, reuse and future releases

This release contains **bibliographical metadata only**. Its original compilation and documentation are provided under the terms described in `LICENSE` (CC BY 4.0, insofar as the creator holds the relevant rights). The licence does not grant rights in third-party material. Underlying historical works, digital collections and database-derived content may be subject to separate copyright, database rights or access agreements. This release does not include, or authorise redistribution of, OCR text or facsimile images from the British Newspaper Archive, Gale or Google Books.

The dataset is a pilot release from a wider doctoral research corpus containing more than 1,200 primary-source entries. Future work may extend the open bibliographical metadata to that larger corpus and, subject to applicable rights and permissions, make independently prepared and checked full-text transcriptions and additional structured data available. These are prospective extensions, not contents of version 1.0.

## Citation

Li, Deguang. 2026. *The Great Comet of 1811 in Metropolitan Serial Print: A Bibliographical Corpus, 1811–1812*. Version 1.0. Dataset. Zenodo. [https://doi.org/10.5281/zenodo.24146585](https://doi.org/10.5281/zenodo.24146585).

For claims about the historical characteristics of individual serials, researchers should also consult and cite the relevant directory sources identified in `serials.csv`.
