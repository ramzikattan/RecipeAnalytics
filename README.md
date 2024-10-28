# SnapChef: Personalized Recipe Recommender
## Contributors
Jose Nico Currea, Jenna Ferguson, Jennifer Gonzalez, Evan Hadd, Muhammad Ibrahim, Ramzi Kattan, Hadley Krummel

## Project Flow
- **0. Scraper -> CSV of Recipes**: Gather recipes and user reviews from AllRecipes.com, extracting key data like ingredients, cooking times, and ratings, and storing them in a CSV format.
- **1. Pre-Processing -> Filtered Recipe CSV**: Clean the data by extracting key ingredients from recipes and filtering out unnecessary details. Create a structured dataset ready for analysis.
- **2. Allergy Filtration -> Filtered Recipe CSV**: Filter recipes based on common allergens (e.g., gluten, dairy, nuts) to exclude recipes containing ingredients that may trigger allergies.
- **3. Ingredient Labeling & Attribute Extraction -> Ingredient List & Attribute List**: Label ingredients in photos using Google Vision and refine labels with a fine-tuned Faster R-CNN model, complemented by OpenAI GPT-4 for attribute extraction based on user descriptions.
- **4. Ingredient Recommender -> Threshold-Filtered Recipe CSV**: Use an ingredient-matching model to score recipes based on ingredients available to the user, filtering recipes based on ingredient feasibility.
- **5. Attribute Recommender -> Sentiment & Similarity Evaluations**: Generate similarity scores between user-described attributes and recipe reviews, combining these with feasibility scores to rank recipes.
- **6. Final Recommendation -> Top 3 Recipes**: Present the top three recipes based on feasibility and attribute similarity.

## Presentation Outline

### Section 1: Proof of Concept
- **Labeling Ingredients Example**: Demonstrate the process of extracting key ingredients from user-uploaded images.
- **User Description Example**: Showcase how the system interprets user descriptions to extract meal preferences and constraints.
- **Recommended Recipes (No Code just Demonstration)**: Present sample recipe recommendations to illustrate the end-to-end functionality.

### Section 2: Backend Workflow
- **Scraping**: Overview of the web scraping process using Selenium and BeautifulSoup to gather data from AllRecipes.com.
- **Pre-Processing**: Data cleaning and filtering to prepare recipes for further analysis, including ingredient extraction.
- **Allergy Filtration**: Implementation of allergen filtering to exclude recipes with ingredients that users may want to avoid.
- **Image Analytics & Attribute Extraction**: User uploads images to identify available ingredients; extract user preferences with OpenAI's GPT-4.
- **Ingredient-Requirements Recommendations**: Recommend recipes based on a threshold for ingredient feasibility.
- **Attribute-Review Recommendations**: Utilize spaCy for semantic matching of user-described attributes to recipe reviews.

### Section 3: Future Work
- **App Design & Chatbot UI**: Develop a user-friendly app interface, incorporating an interactive chatbot for intuitive interactions.
- **Memory Features (Allergies, Cookware, Preferences)**: Add functionality to remember user preferences, allergies, and available cookware for personalized recommendations.
- **Integration with Grocery Stores (HEB Plugin)**: Enable users to order missing ingredients from local stores directly through the app.
