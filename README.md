# Dignose This If You Can 
###On the effectiveness of search engines in finding medical self-diagnosis information


Data related to the paper "Diagnose This If You Can: On the effectiveness of search engines in finding medical self-diagnosis information", by [G. Zuccon](http://www.zuccon.net/), [B. Koopman](http://koopman.id.au/), [J. Palotti](http://joaopalotti.com/), ECIR 2015.

### What does this research show?
In this work, we examined poorly formulated self-diagnosis queries and we found that major search engines were providing irrelevant information that could lead to incorrect self-diagnosis, self-treatment and ultimately possible harm.


### What is in this repository?

* ecir2015\_circumlocation\_health\_search.pdf: pre-print of the paper published at ECIR 2015.

* ecir2015\_poster.pdf: the poster of the paper that was presented at the ECIR 2015 conference.

* queries.txt: the file containing the queries that were used in the evaluation described in the paper. The file is tab separated and contains the query id, the true condition, and the actual query. This format can be directly used with [Relevation](https://github.com/ielab/relevation).

* bingresults.txt: a [TREC style result file](http://faculty.washington.edu/levow/courses/ling573_SPR2011/hw/trec_eval_desc.htm) containing the results returned by Bing (using the official Bing API) in answers to the queries used in the paper.

* googleresults.txt: a [TREC style result file](http://faculty.washington.edu/levow/courses/ling573_SPR2011/hw/trec_eval_desc.htm) containing the results returned by Google (using the deprecated Ajax API) in answers to the queries used in the paper.

* qrels.ecir2015.txt: relevance assessments in [TREC format](http://faculty.washington.edu/levow/courses/ling573_SPR2011/hw/trec_eval_desc.htm) for the queries and result files used in this work.

* id2url-mapping: mappings from document identifiers (in the format 1.txt, 2.txt etc.) to URLs of the web pages retrieved by the two search engines. For more detials, see the notes below.

### Notes

* Result files are in TREC format. This means that TRECeval can be directly used with these result files. For more information about the TREC result file format, see [these notes about TRECeval](http://faculty.washington.edu/levow/courses/ling573_SPR2011/hw/trec_eval_desc.htm).

* Webpages were not crawled; rather, we recorded the link to the webpages the search engines provided and then fetched (but not stored) the pages to show to the relevance assessors using Relevation.

* TRECeval results and qrels format does not allow the use of URLs as document identifier. This is why we had to create a mapping that allows to assign a document id (e.g. 1.txt) to an URL. These mappings are contained in the folder id2url-mapping. Note that each mapping corresponds to one file; this is because in this way [Relevation](https://github.com/ielab/relevation) could be used to directly load these mappings and automatically fetch the corresponding webpage (with a minor modification to Relevation's source code).


### Other information about this work
See the [dedicated webpage](http://zuccon.net/diagnose-this.html) for this work, which provides further details, FAQs, media coverage and follow up.