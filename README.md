</p> The BA folder includes all code used in the process of my Bachelor thesis. 
The notebook CollocationsPaket is a Jupyter Notebook in Python used to search for collocations in a text file. It was applied on the text file output-leicht.txt containing merged texts from a "Deutsch perfekt" Database labelled as "_Leicht" and publsihed from 2017 to 2020. The notebook AppliedFunctions contains sueful additional functions when working with CollocationsPaket and analyzing its functioning. </p> 
</p> <i>CollocationsPaket</i></p>
<i> To use CollocationsPaket</i>, run the cells in the listed order 
</p> <i>Purpose</i>: The ultimate goal was to find "feste Wendungen" - words that co-appear in a certain combination overly often and 
make use of grammatical structures more difficult than the individual vocabulary.
This was achieved by identifying bigrams, trigrams and fourgrams with the nltk collocations package. 
The notebook creates output files with top bigrams, trigrams and fourgrams, sorted by the corresponding measurement value used to identify them. 
The used measurement values are <i>pointwise mutual information, likelihood ratio, and frequency</i>. 
The functions in the code take a specified "ngram" (bigram, trigram or fourgram) as a string, and the amount of top entries one wants to identify, , the integer <i>n</i>. </p>
</p> <i>Filtering:</i> Ngrams with the word 'gibt' or Named person/location Entities occurred very often in similar grammatical structures 
and didn't provide any additional helpful information on "feste Wendungen", but rather cluttered the output. 
The code thus attempts to not include ngrams with 'gibt' or Named person/location Entities in the final output to make it more readable.
Thus, the final list of top ngrams is often shorter than <i>n</i>. The filtering process was analyzed in <i>AppliedFunctions</i></i>
The model used for Named Entity Recognition is the spacy model <i>de_core_news_sm</i>. 
</p> <i>AppliedFunctions</i></p>
<i> To use AppliedFunctions</i>, search for the appropriate cells and run them respectively. 
</p> <i>Purpose</i>:
The functions included in this notebook serve the sake of illustration, analyzation and proposals of improval regarding CollocationsPaket. 
</p> <i>Filtering</i>: 
The notebook contains functions that were used to analyze the the filtering process. Since the filtering out didn't work in 100% of all cases, we reviewed the exact amount of filtered out n-grams. Review them for more details and the exact results. It was found that in total, the code filtered out 67 bigrams, 130 trigrams, and 84 fourgrams. Therefore, it still successfully shortened the output - which was the goal of the filtering process. </p>
</p> <i>Report of Limitations:</i> Making sure that the output list is exactly <i>n</i> long is a potential task for the future. A not yet working proposal for implementation is also included in AppliedFunctions. 
