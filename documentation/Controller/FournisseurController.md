# FournisseurController

- [FournisseurController](#fournisseurcontroller)
  - [consulter_demandes_recues](#consulter_demandes_recues)
  - [faire_une_offre](#faire_une_offre)
  - [ajout_produit_reel](#ajout_produit_reel)

## consulter_demandes_recues
Route permettant de consulter les demandes reçues  
on charge toutes les demandes validées  
on affiche les demandes avec une partie pour les demandes non traitées et une partie pour les demandes traitées  

template associés:
- [Fournisseur/consulter_demandes_recues.html.twig](../Template.md)

## faire_une_offre
Route permettant de faire une offre pour la demande choisie  
on charge toutes les demandes validées  
on commence par recharger l'entité offre si une offre a été faite sans avoir été validée sinon on crée une offre NON_ENREGISTREE  
on crée le formulaire permettant de valider l'offre  

template associés:
- [Fournisseur/faire_une_offre.html.twig](../Template.md)

## ajout_produit_reel
Route permettant d'ajouter des produits réels dans une offre  
on crée le formulaire pour ajouter un ProduitReel  
s'il est rempli, on ajoute le produit  
il faut bien choisir la descriptionProduit associé au ProduitReel à insérer  (pour l'outil CCO)

template associés:
- [Fournisseur/ajout_produit_reel.html.twig](../Template.md)



