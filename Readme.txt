All code is inside the /code folder and is in form of .ipynb files

Code should be run in the order its mentioned in the readme 

##### Warning- Running the complete code specially the data prep can take hours based on the machine ######

Code is divided into multiple folders based on the stage of the project 

The readme talks about the folder structure and briefly about the files in each folder

1. 	/code/data prep - This folder is for the data prep code. The orginal data for this code can be downloaded from 
	https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/0TJX8Y or can be found in the raw data folder
	Please change the path accordingly.
	
	un_speeches_tokenised.json is attached with the code submission for running the NLP code base(this is the pre processed data 
	which is the output to the below process.

		un data prep.ipynb- This file take the .txt file of the corpus and merges with the meta data
			*Please make sure the paths are changed accordingly while running it*
		
		Analysis and tokenisation.iypnb- This file splits the code into word and sentence token and produces a json 
		output for use in later process called un_speeches_tokenised.json

2.	/code/Sentiment Speech embeddings and cluster- This folder contains the un_speeches_tokenised.json prep data file and 
	also the code,visualization,model file for the sentiment speech vectorisation and clustering approach.
		
		un_speeches_tokenised.json- The data file for data prep step
		
		Sentiment_and EDA.ipynb- This code is for sentiment analysis and EDA
		
		sentiments_major_nations.html- Visualization of the sentiments of 9 major countries
		
	
		Below are description of the files for 2019 analysis. Other years follow a similiar naming convention and names are
		self explanatory. Replace the year for the file of the respective year
		
		Doc2Vec for speech2019 similiarity_without_GPE_new.ipynb- The code for file GPE removal ,doc2vec and clustering for 2019
		
		doc2vec_new_without_gpe_2019.model- The saved Doc2Vec model 
		
		speechs_2019_Without_GPE_new.html- Visualization of the TSNE of the speeches embeddings viaa Doc2Vec by countries
		
		speechs_2019_Without_GPE_new_labels_dendogram.html- Visualization of the TSNE of the speeches embeddings viaa Doc2Vec by countries clustered 
		by hierachial clustering
		
		speechs_2019_Without_GPE_new_labels_kmeans.html-Visualization of the TSNE of the speeches embeddings viaa Doc2Vec by countries clustered 
		by K means
		
		speechs_2019_Without_GPE_new_labels1.html-Visualization of the TSNE of the speeches embeddings viaa Doc2Vec by countries clustered 
		by DBSCAN
		
		
3. 	/code/Topic modelling- This folder contains topic modelling and output of the files from the previous step

		Below are description of the files for 2019 analysis. Other years follow a similiar naming convention and names are
		self explanatory. Replace the year for the file of the respective year
		
		un_speeches_2019_labels.json- Output of the speech embeddings and clustering via DBSCAN step
		
		2019 Topic modelling.ipynb- The file for LDA for clustered 2019 speeches
		
		LDA_results_2019.txt- Results for 2019 LDA across clusters
		
		speechs_2019_worldmap with topics.html- Visualization of the world map of major topics for 2019 speeches
		
4.	/raw data- This folder contains raw data in zip format and is input to file in the data prep step.		


REFERENCES
[1] A. Baturo, N. Dasandi, and S. J. Mikhaylov, “Understanding state
preferences with text as data: Introducing the UN General Debate
corpus,” Research Politics, vol. 4, no. 2, p. 2053168017712821, 2017,
doi: 10.1177/2053168017712821.
[2] S. Jankin Mikhaylov, A. Baturo, and N. Dasandi, “United Nations
General Debate Corpus,” Harvard Dataverse, 2017.
[3] M. Laver, K. Benoit, and J. Garry, “Extracting Policy Positions from
Political Texts Using Words as Data,” The American Political Science
Review, vol. 97, no. 2, pp. 311–331, 2003.
[4] A. Baturo and N. Dasandi, “What drives the international develop-
ment agenda? An NLP analysis of the united nations general debate
1970–2016,” in 2017 International Conference on the Frontiers and
Advances in Data Science (FADS), Oct. 2017, pp. 171–176. doi:
10.1109/FADS.2017.8253221.
[5] J. Pennington, R. Socher, and C. Manning, “Glove: Global Vectors
for Word Representation,” in Proceedings of the 2014 Conference on
Empirical Methods in Natural Language Processing (EMNLP), Doha,
Qatar, 2014, pp. 1532–1543. doi: 10.3115/v1/D14-1162.
[6] M. Honnibal and I. Montani, “spaCy 2: Natural language understanding
with Bloom embeddings, convolutional neural networks and incremental
parsing,” 2017.
[7] Q. Le and T. Mikolov, “Distributed Representations of Sentences and
Documents,” in Proceedings of the 31st International Conference on
Machine Learning, Jun. 2014, pp. 1188–1196. Accessed: Dec. 08, 2022.
[Online]. Available: https://proceedings.mlr.press/v32/le14.html.
[8] Van der Maaten, L.J.P.; Hinton, G.E. Visualizing High-Dimensional Data
Using t-SNE. Journal of Machine Learning Research 9:2579-2605, 2008.
[9] Ester, M., H. P. Kriegel, J. Sander, and X. Xu, ”A Density-Based Algo-
rithm for Discovering Clusters in Large Spatial Databases with Noise”.
In: Proceedings of the 2nd International Conference on Knowledge
Discovery and Data Mining, Portland, OR, AAAI Press, pp. 226-231.
1996.
[10] R. Rehurek and P. Sojka, “Gensim–python framework for vector space
modelling,” NLP Centre, Faculty of Informatics, Masaryk University,
Brno, Czech Republic, vol. 3, no. 2, 2011
