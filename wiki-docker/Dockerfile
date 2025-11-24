# Basé sur Node.js (requis par Wiki.js)
FROM node:18

# Création du dossier de travail
WORKDIR /wiki

# Téléchargement de la dernière version de Wiki.js
RUN wget https://github.com/Requarks/wiki/releases/latest/download/wiki-js.tar.gz

# Extraction de l'archive
RUN tar xzf wiki-js.tar.gz

# Copie et renommage du fichier de config exemple
RUN mv config.sample.yml config.yml

# Exposition du port 3000 (port par défaut de Wiki.js)
EXPOSE 3000

# Commande de lancement
CMD ["node", "server"]
