# Movie Recommendation System

This is a movie recommendation system created in Python. It utilizes "The Movies" dataset from Kaggle, containing various movie metadata such as title, genre, language, cast, crew, etc. I have removed unnecessary columns, empty rows, and adjusted some values to align with real-world data. As part of data cleaning, I converted the data format to lowercase, removed spaces between words, and combined all metadata into a single column.

I applied the TFIDF Vectorizer to convert this data into a TFIDF matrix, which selects features automatically. Another option here is the Count Vectorizer, but I opted for TFIDF because it considers both word counts and their relative positions, offering a more nuanced approach. You can find these functions in the SciKit Library; ensure to pass appropriate parameters based on your needs.

The system comprises two parts. The first is movie-based recommendation, where you input different movies you've watched or liked, and it outputs related movies. I created a centroid vector, the mean of every distinct parameter of all movies, as a base case. It then outputs the K Nearest Neighbors (KNN) of the centroid movie, and various filters like genre, cast, crew, and tags can be applied.

The second part uses user-based recommendation. Previous watch history or favorite movies are required for this. Users are divided into clusters based on their ratings and favorite movies. Top-rated movies among the cluster and movies related to them are recommended to all users in the cluster. There's an option to ignore already watched movies. The system is encapsulated in a function to integrate with a Telegram chat bot, serving as the interface. The bot is currently inactive, and I recommend setting up your own bot and entering the API key. You can also use it without Telegram by passing parameters directly into the function, as shown in the example.

The dataset [(The Movies)[https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset?resource=download]] comprises over 45,000 movies in 26 different languages. I have provided documentation for the project. I hope you find it helpful. Thank you for stopping by! ✌️ __...  Yagna Rao

