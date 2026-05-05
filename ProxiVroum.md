Enonce : ProxiVroum

Vous concevez ProxiVroum, plateforme de covoiturage regionale.

Acteurs ; Conducteur, Passager, Moderateur, Service Compatibilite.

Fonctionnalite : Publication d'un trajet, recherche, reservation, paiement, notation apres trajet,
support en cas de lititge, statistiques Moderateur, exports comptables.

Contraintes : pic de chare le vendredi soir et dimanche soir, disponibiliye visees 99,5 % paiement conforme,
 donnees personnelles RGPD.

 Constructio au fil des sections

 Exercice 1 - Demarche

 - 3 User stories principales au format INVEST (et crite d'acceotation par user story)
 - 3 criteres de qualite mesurables
 - 1 ADR sur un choiox technique structurant

 QUESTION 1 : USER STORIES AU FORMAT INVEST

 -> 3 USER STORIES & CRITERES D'ACCEPTATION

**User Story 1 – Publication d’un trajet**

En tant que Conducteur
Je veux publier un trajet
Afin de proposer des places à des passagers

Critères d’acceptation :

Le conducteur peut saisir : départ, destination, date, heure, prix, nombre de places.

**User Story 2 – Réservation d’un trajet**

En tant que Passager
Je veux réserver une place
Afin de voyager avec un conducteur

Critères d’acceptation :

Le passager peut voir les trajets disponibles.

**User Story 3 - Suppression d'un trajet**

En tant que modérateur
Je veux supprimer un trajet signalé
Afin de garantir la sécurité et la fiabilité de la plateforme

Critères d’acceptation :

Le modérateur peut consulter la liste des trajets signalés

QUESTION 2 : CRITERES DE QUALITE MESURABLES

- Performance
Temps de réponse < 2 secondes pour une recherche de trajet

- Disponibilité
Disponibilité du système ≥ 99,5 % (comme demandé dans les contraintes)

- Sécurité & conformité
100 % des paiements conformes aux normes (ex : authentification forte)

QUESTION 3 : ADR (Architecture Decision Record)

Décision : Utilisation d’un service de paiement externe

- Contexte :
La plateforme doit gérer des paiements sécurisés avec conformité réglementaire.

- Décision :
Utiliser un service tiers (ex : Stripe ou PayPal) au lieu de développer une solution interne.

- Justification :

* Sécurité déjà assurée (normes PCI-DSS)
* Gain de temps de développement
* Gestion simplifiée des litiges et remboursements

- Conséquences :

* Dépendance à un service externe
* Frais de transaction
* Maintenance réduite côté plateforme