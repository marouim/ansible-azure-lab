# Comment provisionner le lab

### 1 - Creer un fichier de variable d'environnement pour l'authentification Azure

Créer un fichier nommé azure_credentials.sh avec le contenu suivant. Remplacer les [] par les vrais valeurs.
'''
export AZURE_CLIENT_ID=[Votre client ID]
export AZURE_TENANT=[Votre tenant ID]
export AZURE_SUBSCRIPTION_ID=[Votre subscription ID]
export AZURE_SECRET=[Votre secret ID]
'''

### 2 - Charger les variables d'environnement dans votre session

'''
source ./azure_credentials.sh
'''

### 3 - Lancer le playbook pour configurer l'environnement. 

La commande doit inclure le nom du "Pod" qui sera utilisé pour les noms des resources Azure.

'''
ansible-playbook bringup.yml --extra-vars "lab_id=pod1"
'''

