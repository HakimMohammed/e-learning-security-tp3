FROM quay.io/keycloak/keycloak:23.0

# Copier le fichier de configuration du realm
COPY realms/elearning-realm.json /opt/keycloak/data/import/

# Configuration des variables d'environnement
ENV KEYCLOAK_ADMIN=admin
ENV KEYCLOAK_ADMIN_PASSWORD=admin

# Démarrer Keycloak avec l'import du realm
ENTRYPOINT ["/opt/keycloak/bin/kc.sh", "start-dev", "--import-realm"]