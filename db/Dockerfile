# Utilisation de l'image officielle PostgreSQL basée sur Alpine
FROM postgres:alpine

# Copier le script SQL d'initialisation
COPY words.sql /docker-entrypoint-initdb.d/words.sql

# Configurer l'authentification PostgreSQL
ENV POSTGRES_HOST_AUTH_METHOD=trust

# Optionnel : Si vous souhaitez définir d'autres variables d'environnement
# ENV POSTGRES_DB=your_database_name
# ENV POSTGRES_USER=your_username
# ENV POSTGRES_PASSWORD=your_password