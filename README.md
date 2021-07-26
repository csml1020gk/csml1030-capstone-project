# csml1030-capstone-project
Document Classification 
York University MLC - CSML1030 Project proposal 
Project category : NLP 
July 2021 - September 2021

About Athennian:
Athennian’s product is a cloud based legal entity management software. The product is used by law firms and legal departments to power compliance and governance.Services provided include digital transformation of minute books for the law firm’s clients.

The problem:
Minute books have historically been stored by law firms on behalf of their clients in binders following traditional filing practices. Law firms wish  to move from physically storing minute book files in filing cabinets to the cloud. The first step in developing the paperless solution was to ensure minute books are scanned into PDFs. Coding approaches to analysing PDFs can provide insights and reports, but are not scalable.  Our task is to develop a scalable machine learning solution deployed on the cloud.  


Why is it interesting:
Digitizing the minute books and making them available on the cloud can help law firms provide additional value to their clients through on demand data access.

Challenges:
Minute books are generally scanned copies and due to different scanning practices, the pdfs are not uniform.
The data is unstructured and they are not organized.
The content varies and could be different for each client, as it is basically a summary of the corporation. It could range from few pages upto a few hundred pages and could include non standard forms.The data within the minute books may not be organized into the same sections.
The pages may not be scanned in the same order 






Benefits of a machine learning solution:
APIs for pretrained NLP models are widely available to tackle a variety of text data.
A model developed based on entities recognized from the training data can predict entities on text data.Unlike a rule based approach where adding or modifying rules could need a lot of analysis,  a model based approach can be scaled.Machine learning solutions can learn from sample data. 

How will it be done:
The extractor model has three stages and will evolve over several iterations 
Step1 :detect variables of concern in the input document.
Step2: categorize the variables
Step3: develop relationships that can be used as input to other software 
Each step could involve researching several APIs, iterating and choosing the right language model.


The data 
Sample data has already been collected . We have 4 sample PDFS which are representations of typical scanned copies of client’s minute books.

As the first text analysis technique, text extraction extracts pieces of data within the text. 
step, text needs to be extracted from the PDFS in order to be usable in code.
      
Scanned physical PDF minute books - > structure data to be useful for services offered by the law firms to their clients.The data can be re used in many ways eg. submit to other parties, create new documents/ reports.

We tried several text extraction libraries. The quality of the output from each of the tools was roughly the same. Scanned pages with images such as certificates, page dividers could not be extracted correctly and the use of a OCR tool for this purpose could be considered in a future iteration.

In order to continue with modeling for the first iteration ,we chose <   > .









Following basic text preprocessing, we performed qualitative text analysis on the sample PDFs:



PDF1
PDF2
PDF3 
PDF4 
Number of pages 








Sections 








Word frequency 








Density of text










Time Frame:
Start date: July 14, 2021
Submission: September 10, 2021 
The scope of the project and deliverable may be changed due to the timeframe available. 


Methodology:


Text Mining:
Having gathered and extracted the data, we proceed to prepare the data for machine learning using NLP techniques.
Our focus is on whole documents.
We choose a language model/grammar ( English )

Tokenization: What tokenization strategies work best so that the data is split properly?
Part of speech tagging: Is it necessary to add a grammatical category to each token?
Parsing: Is parsing to determine the syntactic structure of the text necessary?
Stemming and Lemmatization: Is it necessary to perform stemming and lemmatization?
Stopword removal:Could it be customized to remove  the characters generated from images? Is there a pattern among the PDFs? 



Text analysis methods: 
Text extraction is the process of recognising structured pieces of information from unstructured text. In our case, extracting variables of interest for further analysis.
1.regular expressions. To extract text, we create a regular expression that defines the pattern of characters associated with a tag. The matched text is assigned to the tag. 
2.Conditional Random Fields :Through CRF, we can add multiple variables which depend on each other to the patterns we use to detect information in texts, such as syntactic or semantic information.

1.Define the tags
2.regexp to extract company name , save to df 
3. Tag the extracted examples 
4. Test on new data 


Variable 
Category (tag)






Current Entity Name 
BASIC






Entity Type
TYPE










Evaluation criteria:
Metrics to assess the performance of text extractor 

Visualizing results:








Conclusion:
Text analysis is a powerful tool that can help provide insights from the PDF minute books. Automating the extraction of key variables can save time, allow clients to view minute books in a digital format, request changes, download and share them. In other words, provide better customer service to their clients. 
Appendix: 








