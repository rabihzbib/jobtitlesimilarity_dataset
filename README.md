# Job Title Text Ranking Evaluation Dataset

This repository includes the evaluation dataset used in the text ranking experiments reported in the paper *Learning
Job Titles Similarity from Noisy Skill Labels* by Rabih Zbib et al. [[*]](link_to_arxiv). 

The task involves ranking a set of job titles, given another job title as query, such that the resulting ranking
reflects the semantic similarity of each job title to the query. To build the dataset, we started with 2,724 job titles
(short text phrases with the name of an occupation). After a minimal pre-processing, including clean-up and
lower-casing, we randomly divided the job titles into two groups: 105 job titles were used as queries, and the remaining
as corpus documents. Each query/document pair was labeled for binary relevance after adjudicating two independent
human annotations. (The inter-annotator agreement for this binary relevance labels was 86%.) 

The result is a dataset composed of the following files:

 - **corpus_documents.tsv**: includes the mapping between `corpus_document_id` to the text form of each job title in
                             the corpus.
 - **queries.tsv**: includes the mapping between `query_id` to the text form of each query job title.
 - **annotations.tsv**: includes the binary relevance annotations between. Only the relevant pairs are included, and the
                        file is formatted in the format required by `trec_eval` software library.


