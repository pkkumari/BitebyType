# 🍽 BiteByType

A personalized meal finder built with Streamlit that recommends recipes based on your personality, favorite ingredients, or nutritional needs—and even shows nearby restaurants serving similar cuisines!

---

## Table of Contents

- [Features](#features)  
- [Demo](#demo)  
- [Tech Stack](#tech-stack)  
- [Getting Started](#getting-started)  
  - [Prerequisites](#prerequisites)  
  - [Installation](#installation)  
  - [Configuration](#configuration)  
  - [Running the App](#running-the-app)  
- [Usage](#usage)  
- [Project Structure](#project-structure)  
- [Contributing](#contributing)  
- [License](#license)  

---

## Features

- 🔍 **Search by Personality**  
  Map Big-Five (and beyond) traits to cuisines and fetch a random recipe.  
- 🥑 **Search by Ingredient**  
  Find recipes using one main ingredient and max prep time.  
- 🏋️ **Search by Nutrients**  
  Query recipes by calories, protein, or fat thresholds.  
- 📍 **Nearby Restaurants**  
  Use the Yelp API to list top 5 restaurants near you serving your chosen cuisine.  
- ⚡️ **Caching**  
  API responses are cached to speed up repeat queries.

---


## Tech Stack

- [Streamlit](https://streamlit.io/) for the interactive web UI  
- [Requests](https://docs.python-requests.org/) for HTTP calls  
- [Spoonacular API](https://spoonacular.com/food-api) for recipe data  
- [Yelp Fusion API](https://www.yelp.com/developers/documentation/v3) for restaurant recommendations  
- Python 3.8+

---

## Getting Started

### Prerequisites

- Python 3.7 or newer  
- A free API key from:
  - Spoonacular (https://spoonacular.com/food-api)
  - Yelp Fusion (https://www.yelp.com/developers)

### Installation

1. **Clone the repo**  
   ```bash
   git clone https://github.com/<your-username>/bitebytype.git
   cd bitebytype
   ```

2. **Create & activate a virtual environment**  
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate   # macOS/Linux
   .venv\Scripts\activate      # Windows
   ```

3. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

### Configuration

Streamlit uses a `secrets.toml` file to securely store API keys. Create `./.streamlit/secrets.toml` with:

```toml
# .streamlit/secrets.toml
SPOONACULAR_API_KEY = "your_spoonacular_api_key"
YELP_API_KEY       = "your_yelp_api_key"
```

### Running the App

```bash
streamlit run recipe.py
```

Then open the URL shown in your terminal (usually `http://localhost:8501`).

---

## Usage

1. **Choose a search mode**:  
   - **By Personality**: Select a trait & diet filter.  
   - **By Ingredient**: Enter an ingredient & max prep time.  
   - **By Nutrients**: Pick nutrient ranges & max prep time.  
2. **Enter your location** for restaurant recommendations (optional).  
3. **Click “Find Recipe”** and enjoy!

---

## Project Structure

```
bitebytype/
├── recipe.py             # Main Streamlit app
├── requirements.txt      # Python dependencies
├── .streamlit/
│   └── secrets.toml      # API keys (excluded from VCS)
└── README.md             # This file
```


