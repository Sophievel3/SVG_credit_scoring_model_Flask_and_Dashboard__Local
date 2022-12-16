SVG_credit_scoring_model
            
            
                       I M P L E M E N T A T I O N   D'U N   M O D E L E   D E   S C O R E 
                         (Déploiement en local des parties Flask et Dashboard-Streamlit).




---------------------------------------------------------------------------------------------------------

On retrouve ici tous les fichiers pour:
- Déployer en local les parties Flask et Dashboard-Streamlit.

-----------------
Procédure à suivre pour le déploiement en local:

- Mettre tout le contenu de ce repository dans un même dossier. 
- Lancer ensuite d'abord le code "P7_Sofia_Velasco_1_Flask_Local", sur python (ie. intoduire dans le prompt python -une fois dans le dossier correspondant- la commande:  python P7_Sofia_Velasco_1_Flask_Local.py).

Une url de la forme: 'http://192.168.43.52:81/' apparaîtra alors dans votre prompt python. C'est le 'localhost' dont les premiers chiffres changent en fonction du wifi dans lequel on est connectés.
- Dans le code "P7_Sofia_Velasco_1_Dashboard_Local", changer 3 fois (ie. lignes 42,44 et 53), le 'localhost' dans les URL affichées (ie. avant 'app/...') et mettre le localhost en cours. 
- Lancer ensuite le code "P7_Sofia_Velasco_1_Dashboard_Local", en écrivant sur le prompt python la commande:  streamlit run P7_Sofia_Velasco_1_Dashboard_Local.py .

Sur l'explorateur s'ouvrira alors une page qui, travaillant sur le serveur local, montrera le Dashboard-Streamlit.
- Introduire un des ID, et faire clic sur "Explain Results". Seront alors déployés: le score su client, les Features Importances Globales du modèle et les Features Importances Locales du client.
---------------------------------------------------------------------------------------------------------


INVENTAIRE DES FICHIERS PRESENTS:

1. Un dossier "templates"--> On y trouve le fichier "index.html", utilisé sur Flask pour afficher les résultats de LIME.

2. .gitattributes --> Document permettant d'utiliser Git LFS pour les fichiers des bases de données trop lourds.

3. Base_complete.zip --> La base des données entière suite à tous ces traitements (train+test). (ie. Avec l'information de tous les clients, en format zip pour prendre moins de mémoire sur github). 

4. P7_Sofia_Velasco_1_Dashboard --> Code utilisé pour faire le Dashboard sur Streamlit.

5. P7_Sofia_Velasco_1_Flask_Local.py --> Code Flask (tournant en local). 

6. expl_pkl --> Le explainer résultant de l'analyse "LIME" de notre meilleur modèle.

7. global_pkl --> Les "Global Features Importances" de notre meilleur modèle.

8. model_pkl --> le meilleure modèle (LGBMClassifier), avec les meilleures hyperparamètres, entraîné et sauvegardé à l'aide du packaging "Pickle".

9. X_train_req_saved --> La base qui a servi pour entraîner et tester le modèle. (Celle ré-équilibrée avec SMOTE, en format zip pour prendre moins de mémoire sur github).

---------------------------------------------------------------------------------------------------------

