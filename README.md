# Content Based Movie Recommendation

## What are we doing?

Recommandation systems are used to help customer find content/data that they are more likely to consume. This project aims to build a movie recommendation system. The project uses TMBD 5000 dataset (https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata).

## What type of recommendation systems are we building?

We are building a content based recommendation system. These types of recommendation systems try to suggest your content similar to the content that you have previously consumed. For e.g. - If you have been watching a lot of thriller movies, these type of recommendation system will suggest you content which is similar to your watch history.

## What are other type of recommendation system?

* Collaborative Filtering: These types of recommendation systems use other people's consumption behavior to suggest other user content to watch. For e.g. if you've watched a lot of thriller movies recently, then these recommendation system will suggest you content of users who have also been watching thriller movies along with other genre. The hypothesis behind these systems is that people with similar taste in content have higher probability of consuming each others content.

* Hybrid: These types of recommendation systems combine both content based and collaborative filtering techniques to recommend content.

## What methodology are we using?

* We are using movies overview, cast, director, genre information as source information.
* The source information from multiple columns is combined into a single columns, `tags`. Think of tags as a column that contains overview of a movie, it's cast, director and genre.
* Stemming is applied to the tags column.
* A bag of words representation is created for all movies, using words from tag column from all movies.
* After applying bag of words, each movie now gets its vector for tags.
* A cosine similarity is then found between all movies and their bag of word representation for the tag columns.
* Movies whose tags have high similarity with tags of other movies are expected to be more similar with respect to their content.
