# GamePriceAI: Estimating optimal steam game prices with AI

When I was working in a game company, it was pretty hard determining the price just from guesswork alone. This is a small project I want to launch to see if I can solve that issue with predictive AI, telling the optimal price (or the popular price) backed up by data from Steam. 

This project is my practice/ test to learn machine learning and develop predictive AI to learn from past data and suggest a price or price range that could lead to better decision making. 

### project structure plan
```
project/
├── README.md
├── requirements.txt
├── data/                    # Raw + cleaned CSVs (from SteamSpy, Steam APIs)
├── notebooks/               # Exploratory analysis + model training
├── models/                  # Saved price prediction models
├── figures/                 # Visualizations (price vs. score, etc.)
└── src/                     # Scripts for preprocessing, training, prediction
```

### Roadmap

1. Data collection
   - Steamdb, Steam’s API, [Stream Scraper](https://github.com/FronkonGames/Steam-Games-Scraper) or find existing data sets from Kaggle:
     - Need to contain Prices (discounted ones if possible, may able to get it in steamdb)
     - Review scores, owner numbers, genre, tags, release year

2. Data cleaning 
   - Prices should be in one currency e.g. usd
   - Create variables, e.g. discounted 5+ times or launch month
   - Other basic cleaning like missing value, duplicates, or anything that comes to. 

3. Targeting
   - Predict a price tier (cheap, standard, premium)
   - Or aim to estimate an exact price that leads to high engagement/ownership?

4. Train AI
   - Use models like Random Forest or XGBoost
   - Compare which models give the most accurate results

5. Analyse
   - Use SHAP or similar tools to see which features matter most
   - Plot key trends by genre, review score, or discount strategy. Maybe powerbi?
  
6. Repeat  
   - Tune hyperparameters and retrain  
   - Try new features or new targets  
   - Think if there is any unseen game data

7. App making?   
   - Create a basic Streamlit app where users input their game info and get a price recommendation? optional 

### Limitations and considerations

- Steamspy estimates may not always be precise; owner counts are rounded
- No data on marketing, community hype, or external influences
- Price prediction depends on the data's quality — not a guaranteed success formula

### Bonus ideas (optional)

- Try using unsupervised learning clustering games based on features to discover pricing patterns
- Compare your price prediction to actual top-selling games during Steam sales
- Test different modeling approaches like LightGBM or CatBoost for performance gains
- Explore NLP analysis of game reviews or descriptions to include player sentiment

### Dependencies
- Python 3.10+
- Key libraries: pandas, scikit-learn, xgboost, shap, matplotlib, streamlit

### License 📜

MIT License
