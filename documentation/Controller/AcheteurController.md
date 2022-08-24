# AcheteurController

- [AcheteurController](#acheteurcontroller)
  - [faire_une_demande](#faire_une_demande)
  - [ajout_description_produit](#ajout_description_produit)
  - [consulter_demande](#consulter_demande)
  - [detail_demande](#detail_demande)
  - [supprimer_demande](#supprimer_demande)
  - [consulter_offre](#consulter_offre)
  - [detail_offre](#detail_offre)
  - [outil_cco](#outil_cco)
  - [recapitulatif](#recapitulatif)


## faire_une_demande
Route permettant de faire une nouvelle demande  
on commence par recharger l'entite demande si une demande a été faite sans avoir été validée sinon on cree une demande NON_ENREGISTREE  
on creer le formulaire permettant de valider la demande

template associés:
- [Acheteur/faire_une_demande.html.twig](../Template.md)


## ajout_description_produit
Route permettant d'ajouter des descriptions de produit dans une demande  
on cree le formulaire pour ajouter une descriptionProduit  
s'il est rempli, on ajoute la description de produit

template associés:
- [Acheteur/ajout_description_produit.html.twig](../Template.md)

## consulter_demande
Route permettant de consulter toutes ses demandes 
on affiche la liste des demandes de l'utilisateur  
depuis cette liste, un utilisateur peut
 - voir les details d'une demande
 - supprimer une demande
 - voir les offres pour une demande
 - utiliser l'outil CCO pour une demande

template associés:
- [Acheteur/consulter_demande.html.twig](../Template.md))

## detail_demande
Route permettant de consulter les produits contenus dans une demande  
on n'affiche la liste des produits de la demande

template associés:
- [Acheteur/detail_demande.html.twig](../Template.md)

## supprimer_demande
Route permettant de supprimer une demande  
attention tous les produits et les offres associés à cette demande seront supprimées  

## consulter_offre
Route permettant de consulter les offres faites pour une demande  
on n'affiche la liste des offres  

template associés:
- [Acheteur/consulter_offre.html.twig](../Template.md)

## detail_offre
Route permettant de consulter les produits proposés dans une offre  
on n'affiche la liste des produitReels  

template associés:
- [Acheteur/detail_offre.html.twig](../Template.md)

## outil_cco
Route permettant d'utiliser l'outil cco sur une offre  
l'outil affiche tous les produitsReels proposés dans toutes les offres proposées pour cette demande   
les produitsReels sont triés par DescriptionProduit:  
pour chaque DescriptionProduit, on affiche les ProduitsReels associés  
la page contient un formulaire, on sélectionne les produits à traité et on lance l'outil  
cela renvoie vers la page recapitulatif  

template associés:
- [Acheteur/outil_cco/liste_produits.html.twig](../Template.md)

## recapitulatif
Route permettant de voir le recapitulatif de l'outil cco  
on récupère la liste des produitReel envoyés avec la méthode POST  
on remplit le tableau $allSelectedProduit qui contient pour chaque descriptionProduit, le ProduitReel associé le moins chere  
on affiche le recapitulatif triés par fournisseur (cela permet de voir toutes les commandes à effectuer)  

template associés:
- ['Acheteur/outil_cco/recapitulatif.html.twig'](../Template.md)
