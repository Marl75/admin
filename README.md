# Suivi d'utilisation

Page d'administration commune à mes applis : **[marl75.github.io/admin](https://marl75.github.io/admin/)**

- Un onglet par appli : [Collection](https://marl75.github.io/mes-livres/) et [Routine](https://marl75.github.io/fitness-coach/), plus un onglet **Site** pour [marlenemenoire.com](https://marlenemenoire.com/)
- L'onglet Site lit les visiteurs mesurés par [GoatCounter](https://marlenemenoire.goatcounter.com) (sans cookie) via son compteur public : aucune clé dans la page, réglage « Allow adding visitor counts on your website » à cocher côté GoatCounter
- Chaque appli a son propre projet Firebase ; la page se connecte aux deux avec le même e-mail et mot de passe
- Les statistiques (`usage/{uid}` dans chaque projet) ne sont lisibles que par l'administratrice, grâce aux règles Firestore de chaque projet ; si l'accès n'est pas encore autorisé, la page affiche les règles à coller dans la console Firebase
- Un onglet **Retours** rassemble les messages « Une idée, un souci ? » envoyés depuis les applis (pour l'instant Routine : collection `feedback`), avec leur contexte (version, écran, langue, navigateur) et un statut Nouveau / À traiter / Fait
- Aucune donnée n'est stockée dans ce dépôt : la page lit tout en direct depuis Firebase
