# Utilisez une image de base Python
FROM python:3.9-slim

# Définir le répertoire de travail
WORKDIR /app

# Copier les fichiers nécessaires dans l'image Docker
COPY crypto_portfolio.py /app/crypto_portfolio.py
COPY db.py /app/db.py
COPY run.sh /app/run.sh
COPY requirements.txt /app/requirements.txt

# Installer les dépendances
RUN pip install --no-cache-dir -r requirements.txt

# Rendre le script de démarrage exécutable
RUN chmod +x /app/run.sh

# Définir le point d'entrée du conteneur
ENTRYPOINT ["/app/run.sh"]
