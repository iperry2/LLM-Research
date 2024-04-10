# OPENAI-API

PURPOSE:  Documentation of first experiment done on querying a panda dataframe.  PDF's used in first experiment are in Sample.PDFs.zip.  PDF's are read in, normalized, embedded and put into a database.  Then database is queried upon.  Cosine similarity can be performed and specific questions can be asked on the dataset.

METHODS:  (1).  Read PDF files in folder into reader  (2).  Create dataframe with files (unedited)  (3).  normalize texts in df   (4).  Use tokenizer to tokenize df  (5).  Embed df  (6). Query or run comparison tests on df

ISSUES:  Context window is an issue in this experiment.  I am only able to feed roughly 25 "chunks" max into a query to fit inside the context window of the chosen LLM, but the query responses are functioning correctly and giving good information.  Another issue that could possibly skew cosine similarity searches is the formatting in PDF's.  Some PDF's repeat the title, authors name, etc at the top of each page.  There are also other formatting techniques that can cause repeat words / phrases.  A method needs to be devised to consider the PDF formats and to act accordingly so that PDF formatting does not skew results.

OUTPUT FROM EXPERIMENT 1:

    index                                               text  text_len  n_tokens                                             ada_v2  similarity
0      89  Springer Nature 2021 L ATEX template 6 AI to a...      2064       435  [-0.01664821244776249, 0.011838872916996479, 0...    0.432164
1     136  A.1 Screening Phase of Systematic Literature R...      3154       735  [-0.05408083274960518, 0.01748509891331196, 0....    0.414329
2      94  Springer Nature 2021 L ATEX template AI to aut...      3396       643  [-0.044118233025074005, 0.019377470016479492, ...    0.405429
3     121  (a) ASReview (b) RobotAnalyst Fig. 2 : Example...      2473       498  [-0.04962187260389328, 0.021930845454335213, 0...    0.405254
4     100  Springer Nature 2021 L ATEX template AI to aut...      2871       691  [-0.025931384414434433, 0.039575282484292984, ...    0.401183
5      92  Springer Nature 2021 L ATEX template AI to aut...      3531       707  [-0.015247180126607418, 0.034766774624586105, ...    0.393338
6     120  (Abstractr, FAST2, Rayyan, RobotAnalyst) exclu...      3792       810  [-0.04040976241230965, 0.01886066049337387, 0....    0.393051
7      95  Springer Nature 2021 L ATEX template 12 AI to ...      3478       675  [-0.0297419261187315, 0.023219799622893333, 0....    0.392724
8      99  Springer Nature 2021 L ATEX template 16 AI to ...      3533       683  [-0.019788986071944237, 0.029842868447303772, ...    0.392034
9      88  Springer Nature 2021 L ATEX template AI to aut...      2329       471  [-0.018015630543231964, 0.02516648918390274, 0...    0.387601
10    101  Springer Nature 2021 L ATEX template 18 AI to ...      3328       646  [-0.020250288769602776, 0.04757210612297058, 0...    0.386951
11    114  and the papers citing them. This process led t...      1473       315  [0.013657258823513985, 0.019240688532590866, 0...    0.384614
12    122  Fig. 3 : Examples of the tagging process of Co...      2491       484  [-0.03773682191967964, 0.040715306997299194, 0...    0.383918
13     91  Springer Nature 2021 L ATEX template 8 AI to a...      3251       620  [-0.03894846886396408, 0.023499155417084694, 0...    0.382679
14     93  Springer Nature 2021 L ATEX template 10 AI to ...      3480       684  [-0.030674586072564125, 0.04793224111199379, 0...    0.380571
15    119  4.2 Results In this section, we present the re...      3447       721  [-0.03444983810186386, 0.037512630224227905, 0...    0.379536
16    137  A.2 Extraction Phase of Systematic Literature ...      1873       409  [-0.02989894524216652, 0.017277246341109276, 0...    0.378214
17     87  Springer Nature 2021 L ATEX template 4 AI to a...      3463       665  [0.012063674628734589, 0.036320462822914124, 0...    0.375723
18    112  the relevant papers according only to the titl...      3510       674  [0.002680516801774502, 0.035781070590019226, 0...    0.375250
19     90  Springer Nature 2021 L ATEX template AI to aut...      3216       635  [-0.03239254280924797, 0.042684487998485565, 0...    0.374014
20    102  Springer Nature 2021 L ATEX template AI to aut...      3477       654  [-0.0028431073296815157, 0.029296431690454483,...    0.364503
21    123  keywords in their titles or abstracts. Rayyan ...      3409       724  [-0.02940652333199978, 0.025924542918801308, 0...    0.364481
22    103  Springer Nature 2021 L ATEX template 20 AI to ...      3458       670  [-0.010923407971858978, 0.02986292541027069, 0...    0.362138
23    115  Table 1 : The 21 SLR tools analysed in this su...      2468       584  [-0.03292127326130867, 0.05831916630268097, 0....    0.360862
24    125  (a) Nested Knowledge: Hierarchical Ontol- ogy ...      2484       524  [-0.021026095375418663, 0.033674392849206924, ...    0.360141
25     83  26 [111] K. Nandra, D. Barret, X. Barcons, A. ...       644       284  [0.012574666179716587, -0.004050031770020723, ...    0.359884
-------------------------------------------------------------------------------------------------------------------------------------------------------------------
The references provided cover a variety of topics in astronomy and astrophysics. Topics being studied include the use of AI in systematic literature reviews in astronomy, the analysis of scientific literature, the distribution of primary studies per year, the automation of systematic reviews, paper classification tools, and the AI features used in systematic literature review tools.

The differences between the papers lie in their specific focus and methodologies. Some papers analyze the automation of systematic reviews using AI, while others focus on the classification of relevant papers in systematic literature reviews. There are variations in the AI approaches used, such as machine learning algorithms like Support Vector Machines, Neural Networks, and Named Entity Recognition. Additionally, some papers explore the use of specific tools like Abstrackr, Colandr, and Iris.ai for tasks such as screening, data extraction, and summarization in the context of systematic literature reviews in astronomy and astrophysics.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

PREREQUISITES: 

HOW TO USE:

