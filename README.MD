# Petites notes :

## Objectif : 
Améliorer la gestion des stocks,
Analyser les ventes de la boutique
Améliorer l'accès au back-office pour les employés
Centraliser un maximum les informations

## Bonnes Pratiques :
- Attention aux problèmes d'encoding excel -> csv (UTF8)
- Unicité des clés (SKU pour le WEB // Product_id pour le ERP)
- Vérifier les joitures (quel typo, clé,...)
- Pour chaque modification ou suppression de données, justification obligatoire

## Notes supplémentaires : 
Minimum 5 incohérence à relever sur le projet 

- Après exploration et nettoyage des données, calculer le CA par produit et le CA total

- Possible erreurs de saisie (prix produit) -> valeurs abérante + faire représentation graphique

## Mes théories : 

- Le fichier de Sylvie contient toutes les références produit de l'entreprise ainsi que les références produits de la boutique en ligne. Certaines références produit de l'entreprise n'ont pas de correspondance avec les références en ligne.

Je me demande si ce n'est pas simplement parce que toute les référence de l'entreprise ne se trouve pas sur internet (Certaines références sont commercialisé Off-Line).

-> indice 1 : Sur le fichier ERP, la colonne onsale_web n'a que deux valeurs possible : 1 et 0 (1 étant un produit commercialisé en ligne et 0 n'étant pas commercialisé en ligne)
