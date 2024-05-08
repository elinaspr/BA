</p> The BA folder includes all code used in the process of my Bachelor thesis. 
The document CollocationsPaket is a Jupyter Notebook in Python. </p> 
<i> To use the project</i>, run the cells in the listed order (cell 5 only during the first time to create a single text file with all relevant texts, 
cell 4 only if such a text file already exists.) </p>
</p> <i>Purpose</i>: The ultimate goal was to find "feste Wendungen" - words that co-appear in a certain combination overly often and 
make use of grammatical structures more difficult than the individual vocabulary.
This was achieved by identifying bigrams, trigrams and fourgrams with the nltk collocations package. 
The notebook creates output files with top bigrams, trigrams and fourgrams, sorted by the corresponding measurement value used to identify them. 
The used measurement values include pointwise mutual information, likelihood ratio, and frequency. 
The functions in the code take a specified "ngram" (bigram, trigram or fourgram) as a string, and the amount of top entries one wants to identify, , the integer <i>n</i. </p>
</p> <i>Filtering:</i> Ngrams with the word 'gibt' or named location/person entities occurred very often in similar grammatical structures 
and didn't provide any additional helpful information on "feste Wendungen", but rather cluttered the output. 
The code thus attempts to not include ngrams with 'gibt' or Named person/location Entities in the final output to make it more readable.
Thus, the final list of top ngrams is often shorter than <i>n</i.
The model used for Named Entity Recognition is the spacy model de_core_news_sm. 
The identification of named entities and 'gibt' does not work in all cases, but in some. Therefore, it still successfully shortens the output - which was the goal of the filtering process. </p>
</p> <i>Limitations:</i> Making sure that the output list is exactly <i>n</i> long is a potential task for the future. A not yet working proposal for implementation is included in cell 11. 
