**Description:**

A recommendation system using two approaches of context-based modelling is
built and analysed. The dataset used here is that of “Netflix TV shows and
movies” consisting of records of over 6000 movies and 3000 TV Shows. While
one model explores various features like director, country of origin, cast, and
genre the other leverages keywords from the description provided by Netflix to
recommend a TV Show/Movie to a user. The assumption is that the input to the
model is a TV show/movie that the user has already watched and likes. We
utilised concepts of cosine similarity that best fit the algorithms and the data to
implement the models and compare them. We see that recommendations given
based on features like director, country of origin, cast, and genre are more
fruitful to a user.

**First Model Approach:**

There are five features of the dataset that we will make use of in the approach
director, country, cast, and listed in which is nothing but the genre. The Input is
a single movie or TV show that the user currently likes and the output is a list of
five other movies or TV shows that he can watch next based on these features
that we've considered. The idea is to convert the data of these into binary data
frames such that these combined values of the features can be compared for
each movie. We can then compute a similarity between them and select the top
five similarities as our result. The similarity measure that we made use of is
cosine similarity which was explained previously.

**Second Model Approach:**

Netflix and countless other product-based companies also give content
descriptions. In the case of Netflix, this content is usually the summary of the
movie or the tv show. These Netflix descriptions or synopses are concise and
usually something that captures the eye of the audience. In some cases, this is
taken positively by the public and in other cases, fans are offended as these
descriptions are not apt for the said movie/TV show. Our second approach takes
advantage of these descriptions. We extract all the words from the description
and convert them into binary data frames for easier comparison. This can be
easily achieved using natural language processing libraries such as Punkt from
nltk package. This is done for each record. We then compare these and find the
movies that have the most words in common, this again is done using a
similarity measure called cosine similarity.
