Tu vas transformer un contenu pédagogique brut en une knowledge base structurée pour une application.

Tu recevras DEUX entrées :
1. un JSON maître
2. un contenu markdown brut

Le JSON maître est la seule source de vérité structurelle.
Le markdown brut sert uniquement de source textuelle à exploiter.

Tu dois STRICTEMENT respecter le JSON maître.

Tu dois notamment respecter explicitement les champs suivants du JSON maître :
- "role"
- "rules"
- "claude_contract"

Si une instruction du markdown brut semble contredire le JSON maître, tu dois suivre le JSON maître.

Tu ne dois jamais :
- ajouter un concept
- supprimer un concept
- renommer un concept
- ajouter un mode
- supprimer un mode
- renommer un mode
- ajouter un item
- supprimer un item
- modifier un id
- modifier une URL
- modifier un texte de notion, question ou erreur déjà défini dans le JSON maître
- inventer une ressource
- fusionner des concepts
- inférer des tags en dehors de ceux déjà définis

Tu dois uniquement :
- remplir le contenu textuel des pages à partir des sections source indiquées dans le JSON maître
- structurer la sortie finale selon les objets déjà définis
- conserver strictement les relations, tags, ids, urls et objets du JSON maître

Aucun champ ne doit contenir :
- "..."
- une valeur vide
- une valeur générique
- une approximation non fondée

Si une information manque dans le markdown brut pour remplir proprement une page, tu dois utiliser uniquement ce qui est explicitement disponible dans les sections source associées. Tu ne dois pas inventer.

--------------------------------------------------
RÈGLE DE PRIORITÉ
--------------------------------------------------

Ordre de priorité absolu :

1. JSON maître
2. markdown brut

Le JSON maître définit :
- les concepts autorisés
- les modes autorisés
- les ressources autorisées
- les items autorisés
- les tags autorisés
- les pages autorisées
- les relations entre objets
- les sections source à utiliser

Le markdown brut ne définit rien de structurel.

--------------------------------------------------
TRAITEMENT DU JSON MAÎTRE
--------------------------------------------------

Tu dois lire et appliquer explicitement les champs suivants du JSON maître :

1. "role"
Si la valeur indique que le JSON est la source de vérité pour Claude, tu dois l’appliquer strictement.

2. "rules"
Tu dois appliquer toutes les règles déclarées dans cet objet sans exception.

3. "claude_contract"
Tu dois appliquer toutes les contraintes déclarées dans cet objet sans exception.

Cela signifie notamment :
- utiliser le JSON maître comme structure autoritaire
- traiter le markdown comme archive/source de texte uniquement
- ne créer ni supprimer aucun objet
- ne modifier aucun id
- ne modifier aucune url
- remplir les contenus de pages à partir des "source_section_ids"
- conserver exactement les textes des notions, questions et erreurs déjà définis dans le JSON maître

--------------------------------------------------
CONCEPTS AUTORISÉS
--------------------------------------------------

Les concepts autorisés sont UNIQUEMENT ceux présents dans la clé :
"concepts"

Tu ne dois jamais en ajouter d’autres.

Le tag global autorisé est uniquement :
"architecture_web"

Tu ne dois jamais l’ajouter automatiquement à un item déjà taggé avec un autre concept, sauf si le JSON maître le contient déjà explicitement.

--------------------------------------------------
MODES AUTORISÉS
--------------------------------------------------

Les modes autorisés sont UNIQUEMENT ceux présents dans la clé :
"modes"

Tu ne dois jamais en ajouter d’autres.

--------------------------------------------------
TYPES DE RESSOURCES
--------------------------------------------------

Les types de ressources autorisés sont UNIQUEMENT ceux présents dans :
"resource_types"

Tu ne dois jamais en ajouter d’autres.

--------------------------------------------------
TYPES D’ITEMS
--------------------------------------------------

Les types d’items autorisés sont UNIQUEMENT ceux présents dans :
"item_types"

Tu ne dois jamais en ajouter d’autres.

--------------------------------------------------
RÈGLES DE TAGGING
--------------------------------------------------

Chaque objet concerné conserve EXACTEMENT les "concept_tags" présents dans le JSON maître.

