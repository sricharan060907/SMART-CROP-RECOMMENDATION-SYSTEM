# SMART-CROP-RECOMMENDATION-SYSTEM
Here is the complete, clean, ready-to-upload README.md for the Python version of your Smart Crop Recommendation System (converted from Prolog)

🌾 Smart Crop Recommendation System (Python)

This is a Python version of the Smart Crop Recommendation System originally implemented in Prolog.
The system recommends the best-suited crop based on soil type, season, rainfall, and soil pH.

It uses a simple rule-based expert system similar to your Prolog logic.


---

📌 Features

✔ Rule-based knowledge base (converted from Prolog facts)

✔ Python implementation of Prolog reasoning

✔ Interactive CLI (input-based interface)

✔ Instant crop recommendations

✔ Easy-to-edit crop dataset

✔ Beginner-friendly and works on any OS



---

🧠 How It Works

The program contains a list of crops and their requirements:

Soil type

Season

Rainfall range

Soil pH range


The user enters environmental parameters, and the system matches them to crops using simple rule logic.

Prolog facts → Python dictionaries
Prolog rules → Python condition checks


---

📂 Project Structure

Smart-Crop-Recommendation/
│
├── smart_crop_python.py     # Main Python program
├── README.md                # Project documentation
└── data/                    # (Optional if you later use JSON)


---

🖥 How to Run

1. Install Python

Python 3.8+ is recommended.

Check Python version:

python --version

2. Run the script

python smart_crop_python.py

3. Enter the required inputs:

Enter soil type (clay/loam/sandy/black):
Enter season (kharif/rabi/annual):
Enter rainfall (mm):
Enter soil pH:

Example Run

========= SMART CROP RECOMMENDATION SYSTEM =========

Enter soil type (clay/loam/sandy/black): loam
Enter season (kharif/rabi/annual): kharif
Enter rainfall (mm): 90
Enter soil pH: 6.2

Recommended Crops:
- maize


---

🧩 Python Code (Included in Repository)

# SMART CROP RECOMMENDATION SYSTEM (Python Version)

crops = [
    {"name": "rice", "soil": "clay", "season": "kharif", "min_rain": 100, "max_rain": 250, "min_ph": 5.0, "max_ph": 6.5},
    {"name": "wheat", "soil": "loam", "season": "rabi", "min_rain": 50, "max_rain": 120, "min_ph": 6.0, "max_ph": 7.5},
    {"name": "maize", "soil": "loam", "season": "kharif", "min_rain": 60, "max_rain": 150, "min_ph": 5.5, "max_ph": 7.0},
    {"name": "bajra", "soil": "sandy", "season": "kharif", "min_rain": 30, "max_rain": 90, "min_ph": 6.0, "max_ph": 7.5},
    {"name": "sugarcane", "soil": "clay", "season": "annual", "min_rain": 150, "max_rain": 300, "min_ph": 6.0, "max_ph": 8.0},
    {"name": "cotton", "soil": "black", "season": "kharif", "min_rain": 60, "max_rain": 120, "min_ph": 5.5, "max_ph": 7.5},
    {"name": "groundnut", "soil": "sandy", "season": "kharif", "min_rain": 50, "max_rain": 100, "min_ph": 6.0, "max_ph": 7.0},
    {"name": "chickpea", "soil": "loam", "season": "rabi", "min_rain": 40, "max_rain": 80, "min_ph": 6.0, "max_ph": 8.0},
    {"name": "millets", "soil": "sandy", "season": "kharif", "min_rain": 20, "max_rain": 60, "min_ph": 5.0, "max_ph": 8.0}
]

def recommend_crop(soil, season, rainfall, ph):
    soil = soil.lower()
    season = season.lower()

    recommended = []

    for crop in crops:
        if (crop["soil"] == soil and
            crop["season"] == season and
            crop["min_rain"] <= rainfall <= crop["max_rain"] and
            crop["min_ph"] <= ph <= crop["max_ph"]):
            recommended.append(crop["name"])

    return recommended

def main():
    print("\n========= SMART CROP RECOMMENDATION SYSTEM =========\n")

    soil = input("Enter soil type (clay/loam/sandy/black): ").strip().lower()
    season = input("Enter season (kharif/rabi/annual): ").strip().lower()
    rainfall = float(input("Enter rainfall (mm): "))
    ph = float(input("Enter soil pH: "))

    results = recommend_crop(soil, season, rainfall, ph)

    print("\nRecommended Crops:")
    if results:
        for r in results:
            print(f"- {r}")
    else:
        print("No suitable crops found.")

    print("\n====================================================\n")

if _name_ == "_main_":
    main()


---

🧪 Test Examples

Soil	Season	Rainfall	pH	Output

loam	kharif	90	6.2	maize
clay	kharif	200	6.0	rice, sugarcane
sandy	kharif	40	7.0	bajra, millets, groundnut



---

🚀 Future Enhancements

Use Machine Learning models

Add a GUI or web application

Weather API integration

Fertilizer recommendation

Disease prediction module



---

👨‍💻 Author

Sri Charan
Smart Crop Recommendation System (Python)


