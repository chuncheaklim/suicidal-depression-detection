# suicidal-depression-detection
Suicidal depression detection from Reddit texts in translated Malay language using deep and transfer learning

The aim of this project is to identify potential suicide tendencies in Malay language Reddit texts. The motivation behind this research is the lack of comprehensive implementations for this domain in Malay, whereas other languages have more mature solutions. With the Covid-19 pandemic affecting Malaysia, leading to physical and mental challenges like fear of losing loved ones, unemployment, and increased depression, the project seeks to utilize text mining algorithms to detect signs of depression early and prevent tragic outcomes.

To achieve this, a dataset of 232,074 texts from the Suicide Watch subreddit was used. Originally in English, the texts were translated into Malay due to limitations in web scraping using the Snscrape API since April 2023. For the initial phase, 20,000 texts were extracted, and those with more than 128 words were filtered out to avoid excessive zero paddings for shorter texts.

The translated texts underwent preprocessing, and word cloud analysis revealed that users with suicidal tendencies expressed more negativity and self-centeredness, using first-person terms more frequently than non-depressed users. Feature extraction using Word2Vec and FastText was performed, and the social network of the 20 most common words was visualized.

Different models were considered for the next step, including bi-LSTM using the extracted features and BERT and XLNet using the raw translated text without preprocessing or feature extraction due to their built-in capabilities for handling these tasks.

The evaluation showed that BERT had the highest testing accuracy and the lowest false negative rate. Consequently, it was selected to predict the classification of six unseen texts, which included various noises such as Malay short forms, stop words, and punctuation. BERT successfully classified all the unseen texts correctly, demonstrating its ability to handle contextual information and noisy inputs effectively.
