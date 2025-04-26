# 📊 Social Media Engagement Predictor

Un modèle de Deep Learning pour prédire la popularité des publications sur les réseaux sociaux (likes, partages) en fonction de leurs métadonnées.

## 🚀 Fonctionnalités
- Prédiction du nombre de likes/partages avec un réseau de neurones
- Preprocessing complet (one-hot encoding, normalisation)
- Visualisation des corrélations entre features
- Évaluation des performances (RMSE, R²)

## 🧠 Données

**Dataset** : `sentimentdataset.csv`  

**Features clés** :  
- `Retweets` : Nombre de partages initiaux  
- `Timestamp` : Date/heure de publication  
- `Sentiment` : Analyse de sentiment (Positive/Negative/Neutral)  
- `Platform` : Réseau social source  

**Target** :  
- `Likes` : Nombre de likes à prédire  

## 🛠️ Utilisation

### Entraînement du modèle :
```python
python src/train.py --data_path data/sentimentdataset.csv --epochs 50.
    
```

##  Prédiction

from src.predict import predict_engagement

result = predict_engagement(
    retweets=15,
    year=2023,
    month=6,
    day=15,
    hour=14,
    sentiment="Positive",
    platform="Twitter"
)
print(f"Likes prédits : {result:.0f}")

```


