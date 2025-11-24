FROM node:18-bullseye

WORKDIR /wiki

# Installation de wget
RUN apt-get update && apt-get install -y wget

# Téléchargement et extraction
RUN wget https://github.com/Requarks/wiki/releases/latest/download/wiki-js.tar.gz
RUN tar xzf wiki-js.tar.gz

# --- LA CORRECTION ---
# On copie NOTRE fichier config.yml préparé à l'avance
COPY config.yml config.yml
# ---------------------

# On reconstruit la base de données SQLite pour être sûr (souvent nécessaire)
RUN npm rebuild sqlite3

EXPOSE 3000

CMD ["node", "server"]
