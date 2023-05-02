# DS5001_Final

This is the GitHub repository for my DS5001 final project.

I chose to analyze Shakespeare. 

FINAL_REPORT.ipynb contains a writeup of my findings. final_project_code_new.ipynb contains the code used to create the visualizations and analysis in the report; not every visualization in this notebook made it into the final report. In addition, certain elements were not present in the report (e.g. interactive visualization products), so be sure to examine the code as well.

Outputs of my code are:

LIB; basically a simple list of works- as there is only one author in the corpus, I did not need to include other fields besides title in this table. Metadata for the corpus.

CORPUS; a list of tokens, organized by OHCO (so each token fits under a book ID, act number, scene number, sentence number, and token number. Each token has an assigned part of speech. This table was parsed by NLTK.

VOCAB; a bag of unique words across the set of works, organized by use in descending order. Each word is encoded as a row, and fields for each row include: number of times used (n), frequency of times used (p), perplexity (i; calculated as 
, length of word in number of characters, most likely part of speech, word stem from three different stemmers (reduces derived words to a common stem), whether the word is a stop word (words such as "the", "and", etc. that can be omitted from many tasks), and all TFIDF values.

PAIRS; a list of each work compared to each other work by similarity, using various clustering algorithms. This data is also visualized in dendrograms in the notebook.

TOPICS_plays; a matrix of each work and each topic, which shows each play's association probability with each topic.

LOADINGS; a list of 1000 terms (limited to 1000 in the interest of reducing computational cost) that maps words and their relationship to principal components. Principal components are the components calculated to have the greatest variance for the text. Put simply, these components "explain differences" in the text best.

EMBEDDINGS; the VOCAB table of terms, with associated emotional embeddings added, for: anger, anticipation, disgust, fear, joy, sadness, surprise, trust.

Please enjoy.
