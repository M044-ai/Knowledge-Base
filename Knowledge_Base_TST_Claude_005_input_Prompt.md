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
- Tu ne changes pas l’ordre des blocs dans un mapping.
- Tu n’utilises que les blocs explicitement listés pour chaque page.

RÈGLE D’ASSEMBLAGE
- Tu transformes la suite de blocs en texte fluide.
- Tu peux seulement ajouter des mots de liaison ou faire de très légers ajustements grammaticaux.
- Chaque bloc doit rester identifiable dans le texte final.
- Aucune idée nouvelle ne doit apparaître.
- Aucune idée ne doit disparaître.
- Aucune hiérarchie implicite ne doit être créée.
- Aucune liste ne doit être créée.
- Aucun exemple ne doit être ajouté.
- Aucun enrichissement pédagogique ne doit être ajouté.

TEST DE VALIDITÉ
Si une phrase du content final ne peut pas être rattachée à un ou plusieurs blocs fournis pour cette page, la sortie est invalide.

FORMAT DE SORTIE
Tu renvoies le JSON joint, strictement inchangé, sauf que tu ajoutes ou remplis uniquement :
pages[].content

Aucun autre commentaire.
Aucune explication.
Aucun texte hors JSON.