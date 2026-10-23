# OLLB — Confidentialité de l’extracteur de données pharmacies

Mise à jour : 23 octobre 2026. Version pilote.

Cette notice décrit le fonctionnement vérifié de l’extracteur OLLB et les choix de son exploitant. La durée de conservation ci-dessous est une règle retenue pour le service ; sa mise en œuvre sur le serveur reste à vérifier. Cette page ne constitue pas une attestation de conformité ni une annonce de certification du logiciel.

## Exploitant et contact

Le serveur de réception `https://pharma.ollb.fr` est exploité par **Olivier Lebrun, à titre personnel**.

Contact pour les questions de confidentialité et les demandes relatives aux données : **olivierlebrun@me.com**. Ne transmettez pas de données de patients, de jetons ou de mots de passe par e-mail.

## Finalités et origine des données

L’extracteur est destiné aux pharmacies participantes. Il lit leur logiciel de gestion afin de centraliser les données d’activité et de gestion sur le serveur OLLB et de suivre techniquement les extractions et leur réception.

L’installation configure un service Windows. Les envois sont automatiques, avec un passage prévu toutes les 15 minutes. L’historique demandé commence au 1er janvier 2025, selon les données accessibles au lecteur et au logiciel de la pharmacie.

L’installation technique ne vaut pas, à elle seule, autorisation de traiter des données personnelles de patients. Les rôles des intervenants et le fondement applicable aux traitements doivent être établis avec les pharmacies avant leur mise en œuvre.

## Données susceptibles d’être envoyées

Selon les capacités du lecteur : données de produits et médicaments, fabricants, fournisseurs, ventes, stocks, commandes, délivrances, dates, quantités et montants disponibles dans ces flux.

Les lots comportent aussi l’identifiant et le libellé de la pharmacie, le logiciel détecté, la catégorie de flux, la période historique, le nombre de lignes et les horodatages. Des rapports techniques indiquent les compteurs d’extraction, les états et les erreurs.

Le filtrage d’envoi retire les champs d’identification directe du patient et du client, les dates de naissance, les références de facture et les champs identifiant le personnel. L’extracteur peut néanmoins accéder localement aux données nécessaires au fonctionnement du lecteur : le filtre d’envoi ne modifie pas la base de la pharmacie.

L’âge en années et le sexe sont prévus dans le format d’envoi. Leur alimentation par les lecteurs n’est pas encore validée dans la version pilote ; ces champs peuvent être absents ou non renseignés. Une future activation doit être examinée avant utilisation et cette notice actualisée si nécessaire.

L’absence d’identifiants directs ne garantit pas l’anonymat des données, notamment lorsque des informations de délivrance sont associées à des dates et à une officine.

## Destination, accès et sécurité technique

La destination configurée est le serveur OLLB `https://pharma.ollb.fr`. L’envoi utilise HTTPS et un jeton propre à la pharmacie. Les lots en attente sont chiffrés localement par les mécanismes Windows ; dans la version service, les dossiers de données sont réservés au système et aux administrateurs.

Les données reçues sont destinées à l’exploitation du service OLLB par son administrateur. Les accès effectifs, les intervenants d’hébergement, le pays d’hébergement et les éventuels transferts restent à documenter avant une diffusion générale. Cette notice ne promet pas une certification particulière de l’hébergement ni un niveau de sécurité non vérifié.

## Conservation et arrêt des envois

L’exploitant a retenu une conservation des données reçues de **cinq ans à compter de leur réception**. La suppression des données arrivées à échéance, les sauvegardes et les durées des journaux serveur doivent encore être vérifiées et mises en cohérence avec cette règle. La publication de cette notice ne configure pas de purge automatique.

Sur le poste, un lot envoyé est supprimé de la file locale après réception d’un accusé valide du serveur. En cas d’échec, il reste conservé pour réessai ; aucune durée maximale automatique de cette attente n’est actuellement annoncée.

Les outils d’arrêt du service et de désinstallation permettent d’arrêter les transmissions futures. La désinstallation conserve les données et rapports locaux et ne supprime pas automatiquement les données déjà reçues sur le serveur. Pour une demande de suppression, contacter l’exploitant.

## Demandes concernant les données

Pour toute demande d’accès, de rectification, d’effacement, de limitation ou d’opposition lorsqu’elle est applicable, contacter **olivierlebrun@me.com** en précisant la pharmacie concernée. Un patient peut également s’adresser à sa pharmacie. Une vérification adaptée peut être nécessaire pour éviter la divulgation de données à un tiers.

Il est possible d’adresser une réclamation à la [CNIL](https://www.cnil.fr/fr/plaintes).

## Évolutions de la notice

La notice sera actualisée lorsque les paramètres du service, les destinataires, les règles de conservation ou les fonctionnalités d’extraction évolueront. Les points indiqués comme restant à vérifier ne doivent pas être considérés comme déjà mis en œuvre.
