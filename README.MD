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

## Analyse des fichiers :

### Fichier_erg :
'product_id' = identifiant de tout les produits de l'entreprise         
'onsale_web' = produit disponible en ligne (1=True)                     
'price' = Prix du produit                                               
'stock_quantity' = Quantité de produit disponible                       
'stock_status' = Produit en stock (instock)                             

### Fichier_web :
'sku' : Identifiant unique associé à un produit.
'virtual' : Indique si le produit est virtuel (peut-être utilisé pour des produits numériques, sans expédition physique).
'downloadable' : Indique si le produit est téléchargeable.
'rating_count' : Nombre de notes ou évaluations données au produit.
'average_rating' : Note moyenne attribuée au produit.
'total_sales' : Nombre total d'articles vendus.
'tax_status' : Indique si une taxe est applicable au produit.
'tax_class' : Le type de taxe appliqué.
'post_author' : ID de l'auteur du post.
'post_date' : Date et heure de création du post (heure locale).
'post_date_gmt' : Date et heure de création du post (heure universelle).
'post_content' : Contenu complet de l'article.
'post_title' : Titre de l'article.
'post_excerpt' : Un extrait du contenu qui donne envie de consulter l'article entier.
'post_status' : Statut de publication de l'article (publié ou non).
'comment_status' : Statut des commentaires (activés ou désactivés).
'ping_status' : Statut des notifications (activées ou désactivées).
'post_password' : Mot de passe nécessaire pour accéder à l'article.
'post_name' : Nom du post (partie de l'URL conviviale pour le référencement).
'post_modified' : Date et heure de la dernière modification de l'article (heure locale).
'post_modified_gmt' : Date et heure de la dernière modification de l'article (heure universelle).
'post_content_filtered' : Éventuellement utilisé pour stocker une version filtrée du contenu.
'post_parent' : ID du post parent (utilisé dans les types de contenu hiérarchiques).
'guid' : Lien de l'article.
'menu_order' : Ordre d'affichage dans les menus (peut être utilisé pour trier).
'post_type' : Type de post (par exemple, 'post', 'page', 'product' pour WooCommerce).
'post_mime_type' : Type MIME du fichier attaché (le cas échéant).
'comment_count' : Nombre de commentaires associés à l'article.

### Fichier_web :
'product_id' = identifiant de tout les produits de l'entreprise         
'sku' = identifiant des produits mis en ligne

