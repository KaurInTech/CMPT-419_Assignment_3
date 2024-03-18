
Datasheet for Dolma

What are the instances? Are there multiple types of instances?
Instances are plain-text spans on English text or computer code. Each instance was obtained by
processing web pages (which might include news, documents, forums, etc), academic articles,
computer code from GitHub, encyclopedic content from Wikipedia, or Project Gutenberg books.

Are relationships between instances made explicit in the data?
Metadata for subsets of Dolma could be used to reconstruct relationships between items:
• Common Crawl. Each document uses the URL of the web page from which it was extracted as its
identifier; therefore, it can be used to identify relationships between documents.
• C4. The URL of each web page from which documents were extracted is included as metadata;
therefore, it can be used to identify relationships between documents.
• Reddit. The originating subreddits and thread ids of documents are included in the metadata.
• peS2o. The id of each document is the Semantic Scholar Corpus ID of its corresponding manuscript.
Metadata for each manuscript can be obtained using the Semantic Scholar APIs (Kinney et al.,
2023).
• The Stack. The name of the GitHub repository each document belongs to is included as metadata.
• Project Gutenberg. The title of each book is included as the first line of each document.
• Wikipedia, Wikibooks. For both, metadata includes the URL corresponding to the page content
was extracted from. Structure and connections between documents can be recovered through the
URL.

How many instances of each type are there?
Summary statistics are reported in table below:





What data does each instance consist of? “Raw” data (e.g., unprocessed text or images)?
Features/attributes?
For each source, raw data is not available directly but could be recovered using source-specific
methods:
• Common Crawl. We obtain data from common crawl snapshots from 2020-05 to 2023-06. WARC
files from Common Crawl can be intersected with Dolma ids to recover original HTML files.
• C4. We obtained this corpus from the HuggingFace Hub 33. In turn, documents in C4 have been
derived from a Common Crawl snapshot for 04/2019. URLs in C4 can be used to recover HTML
files.
• Reddit. The complete set of monthly data dumps used in this work are no longer distributed by
Pushshift, however they can still be obtained through torrents and some public web archives.
• peS2o. peS2o is derived from S2ORC Lo et al. (2020). Original parsed documents can be obtained
from extracting documents in S2ORC that share the same ID with peS2o. Further, metadata in
S2ORC can be used to obtain original PDF.
• The Stack (deduplicated). The filename and repository name, both available in metadata, can be
used to recover original file contents.
33https://huggingface.co/datasets/allenai/c4
53
• Project Gutenberg. The title of each book is the first line of each document.
• Wikipedia, Wikibooks. For both, metadata includes the URL corresponding to the page content
was extracted from. Structure and connections between documents can be recovered through the
URL.


Is there a label/target associated with instances? If the instances are related to people, are
subpopulations identified (e.g., by age, gender, etc.) and what is their distribution?
There are no labels associated with instances. Many text instances were likely created by people or
groups of people, but in the vast majority of cases authorship information is unavailable let alone
subpopulation metadata. we leave aggregation and reporting of these statistics to future work.

Is everything included or does the data rely on external resources? (e.g., websites, tweets,
datasets) If external resources, a) are there guarantees that they will exist, and remain constant,
over time; b) is there an official archival version. Are there licenses, fees or rights associated
with any of the data?
The data are derived from the web and the original resources may not persist over time. However,
each source represents an archival snapshot of that data that should remain fixed and available:
• Common Crawl. The Common Crawl data is available on Amazon S3 as part of the Amazon
Web Services’ Open Data Sponsorship program and can be freely downloaded 34. We followed
Common Crawl terms of use35
• C4. This corpus can be obtained from from the HuggingFace Hub33 and is released under ODC-By
1.0 (Open Data Commons, 2010).
• Reddit. Pushshift no longer distributes this dataset due to changes to the Reddit API’s terms.
Unofficial copies of the data might be be available through torrents and some public web archives.
Pushshift data dumps inherit36 the Terms of use of the Reddit API at the time of their collection
(March 2023).
• peS2o. peS2o is derived from S2ORC Lo et al. (2020). S2ORC is released through the Semantic
Scholar Public API37 under ODC-By 1.0 (Open Data Commons, 2010).
• The Stack (deduplicated). The corpus is available on the HuggingFace Hub 38 and consists of
code released under a variety of permissive licenses. More details including terms of use for
hosting or sharing the corpus are provided in the datacard at the link above.
• Project Gutenberg. Project Gutenberg consists of books that are not protected under U.S.
copyright law. The corpus is available at gutenberg.org.
• Wikipedia, Wikibooks. Wikimedia data dumps are freely available39 and released under CC
BY-SA 4.0 license (Creative Commons, 2013).

Are there recommended data splits or evaluation measures? (e.g., training, development,
testing; accuracy/AUC)
No. A separate evaluation suite Dolma as been decontaminated against will be released at a later date.
Downstream users of this dataset could use any alternative evaluation suite.

What experiments were initially run on this dataset? Have a summary of those results and, if
available, provide the link to a paper with more information here.

Descriptive statistics describing a feature of interest
