Datasheet for RefinedWeb

Dataset Composition

What are the instances?(that is, examples; e.g., documents, images, people, countries) Are there multiple types of instances? (e.g., movies, users, ratings; people, interactions between them; nodes, edges)
Each data instance corresponds to an individual web page which has been crawled, processed, and deduplicated against all other instances. 


Are relationships between instances made explicit in the data(e.g., social network links, user/movie ratings, etc.)?
N/A as there are only one kind of instances.

How many instances are there?(of each type, if ap-propriate)?
There are about 1B instances (968M individual web pages).

What data does each instance consist of? “Raw” data (e.g., unprocessed text or images)? Features/attributes? Is there a label/target associated with instances? If the instances related to people, are subpopulations identified (e.g., by age, gender, etc.) and what is their distribution?
Each instance contain the following features 
-content: the processed and cleaned text contained in the page;
-url: the url of the webpage crawled to produce the sample;
-timestamp: timestamp of when the webpage was crawled by CommonCrawl;
-dump: the CommonCrawl dump the sample is a part of;
-segment: the CommonCrawl segment the sample is a part of;
-image_urls: a list of elements in the type [image_url, image_alt_text] for all the images found in the content of the sample.

Is everything included or does the data rely on external resources? (e.g., websites, tweets, datasets) If external resources, a) are there guarantees that they will exist, and remain constant, over time; b) is there an official archival version; c) are there access restrictions or fees?
Everything is included in the datasets

Are there recommended data splits and evaluation measures? (e.g., training, development, testing; accuracy or AUC)
There are no canonical splits provided for RefinedWeb. RefinedWeb is intended to be used as a pretraining dataset for large language models. Practitioners may leverage it for upstream evaluation with a validation loss, but RefinedWeb does not provide any canonical split.


What experiments were initially run on this dataset?
To understand this dataset we ran ....

Any other comments?
N/A

Descriptive Statistics for web domains represented
