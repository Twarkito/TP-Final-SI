# On part d'une version Debian de Node pour pouvoir installer des outils
FROM node:18-bullseye

# Création du dossier de travail
WORKDIR /wiki

# ÉTAPE AJOUTÉE : Installation de wget (c'est souvent ça qui manque)
RUN apt-get update && apt-get install -y wget

# Téléchargement de Wiki.js
RUN wget https://github.com/Requarks/wiki/releases/latest/download/wiki-js.tar.gz

# Extraction de l'archive
RUN tar xzf wiki-js.tar.gz

# Renommage du fichier de config
RUN mv config.sample.yml config.yml

# Exposition du port
EXPOSE 3000

# Lancement
CMD ["node", "server"]
