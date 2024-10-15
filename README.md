# ESGI test FYC project

Auth : Express JS, très simple sans bdd
Frontend : Vuejs + axios + lint, injection de l'URL au Nginx
Serveur Backend : Django + linter ruff + une vue qui renvoi l'heure
Serveur Nginx : Routage aux autres services + Authentification

lancable avec docker-compose ou bien avec tilt.
Pour tilt vous devez l'installer, installer kind pour avoir un kube en local et ctlptl pour créer un cluster kind avec un registre d'images local, plus globalement il y a besoin de kubectl pour intéragir avec kind
 
