# TP32 
### Objectifs pédagogiques
* Mettre en place Jenkins et configurer les outils (JDK, Maven, SonarScanner).
* Déployer SonarQube via Docker Compose et créer des projets + tokens par microservice.
* Exposer Jenkins avec Ngrok et brancher GitHub via webhooks.
* Créer un job Pipeline Jenkins et écrire un script de pipeline multi-stages.
* Lancer/valider l’exécution (Jenkins, SonarQube, Docker) et vérifier le déclenchement par push.

### Prérequis techniques (outils)
* JDK 17 (ou version compatible avec le projet) + variable JAVA_HOME.
* Maven (installé localement ou géré par Jenkins).
* Git (ligne de commande).
* Docker + Docker Compose.
* Jenkins (installation locale).
* SonarQube (déployé via Docker Compose) + PostgreSQL (dans le compose).
* Ngrok (compte + authtoken).
* Un compte GitHub (accès au dépôt du projet).


### Prérequis de connaissances
* Git : clone, commit, push, notion de webhook.
* Java/Spring Boot : structure d’un projet, build Maven.
* Notions CI/CD : stages (build, analyse, déploiement), exécution automatique.

### Contexte et architecture
L’application est composée de 4 microservices : car, client, gateway, server_eureka (Eureka Server). Le pipeline CI/CD assure :
* **CI :** compilation Maven + analyse SonarQube (qualité, code smells, bugs, vulnérabilités).
* **CD :** déploiement des services dans des conteneurs via Docker Compose.
* **Automatisation :** Jenkins exécute le pipeline à chaque push/pull request via webhook GitHub exposé par Ngrok.

<img width="322" height="220" alt="image" src="https://github.com/user-attachments/assets/84f185a0-c99b-4e05-8ffa-d21ee7baeae4" />

### Exécution : 
<img width="479" height="249" alt="Capture d&#39;écran 2025-12-15 091403" src="https://github.com/user-attachments/assets/ad837543-2503-4ad2-8f93-d2895dda95b9" />
<img width="690" height="439" alt="Capture d&#39;écran 2025-12-15 092155" src="https://github.com/user-attachments/assets/60e47113-f146-4e1b-8a49-63f3d847089b" />
<img width="960" height="501" alt="Capture d&#39;écran 2025-12-15 092936" src="https://github.com/user-attachments/assets/d166d8b0-7883-4c71-ad5d-129db6229110" />
<img width="960" height="502" alt="Capture d&#39;écran 2025-12-15 093019" src="https://github.com/user-attachments/assets/3c846700-60d9-4242-aaac-0ee6aafe86e8" />
<img width="960" height="470" alt="Capture d&#39;écran 2025-12-15 105146" src="https://github.com/user-attachments/assets/c6d30882-f25a-4c16-bc56-18052872f740" />
<img width="960" height="469" alt="Capture d&#39;écran 2025-12-15 105610" src="https://github.com/user-attachments/assets/6c49a35f-d484-4240-9e16-a7c6b68b7690" />
<img width="960" height="469" alt="Capture d&#39;écran 2025-12-15 110517" src="https://github.com/user-attachments/assets/62d1dd1e-f617-4111-a7ff-d0eaae3d5419" />
<img width="960" height="471" alt="Capture d&#39;écran 2025-12-17 095837" src="https://github.com/user-attachments/assets/4d9e0c50-a859-4ee1-b236-0293b59580e4" />
<img width="959" height="472" alt="Capture d&#39;écran 2025-12-17 124009" src="https://github.com/user-attachments/assets/880263ae-e401-4408-a858-89bf0acbcde1" />
<img width="960" height="467" alt="Capture d&#39;écran 2025-12-17 200635" src="https://github.com/user-attachments/assets/63561488-fda9-4a09-8851-7bef05a66e36" />
<img width="1907" height="844" alt="image" src="https://github.com/user-attachments/assets/bc5e0918-0416-429d-a8d1-8e560b821919" />
<img width="960" height="417" alt="image" src="https://github.com/user-attachments/assets/b477ad09-66b1-4e82-b971-4a98fcefcfd9" />
<img width="960" height="504" alt="image" src="https://github.com/user-attachments/assets/a07add5c-6d05-4d48-84ea-69d1935c2d46" />







