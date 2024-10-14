# Movie Recommender System

A movie recommendation system built using Streamlit and TMDb API to suggest similar movies based on user selection. It also fetches movie posters using TMDb API for better visual representation.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [API Key Setup](#api-key-setup)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project recommends movies similar to the one a user selects from a dropdown. It leverages a pre-trained similarity matrix and the TMDb API to fetch movie posters. The system is simple yet effective in providing recommendations based on the movie title.

## Features

- Recommends 5 movies similar to the selected one.
- Fetches and displays movie posters from The Movie Database (TMDb).
- Built using `Streamlit` for a simple web-based interface.

## Installation

To run this project locally, follow these steps:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/movie-recommender-system.git
   cd movie-recommender-system
   ```

2. **Install dependencies**:

   Make sure you have Python 3 installed. Then, install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

3. **Download/Prepare the necessary files**:
   - Ensure you have the `movie_dict.pkl` and `similarity.pkl` files, which are required for movie recommendations.
   - You can generate these files by preprocessing a movie dataset or use the provided pre-trained models.

4. **Setup the TMDb API key**:

   You'll need to provide your own TMDb API key to fetch posters. You can either:
   - Set an environment variable named `TMDB_API_KEY`.
   - Or replace the API key directly in the code (not recommended for production).

   ```bash
   export TMDB_API_KEY=your_tmdb_api_key
   ```

5. **Run the application**:

   Use Streamlit to run the app locally:

   ```bash
   streamlit run app.py
   ```

   This will launch the app in your default web browser.

## Usage

Once the application is running:

1. Select a movie from the dropdown list.
2. Click the "Recommend" button to receive 5 movie recommendations.
3. Posters of the recommended movies will be displayed alongside their titles.

## Project Structure

```bash
movie-recommender-system/
│
├── app.py               # Main Streamlit app
├── movie_dict.pkl        # Preprocessed movie data
├── similarity.pkl        # Movie similarity matrix
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation
└── .gitignore            # Files to ignore in Git
```

## Technologies Used

- **Python**: Core language for the project.
- **Streamlit**: For creating the web-based UI.
- **Pandas**: Data manipulation and analysis.
- **TMDb API**: For fetching movie posters.
- **Pickle**: For loading preprocessed data.

## API Key Setup

To fetch movie posters, the application uses TMDb API. You will need to obtain an API key by signing up at [The Movie Database](https://www.themoviedb.org/).

Once you have the key, either set it as an environment variable `TMDB_API_KEY` or insert it directly into the `fetch_poster` function inside `app.py`:

```python
api_key = 'your_tmdb_api_key'  # Insert your API key here
```

## Contributing

Contributions are welcome! If you'd like to contribute, please fork the repository, create a feature branch, and submit a pull request.

1. Fork the project.
2. Create your feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.
   
## Screenshots

![Screenshot 2024-10-14 200155](https://github.com/user-attachments/assets/c0fe0efb-2a95-42a4-8871-797df7630e2a)
![Screenshot 2024-10-14 200227](https://github.com/user-attachments/assets/751d40bb-9cf0-406c-aad0-99a492f79be6)

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

### Notes:
- Replace the `yourusername` and `your_tmdb_api_key` placeholders with actual values.
- You may want to provide more detailed steps for generating the `movie_dict.pkl` and `similarity.pkl` files if they're not included in the repository.

