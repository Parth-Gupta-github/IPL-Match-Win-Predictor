# IPL Match Win Predictor

IPL Match Win Predictor is a Streamlit web app that predicts the winning probability of an IPL team during a run chase. The app uses a trained machine learning pipeline saved in `pipe.pkl` and takes live match inputs such as batting team, bowling team, city, target, score, overs, and wickets.

## Features

- Predicts win probability for the batting and bowling teams.
- Simple Streamlit user interface.
- Uses match situation inputs from the second innings.
- Loads a pre-trained machine learning model from `pipe.pkl`.
- Includes IPL teams and host cities supported by the trained model.

## Project Structure

```text
IPL-Match-Win-Predictor/
|-- app.py
|-- pipe.pkl
|-- matches.csv
|-- deliveries.csv
|-- ipl-win-predictor.ipynb
|-- requirements.txt
`-- README.md
```

## Requirements

- Python 3.10 or newer
- pip
- Virtual environment support through `venv`

Python 3.13.5 was used during local setup.

## Setup

Open PowerShell in the project folder and run:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

If PowerShell blocks activation scripts, run this command in the same terminal:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Then activate the virtual environment again:

```powershell
.\.venv\Scripts\Activate.ps1
```

## Run The App

Start the Streamlit app with:

```powershell
streamlit run app.py
```

Open the local URL shown in the terminal. It is usually:

```text
http://localhost:8501
```

Keep the terminal open while using the app. To stop the server, press `Ctrl+C`.

## How To Use

1. Select the batting team.
2. Select the bowling team.
3. Select the host city.
4. Enter the target score.
5. Enter the current score.
6. Enter completed overs.
7. Enter wickets lost.
8. Click `Predict Probability`.

The app will show the predicted winning probability for both teams.

## Model And Data

- `pipe.pkl` contains the trained prediction pipeline.
- `matches.csv` and `deliveries.csv` contain IPL match and ball-by-ball data.
- `ipl-win-predictor.ipynb` contains the notebook used for data exploration, feature engineering, and model training.

## Troubleshooting

If dependencies are missing, reinstall them:

```powershell
python -m pip install -r requirements.txt
```

If `streamlit` is not recognized, make sure the virtual environment is active:

```powershell
.\.venv\Scripts\Activate.ps1
```

If the model fails to load, verify that `pipe.pkl` is present in the same folder as `app.py`.
