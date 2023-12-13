## Note:
Aside from the CysticFibrosis collection, all of the original files (and some explanations) are available at http://ir.dcs.gla.ac.uk/resources/test_collections/.

## Collection Statistic Summary
| Collection     | Total Documents | Total Queries | Total QRels |
|----------------|-----------------|---------------|-------------|
| ADI            | 82              | 35            | 170         |
| CACM           | 3204            | 64            | 796         |
| CISI           | 1460            | 112           | 3114        |
| Cranfield      | 1400            | 225           | 1837        |
| CysticFibrosis | 1239            | 100           | 4819        |
| LISA           | 5999            | 35            | 344         |
| Medline        | 1033            | 30            | 696         |
| NPL            | 11429           | 93            | 2083        |
| Time           | 423             | 83            | 324         |

### CysticFibrosis Collection Disclaimer:
There were a few issues with the original files, mostly to do with encoding. These were manually altered before parsing.
- cf74: line 6860 had some unreadable characters, so I filled in the blanks (I believe I found the original abstract/extract).
- cf74: line 9554 (the final line) was all garbage so I removed it, doing so did not alter the total documents counted.
- cf75: line 11739 had the same issue as above.
- cf79 line 13622 also had this issue.
- cf79 lines 9120-9144 were formatted to fit the rest of the documents, but the contents were not changed.

In addition, the assessments for this dataset come in the form: 0012, where each score is from a different group of assessors, 0 is not relevant, 1 is slightly relevant, and 2 is very relevant. For our purposes, partially because the even number doesn't lend well to a majority vote, if any assessor deemed a document to be relevant, we take it to be so.

### Time Collection Disclaimer:
Each original document is headed with a line: `*TEXT DOCID DATE PAGENUM`, starting at TEXT017 and ending at TEXT563, with various gaps in the numbering (e.g. there is no 022, 041, 044, 073-081). However, the assessments do not reference any document with an ID over 425, but do reference documents with an ID under 17. Thus, one would assume that the documents have simply been numbered as they were found. Yet, the corresponding README claims there are 425 total documents, which does line up with the numbering found in the assessments, although we only found 423 total.

Our solution is to simply number the documents as we find them, and leave the assessments as they are.
