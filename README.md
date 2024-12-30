# Anime-Recommendation-System


This project is a recommendation system for anime based on two approaches:
1. **Content-based recommendation**: Suggests similar anime based on their features (synopsis, genres, score, etc.).
2. **Collaborative filtering**: Suggests anime based on user ratings and preferences.

## Project Overview

The Anime Recommendation System utilizes two techniques:
1. **Content-based filtering**: Uses features such as the name, genre, score, and synopsis to find similar anime.
2. **Collaborative filtering**: Uses user ratings to find and recommend anime that are similar to those rated highly by a given user.

### Features:
- Content-based recommendation using TF-IDF vectorization and cosine similarity.
- Collaborative filtering using a ratings matrix and Pearson correlation.
- Retrieving anime recommendations based on user input.

## Technologies Used
- Python 3.x
- Pandas
- Numpy
- scikit-learn (for TF-IDF and cosine similarity)
- Matplotlib
- NLTK (for text processing)
- Jupyter Notebook (for interactive development)

## Setup

### 1. Clone the Repository
To get started with the project, clone the repository:


### 2. Install Dependencies
Ensure that you have Python 3.x installed on your system.


### 3. Download Datasets
You will need the following datasets to run the project:
- **anime.csv**: This dataset contains the basic details about anime.
- **anime_with_synopsis.csv**: This dataset contains additional details about the anime, including synopses.
- **rating_complete.csv**: This dataset contains the user ratings for various anime.

You can download these datasets from [Kaggle's Anime Dataset](https://www.kaggle.com/).

### 4. Run the Application
Once the datasets are available and dependencies are installed, you can run the Python script to start getting recommendations:

```bash
python Anime Recommendation.py
```

### Example Usage:
After running the script, you can get recommendations for a specific anime. For example:
```python
print(get_recommendation("Akira", 9))  # Content-based recommendation
find_me_film(121)  # Collaborative filtering recommendation
```

## Code Explanation

1. **Content-based Recommendation**:
   - We use **TF-IDF (Term Frequency-Inverse Document Frequency)** vectorization to convert text (synopsis) into numerical data.
   - The **cosine similarity** is then used to calculate the similarity between anime based on their features.
   - The `get_recommendation()` function retrieves a list of similar anime.

2. **Collaborative Filtering**:
   - This method is based on user ratings.
   - We use a **ratings matrix** to find correlations between anime based on user preferences.
   - The function `find_me_film()` takes the anime's ID and recommends other anime based on the correlation of user ratings.

3. **Data Merging**:
   - The datasets are merged based on the `MAL_ID` (MyAnimeList ID) to ensure that we get accurate information from multiple sources (anime features, synopsis, and ratings).

4. **Handling Missing Values**:
   - Missing values in the datasets are handled using the `.fillna()` method to avoid errors during calculations and data processing.

## Files Overview

- **anime.csv**: Contains information about anime like `MAL_ID`, `Name`, `Score`, `Genres`, etc.
- **anime_with_synopsis.csv**: Contains additional data such as synopses of anime.
- **rating_complete.csv**: Contains user ratings for the anime, which is used for collaborative filtering.
- **anime_recommendation.py**: The main Python script for generating recommendations using content-based and collaborative filtering.

## Example Output

**Content-based recommendation**:
```python
get_recommendation("Akira", 9)
```
This will return a list of 9 anime that are similar to **Akira** based on its features.

**Collaborative filtering recommendation**:
```python
find_me_film(121)
```
This will return a list of anime that are similar to the anime with ID 121, based on user ratings.

## Contributing

If you'd like to contribute to this project, feel free to fork the repository and submit a pull request. If you find any bugs or have any feature requests, please open an issue.
