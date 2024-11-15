# Sentiment Analysis of Yelp Reviews for Asian Cuisine Restaurants (3-3.5 Stars)

## Project Overview
This project aims to analyze Yelp reviews of Asian cuisine restaurants in Canada with a mid-range rating (3 to 3.5 stars). The goal is to identify common themes in customer reviews, understand sentiment related to different aspects (e.g., food, service, ambiance), and provide actionable recommendations for restaurant owners to improve customer satisfaction.

## Repository Structure
- **01_data_loading_preparation.ipynb**: This notebook covers the initial data loading and preparation, including filtering the Yelp business and review datasets to focus on Asian cuisine restaurants located in Canada.

- **02_exploratory_data_analysis.ipynb**: This notebook performs exploratory data analysis (EDA), providing descriptive statistics, visualizations of ratings, and common keywords to gain an initial understanding of the dataset.

- **03_data_cleaning_and_keywords.ipynb**: This notebook details data cleaning procedures, including removing noise from reviews and extracting relevant keywords for analysis, such as food-related and service-related terms.

- **04_sentiment_and_topic_modeling.ipynb**: This notebook applies sentiment analysis using the VADER model to assess customer sentiment towards different aspects of their dining experience, such as food quality and service. It also uses topic modeling (Latent Dirichlet Allocation - LDA) to identify the key themes discussed by customers in their reviews, providing insights into recurring topics and their associated sentiment.

- **data/**: This folder contains the filtered datasets used in the analysis. The original Yelp dataset is not included due to size constraints but can be accessed from the Yelp Dataset repository.

- **README.md**: A detailed summary of the project, including its purpose, key findings, repository structure, and instructions for running the notebooks.

## Instructions
1. **Data Preparation**: The dataset used for this project can be accessed from the [Yelp Dataset repository](https://www.yelp.com/dataset). After downloading, place the data in the `data/` folder.
2. **Dependencies**: Ensure you have all dependencies installed. You can do this by running:
   ```sh
   pip install -r requirements.txt
   ```
3. **Running the Analysis**:
   - Start with `01_data_loading_preparation.ipynb` and proceed sequentially through each notebook.
   - Each notebook builds on the results of the previous one, so it's important to run them in order.

## Initial Results
- **Food Quality**: Overall sentiment related to food quality was positive, with customers appreciating the authenticity and taste of popular dishes like pho and ramen.
- **Service Issues**: Service was frequently mentioned as a pain point, particularly related to wait times and unfriendly staff interactions.
- **Ambiance**: The ambiance received mixed reviews, with some customers mentioning decor improvements that could enhance their experience.

## Key Recommendations
- **Staff Training**: Improve customer interactions by training staff to be more attentive and friendly.
- **Highlight Popular Dishes**: Promote well-received dishes, such as pho and sushi, in marketing materials.
- **Enhance Ambiance**: Make small but effective improvements in decor, lighting, and music to improve the dining atmosphere.

## Video Presentation
A video presentation titled **"Initial Results and Code Walkthrough"** is available, showcasing the early findings of this analysis along with a code walkthrough of key sections. The link to the video is included in the repository.

## License
This project is licensed under the **MIT License**. See the LICENSE file for more details.

### Data License
The data used in this project is provided under the **Yelp Dataset License**. This license allows for academic, non-commercial use of the dataset, which was obtained from the [Yelp Dataset repository](https://www.yelp.com/dataset).

