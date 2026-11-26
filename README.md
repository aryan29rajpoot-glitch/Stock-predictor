# 📈 Stock Price Predictor

A web-based Stock Price Prediction application built using **Python, Flask, Machine Learning, and JavaScript**. The application fetches historical stock market data and uses Linear Regression to estimate future stock prices.

Users can select popular stocks or enter their own stock ticker symbol, choose the number of days for prediction, and view the prediction results along with a BUY, SELL, or HOLD recommendation.

## 🚀 Features

- **Stock Selection:** Choose popular stocks such as Apple, Microsoft, Google, Amazon, Tesla, and NVIDIA.
- **Custom Stock Search:** Enter a stock ticker symbol manually.
- **Real-Time Historical Data:** Fetch historical stock prices using Yahoo Finance (`yfinance`).
- **Machine Learning Prediction:** Uses Linear Regression to predict future stock prices.
- **Flexible Predictions:** Select a prediction period between 1 and 10 days.
- **Investment Recommendation:** Generates BUY, SELL, or HOLD recommendations based on predicted price movement.
- **Interactive Dashboard:** Simple and user-friendly web interface.
- **Error Handling:** Handles invalid stock symbols and data-fetching errors.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| Flask | Web application framework |
| Scikit-learn | Linear Regression model |
| NumPy | Numerical computations |
| Pandas | Data manipulation |
| yfinance | Fetching historical stock market data |
| HTML5 | Webpage structure |
| CSS3 | User interface styling |
| JavaScript | Frontend functionality |
| Chart.js | Stock chart visualization |

## 🧠 Machine Learning Approach

The application uses **Linear Regression**, a supervised machine learning algorithm.

### How It Works

1. The user enters a stock ticker symbol.
2. The application fetches the last 60 days of historical stock data using Yahoo Finance.
3. Closing prices are extracted from the historical dataset.
4. Time-based features are created using sequential day numbers.
5. A Linear Regression model is trained using historical prices.
6. The trained model predicts prices for the selected future days.
7. The application calculates the percentage change between the current and predicted prices.
8. A BUY, SELL, or HOLD recommendation is generated.

### Recommendation Logic

| Condition | Recommendation |
|---|---|
| Predicted price increases by more than 2% | BUY |
| Predicted price decreases by more than 2% | SELL |
| Price change is within ±2% | HOLD |

**Note:** These recommendations are generated using simple prediction thresholds and should not be considered financial advice.

## 📂 Project Structure

```text
Stock_predictor/
│
├── app.py                  # Flask application and prediction API
├── model.py                # Stock prediction helper functions
├── model.pkl               # Serialized model file
├── train_model.py          # Model training script
├── requirements.txt        # Python dependencies
│
├── static/
│   ├── style.css           # Application styling
│   └── script.js           # Frontend functionality
│
└── templates/
    └── index.html          # Main application webpage
```

## ⚙️ Installation and Setup

Follow these steps to run the project locally.

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

### 2. Navigate to the Project Folder

```bash
cd Stock_predictor
```

### 3. Create a Virtual Environment (Recommended)

```bash
python -m venv venv
```

Activate the virtual environment:

**For Windows:**
```bash
venv\Scripts\activate
```

**For macOS/Linux:**
```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the Application

```bash
python app.py
```

### 6. Open in Browser

Visit:

```text
http://127.0.0.1:10000
```

The Stock Price Predictor application will now be running locally.

## 📊 Example Stocks

The application supports popular stock symbols, including:

- AAPL – Apple
- MSFT – Microsoft
- GOOG – Google
- AMZN – Amazon
- TSLA – Tesla
- NVDA – NVIDIA

Other valid Yahoo Finance ticker symbols can also be entered manually.

## 🔮 Future Improvements

- Implement advanced prediction algorithms such as Random Forest, XGBoost, and LSTM.
- Improve prediction accuracy using technical indicators.
- Add interactive historical stock price charts.
- Include more Indian and international stock exchanges.
- Add user authentication and personalized watchlists.
- Improve model evaluation using MAE, MSE, and RMSE.
- Integrate additional financial market indicators.

## ⚠️ Disclaimer

This project is developed for educational and learning purposes. Stock market predictions are estimates based on historical data and do not guarantee future market performance. Do not use the predictions as the sole basis for investment decisions.

## 👨‍💻 Author

**Aryan Rajpoot**

B.Tech – Computer Science and Engineering (Data Science)

GitHub: [Your GitHub Profile](https://github.com/YOUR-USERNAME)

---

⭐ If you find this project useful, consider giving this repository a star!
