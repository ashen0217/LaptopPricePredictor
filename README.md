# Laptop Price Predictor

A machine learning web application that predicts laptop prices based on various specifications and features. This project consists of two main components: a model training pipeline and a web interface for making predictions.

## Project Structure

```
├── model building/
│   ├── laptop_price.csv        # Dataset for training
│   ├── price_predictor.ipynb   # Model training notebook
│   └── requirements.txt        # Dependencies for model building
└── web application/
    ├── app.py                 # Flask web application
    ├── Procfile              # Heroku deployment file
    ├── requirements.txt      # Dependencies for web application
    ├── model/               # Saved model directory
    ├── static/              # CSS and static files
    └── templates/           # HTML templates
```

## Features

- Predicts laptop prices based on:
  - RAM capacity
  - Weight
  - Company/Brand
  - Type (Gaming, Ultrabook, Notebook, etc.)
  - Operating System
  - CPU (Intel Core i3/i5/i7, AMD)
  - GPU (NVIDIA, AMD, Intel)
  - Screen features (Touchscreen, IPS)
- Interactive web interface for easy prediction
- Responsive design
- Machine learning model trained on real laptop data
- Price prediction in LKR (Sri Lankan Rupees)

## Technologies Used

### Model Building

- Python
- NumPy
- Pandas
- Scikit-learn
- Random Forest Regressor
- GridSearchCV for hyperparameter tuning

### Web Application

- Flask
- HTML/CSS
- Pickle for model serialization
- Bootstrap for styling

## Model Development

The machine learning model was developed using the following steps:

1. Data preprocessing

   - Handling missing values
   - Feature engineering
   - Categorical encoding
   - Data cleaning and transformation

2. Feature Selection

   - Removed unnecessary columns
   - Created new features from existing data
   - One-hot encoding for categorical variables

3. Model Selection

   - Tested multiple algorithms:
     - Linear Regression
     - Lasso Regression
     - Decision Tree
     - Random Forest
   - Selected Random Forest based on best performance

4. Hyperparameter Tuning
   - Used GridSearchCV to find optimal parameters
   - Optimized for better prediction accuracy

## How to Use

### Local Development

1. Clone the repository

```bash
git clone https://github.com/ashen0217/LaptopPricePredictor.git
cd LaptopPricePredictor
```

2. Install dependencies for model building (optional, if you want to retrain the model)

```bash
cd "model building"
pip install -r requirements.txt
```

3. Install dependencies for web application

```bash
cd "../web application"
pip install -r requirements.txt
```

4. Run the Flask application

```bash
python app.py
```

5. Open your browser and navigate to `http://localhost:5000`

## Model Performance

The Random Forest model was selected after comparing various algorithms:

- Achieved high accuracy through hyperparameter tuning
- Handles non-linear relationships effectively
- Robust to outliers and noise in the data

## Future Improvements

- Add more features for prediction
- Implement real-time market price comparison
- Add support for more currencies
- Include price history trends
- Implement automated model retraining
- Add user authentication for saving predictions

## Contributing

Feel free to fork the project and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is open source and available under the [MIT License](LICENSE).
