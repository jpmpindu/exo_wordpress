# Projet WordPress via Docker

Ce projet permet de lancer un site WordPress **prêt à l’emploi** avec Docker Compose.
Il inclut : WordPress, MySQL et phpMyAdmin.

---

## Prérequis

- Installer [Docker Desktop](https://www.docker.com/products/docker-desktop) (Mac, Windows ou Linux)
- Avoir téléchargé ou cloné ce projet sur ton ordinateur

---

## Étapes pour lancer le projet

1️⃣ Ouvrir un terminal et naviguer vers le dossier du projet :

```bash
cd /exo_wordpress
```

2️⃣ Lancer les conteneurs Docker :

```bash
docker compose up -d
```

> L’option `-d` lance les conteneurs en arrière-plan.

3️⃣ Vérifier que les conteneurs tournent :

```bash
docker compose ps
```

---

## Accéder au site WordPress

- Ouvrir un navigateur et aller sur :  
```
http://localhost:8000
```
- Suivre l’installation WordPress (nom du site, admin, mot de passe, etc.)

---

## Accéder à phpMyAdmin (facultatif)

- Ouvrir :  
```
http://localhost:8080
```
- Identifiants :
  - Serveur : `db`
  - Utilisateur : `wpuser`
  - Mot de passe : `wppass`

---

## Arrêter le projet

```bash
docker compose down
```

> Cette commande arrête et supprime les conteneurs mais **les données restent** grâce aux volumes Docker.

---

## Notes importantes

- Les fichiers WordPress sont dans le dossier `wp_data`
- La base de données MySQL est stockée dans le dossier `db_data`
- Pour changer la version de WordPress, modifier l’image dans `docker-compose.yml` :

```yaml
image: wordpress:6.4
```

---

💡 **Astuce :** Si ton navigateur ne charge pas `http://localhost:8000`, vérifier que Docker Desktop est bien lancé et que les ports ne sont pas utilisés par une autre application.

# brad-local-site
# exo_wordpress
# exo_wordpress
