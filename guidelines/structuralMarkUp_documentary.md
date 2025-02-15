# Mark up of structural sections for articles published in Pylon

See also: [StructureFilesXML](https://docs.google.com/spreadsheets/d/1HaacsPU44Rm4qXWzguBxXorc9F1S3N9HDxpgp-c9kHU/edit#gid=0), where, in the form of a googlespreadsheet, the information is presented in rows and columns with further detail concerning Xpaths.

In the relevant [XSLT file](https://github.com/hcayless/P3-processing/blob/main/xslt/process-tei.xsl#L12-L14) in [P3-processing](https://github.com/hcayless/P3-processing) the list of these individual variable names can be found.

## For every article
### Title, author, affiliation, email and acknowledgement
- #articleTitle
  - Title of the article

- #author
  - Surname comma Forename(s)
  - Surname comma Forename(s)
  
- #affiliation
  - Institute for the Study of the Ancient World (no standardisation, simply a string)
  
- #email
  - mksmi@gmail.com

- #acknowledgement
  - For acknowledging publication permission, thanking others for their contributions (this deals with the * which is often found as a marker for the first footnote in print publications)

Here is an **example of such mark up** as used to produce one of our test files:

- To help towards the production of this [C.M. Sampson, “P.Hamb.graec. 185: Garden Tax Between the Archives of (Lucius) Iulius Serenus and Gemellus Horion,” Pylon 1 (2022)](https://journals.ub.uni-heidelberg.de/index.php/pylon/article/view/89345/84255)
  - the stuctural mark up of the word document can be seen [here](https://github.com/jcowey/P3/files/9402332/TitleAuthorAckn.pdf)


## For each and every separate DDB text edited in the article: DOCUMENTARY texts
### Metadata, papyrological header, introduction, text, translation and commentary
- #editionDDB
- #metadata
  - Create a table for the categories that are to be supplied
    - For a list of the categories of metadata see [here](https://github.com/jcowey/P3/blob/master/guidelines/metadataMask.md)

- #papyrologicalHeader:
  - Title (if there is one)
  - Create a table (usually 2 rows and 3 columns) in the word document for the date, measurements, provenance, inventory number, etc

- #introduction
  - Running text in paragraphs

- #text
  - Leiden+ (of the text)
  
- #translation
  - Leiden+ (of the translation)
  
- #commentary
  - Running text in paragraphs

Here is an **example of such mark up** as used to produce one of our test files:

- [Claytor Smith Warga BASP 53 text 2](https://digi.ub.uni-heidelberg.de/editionService/viewer/text/p3test/ClaytorSmithWarga_FourPoll_TaxReceiptsTrial_5#ch_7)
  - for which the stuctural mark up of the word document was [ClaytorSmithWargaText2.pdf](https://github.com/jcowey/P3/files/8080721/ClaytorSmithWargaText2.pdf)

## For each and every separate DCLP text edited in the article: LITERARY texts
### Metadata, papyrological header, introduction, text, translation and commentary
- #editionDCLP
- #metadata
  - Create a table for the categories that are to be supplied
    - For a list of the categories of metadata see [here](https://github.com/jcowey/P3/blob/master/guidelines/metadataMask.md)

- #papyrologicalHeader:
  - Title (if there is one)
  - Create a table (usually 2 rows and 3 columns) in the word document for the date, measurements, provenance, inventory number, etc

- #introduction
  - Running text in paragraphs

- #text
  - Leiden+ (of the text)
  
- #translation
  - Leiden+ (of the translation)
  
- #commentary
  - Running text in paragraphs

Here is an **example of such mark up** as used to produce one of our test files:

- [Lougovaya Cubits](https://digi.ub.uni-heidelberg.de/editionService/viewer/text/p3test/Lougovaya_cubits_and_fingers#ch_17)
  - for which the stuctural mark up of the word document was: [pHarris50.pdf](https://github.com/jcowey/P3/files/7655522/pHarris50.pdf)


## For every section header in the article
### Any subheadings in the article, any quoted passages, corrections made to existing texts and bibliography
- #articleHeader
  - To be used whenever there are section headings within the article

- #blockQuote / #endBlockQuote
  - To be used whenever a section of text (Greek or otherwise) is quoted from an external source and should be displayed separately as a quote
    - e.g. https://github.com/jcowey/P3/blob/master/pylon/testFiles/ClaytorSmithWarga/ClaytorSmithWarga_FourPoll_TaxReceiptsTrial_4.xml#L321-L325
      - in this case please remember to indicate the end of the block quote by placing #endBlockQuote at the end of the quoted section.

- #corrections
  - whenever there are corrections to existing texts, in tabular form

- #bibliography
  - if a bibliography is included

Here is an **example of such mark up for #articleHeader and #blockQuote** as used to produce one of our test files:

- To help towards the production of this [Claytor Smith Warga BASP 53](https://digi.ub.uni-heidelberg.de/editionService/viewer/text/p3test/ClaytorSmithWarga_FourPoll_TaxReceiptsTrial_5#ch_23)
  - the stuctural mark up of the word document was: [articleHeader_and_blockQuote.pdf](https://github.com/jcowey/P3/files/7654312/articleHeader_and_blockQuote.pdf)

Here is an **example of such mark up for #corrections** as used to help towards the implementation of this correction in papyri.info in the correct text there. This does not appear in the HTML / PDF version of the text.
- the stuctural mark up of the word document was: [correctionsClaytorWargaSmith.pdf](https://github.com/jcowey/P3/files/8080777/correctionsClaytorWargaSmith.pdf)

Here is an **example of such mark up for #bibliography** as used to produce one of our test files:

- To help towards the production of this [Schubert Liturgy](https://digi.ub.uni-heidelberg.de/editionService/viewer/text/p3test/schubert_liturgy_geography#ch_9)
  - the stuctural mark up of the word document was: [biblioSchuber.pdf](https://github.com/jcowey/P3/files/7655474/biblioSchuber.pdf)
