# Using AI and SDN to Enhance the Security of IoT Networks

## Description
Ce projet utilise l'intelligence artificielle (IA) et les réseaux définis par logiciel (SDN) pour améliorer la sécurité des réseaux IoT. 
Le projet est déployé sur trois machines virtuelles (VM) distinctes:
1. **Contrôleur Ryu**
2. **Mininet**
3. **Environnement de test**

## Structure du projet
Le projet est organisé comme suit:

### 1. Contrôleur Ryu
Cette VM contient les scripts suivants:
- `collect_benign_traffic.py` : Script pour collecter le trafic bénin.
- `collect_ddos_traffic.py` : Script pour collecter le trafic DDoS.
- `controller.py` : Script principal du contrôleur Ryu.
- `DT_controller.py` : Script du contrôleur utilisant les arbres de décision.
- `FlowStatsfile.csv` : Fichier CSV pour les statistiques de flux.
- `ML.py` : Script pour le machine learning.
- `switch.py` : Script pour la gestion des commutateurs.

#### Packages nécessaires
pip install ryu pandas scikit-learn
### 2. Mininet
Cette VM contient les scripts suivants:

- `generate_benign_traffic.py` : Script pour générer du trafic bénin.
- `generate_ddos_traffic.py` : Script pour générer du trafic DDoS.
- `topology.py` : Script pour la topologie de réseau Mininet.
#### Packages nécessaires
pip install mininet
#### 3. Environnement de Test
Cette VM contient les scripts suivants pour l'application de visualisation:

- `main.py` : Script principal de l'application.
- `machine_learning.py` : Script pour les modèles de machine learning.
- `home.py` : Script pour la page d'accueil de l'application.
- `dashboard.py` : Script pour le tableau de bord.
- `controller.py` : Script pour le contrôleur de l'application.
#### Packages nécessaires
pip install flask dash scikit-learn pandas
#### Instructions de Déploiement
#### 1. Déploiement du Contrôleur Ryu
Cloner le dépôt sur la VM du contrôleur Ryu.
Installer les dépendances avec pip install -r requirements.txt.
Lancer le contrôleur avec python controller.py.
#### 2. Déploiement de Mininet
Cloner le dépôt sur la VM Mininet.
Installer Mininet avec sudo apt-get install mininet.
Générer le trafic bénin et DDoS avec python generate_benign_traffic.py et python generate_ddos_traffic.py.
Configurer la topologie avec python topology.py.
#### 3. Déploiement de l'Environnement de Test
Cloner le dépôt sur la VM de test.
Installer les dépendances avec pip install -r requirements.txt.
Lancer l'application de visualisation avec python main.py.
Utilisation
Contrôleur Ryu : Utilisez les scripts de collecte de trafic pour capturer les données de 
trafic et analysez-les avec les modèles de machine learning.
Mininet : Utilisez les scripts pour générer différents types de trafic et configurer la topologie réseau.
Environnement de Test : Utilisez l'application de visualisation pour surveiller et analyser les performances 
et la sécurité du réseau.