# MUSIC GENRE CLASSIFICATION WITH DIGITAL SIGNAL PROCESSING METHODS

Music genre classification using digital signal processing methods is a wide area where new studies are continuously being made in order to increase the success rate.

In this study, we investigated how various clustering algorithms applied on feature vectors of audio signals affect classification success rates.

We have used GTZAN dataset for the project as it was most convenient. Description of each file are below for the project to be understood.

*FAQ and explanations of some terms can be found at the end of the text.*

## Files 

- **article.pdf**    
  appropriate article of the project
- **clustering.ipynb**      
  python code of reading music files, extracting feature vectors, clustering each feature vector, writing wanted statistical values of clustered vectors. 
detailed explanation inside of file.
- **clustering_use.txt**      
  clustering.ipynb file usage description
- **ml.ipynb**      
  python code of applying various machine learning algorithms to given dataset, printing tables to compare results, printing confusion matrix of wanted ml algorithm.
- **ml_use.txt**     
  ml.ipynb file usage description
- **dataset.txt**    
  link of used dataset. (includes important statement).

  
## TLDR for article
  There is lots of different studies in this subject as i mentioned above.     
Basically, the main idea of the topic is extracting some useful and numerical vectors of features of audio files and feeding them to machine learning algorithms to classify music genres.
Different studies focus on different aspect of this process. Some might do some feature engineering on ml phase, some might compare different features of audio files. 
In this project, we asked that what if we cluster those feature vectors? We might group similar properties of each vector and increase the success rates of classifiers.
So we extracted features, clustered each feature vector to 2 and 3 clusters using different clustering methods, prepared csv files by their statistical values, applied different machine learning algorithms and compared results.
Then, we conclude that clustering vectors by our methods decreases success rates significantly in most of the cases. Detailed comparison can be found in the file article.pdf.
  
  
## FAQ and some explanations 
  1. What is music genre classification?     
    - A field that focuses on classifying and recognizing genres of music files. It can be made via Natural Language Processing (lyrics) and Digital Signal Processing (audio) or both.
    You try to find similarities between the songs in same genre and classify new songs using this similarities. Machine learning, deep learning and clustering methods is frequently used.
  2. Digital signal processing??    
    - A huge field that focuses on digitalizing real life signals and researches features of any kind of signal. In this project, specifically audio signal processing applied. Populer audio processing library librosa is used.
  3. What is feature vectors and why they have to be numeralized?   
    - Feature vectors can be described as properties of audio files in the form that can be understood by computer. Each digitalized audio file has some features such as spectral centroid or mel-frequency cepstral coefficients. S
    Some may be more important in each genre and some may not. For detailed information, signal processing topic can be researched. 
   4. What is the meaning of applying clustering algorithms on feature vectors?   
    - Feature vector is a vector that includes thousands of float numbers inside. For example chroma_stft feature vector of a song is like: [4.13214 3.21314 4.7686 ... 2.965834 3.2141 2.6478]
    Normally you calculate mean or standart deviation of this vector and use them for classifying. Here, we clustered this vector into 2 or 3 groups using different clustering algorithms. So we got relatively similar 2 or 3 vectors from each vector. 
    After that we calculated statistical values and used them for classifying. 
