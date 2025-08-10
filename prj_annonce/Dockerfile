# Utiliser une image officielle Python légère
FROM python:3.11-slim

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier les fichiers requirements.txt
COPY requirements.txt .

# Installer les dépendances
RUN pip install --no-cache-dir -r requirements.txt

# Copier le reste du code source dans le conteneur
COPY . .

# Exposer le port que Django utilisera (par défaut 8000)
EXPOSE 8000

# Commande pour lancer le serveur de développement Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
