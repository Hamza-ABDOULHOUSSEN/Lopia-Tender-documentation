# Template twig

- [Template twig](#template-twig)
  - [modèle (modèle pour toutes les pages)](#modèle-modèle-pour-toutes-les-pages)
    - [base.html.twig](#basehtmltwig)
    - [navbar.html.twig](#navbarhtmltwig)
  - [registration](#registration)
    - [register.html.twig](#registerhtmltwig)
  - [security](#security)
    - [login.html.twig](#loginhtmltwig)
  - [Base](#base)
    - [index.html.twig](#indexhtmltwig)
  - [Acheteur](#acheteur)
    - [faire_une_demande.html.twig](#faire_une_demandehtmltwig)
    - [ajout_description_produit.html.twig](#ajout_description_produithtmltwig)
    - [consulter_demande.html.twig](#consulter_demandehtmltwig)
    - [detail_demande.html.twig](#detail_demandehtmltwig)
    - [consulter_offre.html.twig](#consulter_offrehtmltwig)
    - [detail_offre.html.twig](#detail_offrehtmltwig)
    - [outil_cco/liste_produits.html.twig](#outil_ccoliste_produitshtmltwig)
    - [outil_cco/recapitulatif.html.twig](#outil_ccorecapitulatifhtmltwig)
  - [Fournisseur](#fournisseur)
    - [consulter_demandes_recues.html.twig](#consulter_demandes_recueshtmltwig)
    - [faire_une_offre.html.twig](#faire_une_offrehtmltwig)
    - [ajout_produit_reel.html.twig](#ajout_produit_reelhtmltwig)

---


## modèle (modèle pour toutes les pages)

Ces pages forment la base de toutes les autres pages  
les éléments sont incluent dans toutes les pages

### base.html.twig

### navbar.html.twig
inclut :
- navbar/navbar.html.twig
- navbar/navbarAcheteur.html.twig
- navbar/navbarFournisseur.html.twig
- navbar/navbarSociete.html.twig

---

## registration

### register.html.twig
paramètre :
- registrationForm

---

## security

### login.html.twig
paramètre :
- last_username
- error

---

## Base

### index.html.twig

---

## Acheteur

### faire_une_demande.html.twig
paramètre :
- demandeForm
- demande_id
- descriptionProduits

inclut :
- liste_description_produit.html.twig

### ajout_description_produit.html.twig
paramètre :
- DescriptionProduitForm
- demande_id

### consulter_demande.html.twig
paramètre :
- demandeList

inclut :
- liste_demande.html.twig

### detail_demande.html.twig
paramètre :
- demande
- descriptionProduits

inclut :
- liste_description_produit.html.twig

### consulter_offre.html.twig
paramètre :
- offres

inclut :
- liste_offre.html.twig

### detail_offre.html.twig
paramètre :
- offre
- produitReels

inclut :
- liste_produit_reels.html.twig

### outil_cco/liste_produits.html.twig
paramètre :
- demande
- allProduit
- allProduitIntitule

### outil_cco/recapitulatif.html.twig
paramètre :
- demande
- allSelectedProduitByFournisseur

---

## Fournisseur

### consulter_demandes_recues.html.twig
paramètre :
- demandeListTraitee
- demandeListNonTraitee

inclut :
- liste_demande.html.twig

### faire_une_offre.html.twig
paramètre :
- offreForm
- demande_id
- offre_id
- descriptionProduits
- produitReels

inclut :
- liste_description_produit.html.twig
- liste_produit_reel.html.twig

### ajout_produit_reel.html.twig
paramètre :
- ProduitReelForm
- demande_id
- offre_id
- descriptionProduits
