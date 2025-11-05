# Movie Recommendation Engine

A sophisticated movie recommendation system built with Django and Scikit-Surprise, leveraging collaborative filtering to provide personalized movie suggestions based on user ratings.

## 🚀 Features

- User-based collaborative filtering using SVD (Singular Value Decomposition)
- Web interface for easy interaction
- Top 5 movie recommendations based on user history
- Integration with a comprehensive movie database
- Fast predictions using pre-trained models

## 📋 Prerequisites

- Python 3.x
- Django 2.1.10
- pandas 1.3.3
- scikit-surprise 1.1.1
- fastparquet 0.7.1

## 🛠️ Installation

1. Clone the repository:
```bash
git clone https://github.com/mounimRhouli/mounimRhouli-Movie-Recommendation-Engine.git
cd MovieRecommendations
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

4. Run database migrations:
```bash
python manage.py migrate
```

5. Start the development server:
```bash
python manage.py runserver
```

## 🎯 Usage

1. Access the web interface at `http://localhost:8000`
2. Enter a user ID to get personalized movie recommendations
3. View the top 5 recommended movies along with their estimated ratings

## 📂 Project Structure

```
MovieRecommendations/
├── MovieDjango/              # Project configuration
├── MovieName/                # Main application
│   ├── data/                # Dataset files
│   │   ├── movies.csv
│   │   └── ratings2.csv
│   ├── templates/           # HTML templates
│   │   ├── base.html
│   │   ├── input_form.html
│   │   └── recommendations.html
│   ├── models.py           # Data models
│   ├── views.py            # View logic
│   └── urls.py             # URL routing
├── requirements.txt        # Project dependencies
└── manage.py              # Django management script
```

## 🔧 Technical Details

- Uses the SVD algorithm from Scikit-Surprise for collaborative filtering
- Pre-trained model saved using pickle for faster predictions
- Parquet file format for efficient data storage and retrieval
- Django forms for input validation and processing

## 🚢 Docker Support

The project includes Docker support for easy deployment:

```bash
docker build -t movie-recommender .
docker run -p 8000:8000 movie-recommender
```

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## ⭐ Acknowledgments

- Movie dataset provided by MovieLens
- Built with Django web framework
- Powered by Scikit-Surprise recommendation system library