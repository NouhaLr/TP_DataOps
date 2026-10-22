Q1
	requirements.txt liste les bibliothèques et leurs versions. Votre binôme, une autre machine ou un serveur peuvent alors tout réinstaller à l’identique avec une seule commande. Avec un pip install pandas tapé à la main, personne ne sait quelles versions vous avez. C’est la reproductibilité.
Q2
	8 lignes au lieu de 5. Python voit Tunisia, tunisia, Tunisia (avec un espace), Morocco et MOROCCO comme des pays différents.
Q3
	Voir le tableau ci-dessous.
Q4
	Trop haut. Presque tous les problèmes ajoutent de l’argent qui ne devrait pas être là : doublon, prix aberrant, lignes invalides. Un seul retire de l’argent, la quantité négative, et c’est une toute petite somme (−39,80). On le devine sans tout recalculer.
Q5
	(1) On peut tester chaque fonction seule. (2) Quand ça casse, on sait quelle étape est en cause. On peut aussi réutiliser ou remplacer une étape sans toucher aux autres.
Q6
	Le bon total est 7 655,90. L’ancien script disait 12 771,10, soit 5 115,20 de trop, une erreur de +66,8 % par rapport au vrai total.
Q7
	La commande 1019 : un clavier à 4 500 au lieu de 45. Elle pèse 4 500 sur 5 115 d’erreur, soit environ 88 %. La règle 4 (invalid_unit_price) l’a attrapée.
Q8
	Supprimer en silence, c’est retomber dans l’erreur silencieuse. Le fichier de quarantaine permet de comprendre pourquoi, de corriger à la source, de compter les rejets et de prouver ce qui a été exclu.
Q9
	Avec > -5, la quantité −2 passe le contrôle. test_negative_quantity_is_rejected échoue, car la commande 1 reste dans les lignes propres. Le test a donc détecté votre bug.
Q10
	Un test unitaire vérifie que mon code est juste, sur un petit tableau écrit à la main. Un contrôle de données vérifie que les données du jour sont acceptables, sur les vraies données.
Q12
	Jour 2 : les prix sont multipliés par 100 (44900 au lieu de 449), probablement en centimes. Jour 3 : la colonne unit_price a été renommée en price.
Q13
	Le jour 2 est le plus dangereux. L’ancien script affiche un rapport d’apparence normale mais 100 fois trop grand, sans aucune alerte, et le directeur peut décider sur ce chiffre. Le jour 3, il plante, donc tout le monde le voit.
Q14
	Tout programme qui lance le pipeline : un planificateur (cron, Airflow), la CI GitHub Actions ou un script shell. Il lit le code de sortie 1 et sait que le pipeline a échoué. Il peut alors ne pas publier, alerter l’équipe ou lancer une relance.