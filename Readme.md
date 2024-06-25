Projet Ansible d'installation des outils sur un serveur distant.

Vérifier la configuration du fichier inventory.ini à la racine du projet pour assurer l'accès au conteneur vm-ubuntu-install

A la racine de ce projet lancer

ansible-playbook -i inventory.ini copy-config-playbook.yaml --ask-become-pass --ask-vault-pass

Les credentials sont: 
become-pass=test
vault-pass=secret

Le projet DevOps-Project-Ansible sera copié par 'copy-config-playbook.yaml' dans le répertoire /home/test du contenaur vm-ubuntu-install

Se connecter sur le conteneur vm-ubuntu-install

Aller dans /home/test/DevOps-Project-Ansible

Vérifier les droits d'exécution et d'écriture sur les fichiers et le répertoire config-vm-ubuntu-devops du projet

Aller dans DevOps-Project-Ansible

Lancer la commande d'installation des docker, jenkins, postgres et sonarqube

ansible-playbook -i inventory.yaml playbook.yaml --ask-become-pass --ask-vault-pass

Les credentials sont: 
become-pass=test
vault-pass=secret

Vérifier que l'installation est bien passée et que les conteneurs docker, jenkins, postgres et sonarqube sont up

Configurer sonarqube et jenkins. Créer le node agent_reactjs_node de jenkins 
suivre le README.md du projet https://github.com/lauboudou/DevOps-CI-CD-Project.git

Installer le node agent_reactjs_node

Dans le répertoire :  /home/test/DevOps-Project-Ansible/config-vm-ubuntu-devops
Lancer la commande suivante:

ansible-playbook -i inventory.yaml playbook.yaml --ask-become-pass --ask-vault-pass

Les credentials sont: 
become-pass=test
vault-pass=secret

Vérifier que le conteneur agent_reactjs_node est bien installé et démarré
Vérifier sur le serveur jenkins que le node agent_reactjs_node est bien démarré

Configuré un pipeline et les credentials nécéssaires et effectuer un test avec un projet git

Comme exemple de projet : https://github.com/lauboudou/horoscope-zodiac-js.git