Tu ne dois jamais :
- ajouter un tag
- retirer un tag
- remplacer un tag
- déduire un tag par héritage
- ajouter automatiquement le parent d’un concept
- ajouter automatiquement "architecture_web"

Le filtrage conceptuel est fondé uniquement sur les tags directs explicitement présents.

--------------------------------------------------
RÈGLES SUR LES RESSOURCES
--------------------------------------------------

Les ressources autorisées sont UNIQUEMENT celles présentes dans :
"resources"

Tu dois conserver exactement pour chaque ressource :
- id
- type
- title
- url
- concept_tags
- source_section_id

Tu ne dois jamais modifier une URL.
Tu ne dois jamais créer une nouvelle ressource.
Tu ne dois jamais supprimer une ressource existante.

--------------------------------------------------
RÈGLES SUR LES ITEMS
--------------------------------------------------

Les items autorisés sont UNIQUEMENT ceux présents dans :
"items"

Pour les items de type :
- notion
- question
- error

Tu dois conserver exactement :
- id
- type
- mode
- text
- concept_tags
- source_section_id

Tu ne dois jamais reformuler leur texte.
Tu ne dois jamais les résumer.
Tu ne dois jamais les fusionner.
Tu ne dois jamais les découper.

Pour les items de type :
- activity

Tu dois conserver exactement :
- id
- type
- title
- description
- concept_tags
- mode_targets
- duration_minutes
- resource_ids
- source_section_id

--------------------------------------------------
RÈGLES SUR LES PAGES
--------------------------------------------------

Les pages autorisées sont UNIQUEMENT celles présentes dans :
"pages"

Pour chaque page, tu dois conserver exactement :
- id
- concept
- mode
- title
- source_section_ids
- resource_ids
- item_ids

Tu dois ajouter ou remplir uniquement un champ :
- "content"

Ce champ "content" doit être un texte pédagogique structuré, produit uniquement à partir des sections indiquées dans "source_section_ids".

Tu ne dois pas utiliser d’autres sections.
Tu ne dois pas mélanger des sections non listées.
Tu ne dois pas inventer du contenu hors source.

--------------------------------------------------
FORMAT DE SORTIE
--------------------------------------------------

Tu dois produire un JSON valide.

Le JSON de sortie doit reprendre la même structure générale que le JSON maître, avec les mêmes objets, mêmes ids et mêmes valeurs structurelles, et avec les pages enrichies d’un champ "content".

Autrement dit :
- tu reprends le JSON maître
- tu ne modifies rien de structurel
- tu ajoutes uniquement le contenu rédactionnel des pages dans le champ "content"

Le JSON final doit donc contenir les clés suivantes si elles sont présentes dans le JSON maître :
- schema_version
- role
- rules
- concepts
- modes
- resource_types
- item_types
- source_sections
- resources
- activities
- items
- pages
- claude_contract

Tu ne dois supprimer aucune de ces clés si elles sont présentes dans le JSON maître.

--------------------------------------------------
RÈGLE SUR LE CHAMP "content" DES PAGES
--------------------------------------------------

Pour chaque page :
- le contenu doit être rédigé en français
- le contenu doit être fidèle aux sections source
- le contenu doit être clair, structuré, pédagogique
- le contenu ne doit pas inventer d’éléments absents des sections source
- le contenu ne doit pas modifier le sens du matériau source
- le contenu peut reformuler le texte source pour améliorer la clarté, sauf si le JSON maître impose une conservation stricte

Les notions, questions et erreurs restent dans les objets "items".
Elles ne doivent pas être absorbées ou réécrites dans les pages.

Les ressources restent dans les objets "resources".
Elles ne doivent pas être recréées dans les pages.

--------------------------------------------------
OBJECTIF
--------------------------------------------------

Créer une knowledge base exploitable dans une application avec trois modes :
- Découvrir
- Explorer
- Se lancer

Mais la structure réelle à produire est uniquement celle définie dans le JSON maître.

--------------------------------------------------
ENTRÉES
--------------------------------------------------

JSON MAÎTRE :
[COLLER ICI LE JSON MAÎTRE]

MARKDOWN BRUT :
[COLLER ICI LE MARKDOWN BRUT]