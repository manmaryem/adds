# Active Directory (Ad DS)

# Installation d'un contrôleur de domaine Active Directory sur Windows Server 2012 R2

- La mise en place d'un contrôleur de domaine Active Directory sur Windows Server 2012 R2 et la création d'un domaine "wilders.lan"

## Étape 1 : Installation du rôle AD DS

1. je me connnecte à machine virtuelle Windows Server 2012 R2 celle déja utilisé et configuré pour le DHCP et DNS.

2. Ouvrer le Gestionnaire de serveur en cliquant sur l'icône de gestionnaire de serveur dans la barre des tâches.

3. cliquez sur "Gérer" dans le coin supérieur droit, puis sélectionnez "Ajouter des rôles et fonctionnalités".
   
5. ![image](https://github.com/manmaryem/adds/assets/137881827/ba6136f1-8331-4227-acd3-220c7eb734b4)


6. Suivez l'Assistant "Ajouter des rôles et fonctionnalités" en cliquant sur "Suivant" jusqu'à l'étape "Sélectionner des rôles de serveur". Cochez la case "Services AD DS" pour installer Active Directory Domain Services, puis cliquez sur "Suivant".

7. À l'étape suivante, cliquez sur "Suivant" pour accepter les fonctionnalités requises. Continuez en cliquant sur "Suivant" jusqu'à l'étape "Sélectionner les rôles de serveur", où vous verrez le rôle AD DS. Cliquez à nouveau sur "Suivant".

8. Lister et lire les informations sur le rôle AD DS, puis cliquez sur "Suivant".

9. À l'étape "Confirmer les sélections d'installation", cliquez sur "Installer". L'Assistant d'installation va maintenant installer le rôle AD DS sur votre serveur.

10. Une fois l'installation terminée, cliquez sur "Fermer" pour quitter l'Assistant.

11. ![image](https://github.com/manmaryem/adds/assets/137881827/5480be49-6bb2-43b2-8a4d-0346328cc36d)


## Étape 2 : Configuration d'Active Directory

1. Après avoir installé le rôle AD DS, un indicateur jaune apparaîtra dans le coin supérieur droit du Gestionnaire de serveur. Cliquez sur cet indicateur et sélectionnez "Promouvoir ce serveur en contrôleur de domaine".

2. Dans l'Assistant de promotion du contrôleur de domaine, sélectionnez "Ajouter une nouvelle forêt" car nous allons créer un nouveau domaine.

4. Dans la section "Nom de la forêt racine", entrez "wilders.lan" comme nom de domaine racine. Assurez-vous que la case "Niveau fonctionnel de la forêt" est définie sur "Windows Server 2012 R2". Cliquez sur "Suivant".

5. 3. ![image](https://github.com/manmaryem/adds/assets/137881827/051b632c-e748-49e6-9e98-4074cfa4e4cb)

6. À l'étape suivante, on laisse le nom NetBIOS du domaine tel quel (il sera généralement généré automatiquement à partir du nom de domaine). Cliquez sur "Suivant".

7. Configurez les emplacements des fichiers de base de données, on laisse les valeurs par défaut. Cliquez sur "Suivant".

8. Définissez un mot de passe pour le mode de restauration du service d'annuaire. Cliquez sur "Suivant".

9. ![image](https://github.com/manmaryem/adds/assets/137881827/0eb8f94b-eef2-4898-a661-e6f61438703a)


10. Revérifiez vos paramètres, puis cliquez sur "Suivant" pour commencer la configuration d'Active Directory.

11. ![image](https://github.com/manmaryem/adds/assets/137881827/a22b0003-dbb2-4003-b297-cb57ccbfc57f)


13. Une fois la configuration terminée, cliquez sur "Terminer" pour redémarrer le serveur en tant que contrôleur de domaine.

Après le redémarrage, le contrôleur de domaine Active Directory est fonctionnel avec le domaine "wilders.lan" créé. on peux maintenant gérer les utilisateurs, les groupes, à l'aide de l'outil "Utilisateurs et ordinateurs Active Directory" et d'autres outils d'administration Active Directory.

![image](https://github.com/manmaryem/adds/assets/137881827/97198d7d-e134-487c-ad6a-1386243772bf)

![image](https://github.com/manmaryem/adds/assets/137881827/3423099d-531f-477d-bcc1-95ddd4b503c9)

