Tu vas assembler du contenu à partir d’un JSON unique.

Le JSON joint est la seule source de vérité.
Tu ne dois utiliser aucune autre source.
Tu ne dois pas demander d’autre fichier.
Tu ne dois pas utiliser de connaissances externes.

OBJECTIF
Remplir uniquement le champ "content" des pages présentes dans le JSON, en assemblant les blocs indiqués dans "page_block_mappings".

RÈGLES ABSOLUES
- Tu ne modifies aucune clé existante.
- Tu ne modifies aucun id.
- Tu ne modifies aucun texte de bloc.
- Tu ne modifies aucun item.
- Tu ne modifies aucune ressource.
- Tu ne modifies aucun mapping.
- Tu n’ajoutes aucun objet.
- Tu ne supprimes aucun objet.
- Tu ne crées aucun bloc.
- Tu n’utilises que les blocs explicitement listés pour chaque page.

RÈGLE D’ASSEMBLAGE
- Tu transformes la suite de blocs en texte fluide.
- Tu conserves l’ordre des blocs fourni dans chaque mapping.
- Tu dois reprendre toutes les idées contenues dans les blocs.
- Tu ne dois supprimer aucune idée.
- Tu ne dois ajouter aucune idée nouvelle.

MICRO-LIBERTÉ AUTORISÉE
Tu peux seulement :
- ajouter de très courts mots ou groupes de liaison pour améliorer la fluidité
- ajuster très légèrement la grammaire ou la ponctuation
- fusionner localement deux phrases voisines si le sens reste strictement identique

Cette liberté n’est autorisée que si :
- chaque bloc reste identifiable dans le texte final
- aucune hiérarchie implicite n’est créée
- aucune généralisation n’est ajoutée
- aucun exemple n’est reformulé ou enrichi
- aucun contenu n’est condensé au point de faire disparaître un bloc

INTERDIT
Tu ne dois jamais :
- ajouter une idée
- reformuler pour enrichir
- expliquer davantage
- résumer
- créer une liste
- créer une structure pédagogique
- ajouter une hiérarchie implicite
- changer l’ordre logique des idées
- remplacer un exemple par une autre formulation plus “naturelle” si cela altère sa traçabilité

TEST DE VALIDITÉ
Le texte final doit rester traçable bloc par bloc.
Si une phrase ne peut pas être rattachée à un ou plusieurs blocs du mapping de la page, la sortie est invalide.

FORMAT DE SORTIE
Tu renvoies le JSON joint, strictement inchangé, sauf que tu ajoutes ou remplis uniquement :
pages[].content

Aucun commentaire.
Aucune explication.
Aucun texte hors JSON.