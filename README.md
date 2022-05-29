# Movie-Recommendation-Web-app
Content Based Recommender System recommends movies similar to the movie user likes based on content.
In this project I have used content based filtering to create a very basic prototype of movie recommender.
It is mostly based on the similarity of genre and content.
The top 5 similar movies are recommended.

 <br /> ****Note: Since the similarity.pkl file , required for app.py to run was very large and unable to be uploaded, is attached in a drive link.[https://drive.google.com/file/d/18A6yiN_7NKudVCyPBe8fnywC1piUZkXj/view?usp=sharing
 ](https://drive.google.com/file/d/18A6yiN_7NKudVCyPBe8fnywC1piUZkXj/view?usp=sharing)
 Download it along with the other files
 # Data Preprocessing
The data used is from https://www.kaggle.com/tmdb/tmdb-movie-metadata.
 <br />The movies file and credits file are merged.
 <br />The datas are made as list in respectective column.
 <br />The spaces between words are removed for better results.
 <br />Concatenate the columns overview,genres,keywords,cast and crew i to tags and the words are in lowercase.
# Cosine similarity

The Content-Based Recommender relies on the similarity of the items being recommended. The basic idea is that if you like an item, then you will also like a “similar” item. It generally works well when it’s easy to determine the context/properties of each item.The concepts of Term Frequency (TF) and Inverse Document Frequency (IDF) are used in information retrieval systems and also content based filtering mechanisms (such as a content based recommender). They are used to determine the relative importance of a document / article / news item / movie etc.
TF is simply the frequency of a word in a document. IDF is the inverse of the document frequency among the whole corpus of documents.

Vector Space Model ,each item is stored as a vector of its attributes (which are also vectors) in an n-dimensional space and the angles between the vectors are calculated to determine the similarity between the vectors. Next, the user profile vectors are also created based on his actions on previous attributes of items and the similarity between an item and a user is also determined in a similar way.
The ultimate reason behind using cosine is that the value of cosine will increase with decreasing value of the angle between which signifies more similarity. The vectors are length normalized after which they become vectors of length 1 and then the cosine calculation is simply the sum-product of vectors.

# app.py
Using streamlit
 <br /> Local URL: http://localhost:8501
 <br />  Network URL: http://192.168.1.4:8501
  <br /> PS: Since Deploying to heroku app failed, the web couldn't be hosted

# To run the app
Clone the repository, also include similarity.pkl from the drive link.
 <br />install streamlit and run the app in the project terminal
 <br />install streamlit: pip install streamlit
 <br />run the app:streamlit run app.py

