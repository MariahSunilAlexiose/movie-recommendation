# Movie Recommendation System
This project is a content-based movie recommendation system. It suggests movies similar to the user's favorite movie based on textual features such as genres, keywords, taglines, cast, and director.

## Libraries Used
- `numpy`
- `pandas`
- `difflib`
- `scikit-learn`

## Data
The dataset used is `movies.csv`, which contains information about various movies.

## Steps

1. **Loading and Inspecting Data**:
   - Import necessary libraries.
   - Load the dataset (`movies.csv`).

2. **Selecting Relevant Features**:
   - Choose features: `genres`, `keywords`, `tagline`, `cast`, `director`.

3. **Data Preprocessing**:
   - Fill missing values in the selected features with an empty string.
   - Combine the selected features into a single string for each movie.

4. **Text Feature Extraction**:
   - Convert the combined textual data into numerical feature vectors using `TfidfVectorizer`.

5. **Calculating Similarity Scores**:
   - Compute the similarity score between feature vectors using cosine similarity.

6. **Getting User Input**:
   - Prompt the user to input their favorite movie's name.

7. **Finding Closest Movie Match**:
   - Use `difflib.get_close_matches` to find the closest match to the user's input.

8. **Retrieving the Index of the Movie**:
   - Get the index of the closest matching movie title.

9. **Generating Recommendations**:
   - Enumerate and sort the similarity scores in descending order.
   - Display a list of recommended movies based on their similarity scores.
