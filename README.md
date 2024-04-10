# OPENAI-API

PURPOSE:  Documentation of first experiment done on querying a panda dataframe.  PDF's used in first experiment are in Sample.PDFs.zip.  PDF's are read in, normalized, embedded and put into a database.  Then database is queried upon.  Cosine similarity can be performed and specific questions can be asked on the dataset.

METHODS:  (1).  Read PDF files in folder into reader  (2).  Create dataframe with files (unedited)  (3).  normalize texts in df   (4).  Use tokenizer to tokenize df  (5).  Embed df  (6). Query or run comparison tests on df

ISSUES:  Context window is an issue in this experiment.  I am only able to feed roughly 25 "chunks" max into a query to fit inside the context window of the chosen LLM, but the query responses are functioning correctly and giving good information.  Another issue that could possibly skew cosine similarity searches is the formatting in PDF's.  Some PDF's repeat the title, authors name, etc at the top of each page.  There are also other formatting techniques that can cause repeat words / phrases.  A method needs to be devised to consider the PDF formats and to act accordingly so that PDF formatting does not skew results.

PREREQUISITES: 

HOW TO USE:

