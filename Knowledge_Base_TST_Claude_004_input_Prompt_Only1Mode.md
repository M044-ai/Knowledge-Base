# Ce prompt est appelé par Prompt_Encasing
# Il applique les règles indépendamment du mode

Tu vas transformer un contenu pédagogique brut en une knowledge base structurée pour une application.

Tu recevras DEUX entrées :
1. un JSON maître partiel
2. un contenu markdown brut

Le JSON maître partiel est la seule source de vérité structurelle pour ce lot.  
Le markdown brut sert uniquement de source textuelle à exploiter.

Tu dois STRICTEMENT respecter le JSON maître partiel.

Tu dois notamment respecter explicitement les champs suivants du JSON maître partiel :
- "role"
- "rules"
- "claude_contract"

Si une instruction du markdown brut semble contredire le JSON maître partiel, tu dois suivre le JSON maître partiel.

--------------------------------------------------
INTERDICTIONS ABSOLUES
--------------------------------------------------

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
- modifier un texte de notion, question ou erreur déjà défini dans le JSON maître partiel
- inventer une ressource
- fusionner des concepts
- inférer des tags en dehors de ceux déjà définis

Tu ne dois jamais :
- ajouter un exemple non présent dans les sections source
- ajouter une technologie non présente dans les sections source
- ajouter une analogie non présente dans les sections source
- ajouter une contextualisation
- généraliser au-delà du contenu source
- reformuler en enrichissant le sens
- compléter avec des connaissances externes

--------------------------------------------------
INTERDICTION CRITIQUE — STRUCTURATION IMPLICITE
--------------------------------------------------

Tu ne dois jamais :
- introduire une structuration pédagogique absente du texte source
- créer une hiérarchie implicite
- transformer un texte en résumé structuré
- transformer un texte en contenu pédagogique organisé

Tu ne dois jamais utiliser :
- "les points à voir"
- "les notions à apprendre"
- "les éléments clés"
- "à retenir"
- toute formulation impliquant une hiérarchisation

--------------------------------------------------
INTERDICTION CRITIQUE — TRANSFORMATION EN LISTE
--------------------------------------------------

Tu ne dois jamais transformer un contenu en liste.

Cela inclut strictement :
- les listes avec tirets "-"
- les listes numérotées
- les énumérations après ":"
- les retours à la ligne pour séparer des éléments équivalents
- toute structure visuelle de liste

Tu ne dois jamais :
- regrouper plusieurs éléments sous une même phrase introductive suivie d’éléments séparés
- condenser un texte en énumération
- extraire des éléments pour les aligner sous forme de liste

Même si les éléments existent dans le texte source, tu dois conserver leur forme narrative originale.

--------------------------------------------------
TEST FORMEL OBLIGATOIRE
--------------------------------------------------

Si une liste (visuelle ou implicite) apparaît dans le contenu alors qu’elle n’existe pas EXACTEMENT sous cette forme dans le texte source, le contenu est invalide.

--------------------------------------------------
AUTORISÉ UNIQUEMENT
--------------------------------------------------

Tu dois uniquement :
- reformuler pour clarifier le texte si nécessaire
- améliorer légèrement la lisibilité sans changer la structure
- organiser en paragraphes uniquement
- expliciter des liens déjà présents

Toute reformulation doit être :
- strictement équivalente en sens
- strictement bornée au contenu source
- sans ajout

--------------------------------------------------
RÈGLE DE PRIORITÉ
--------------------------------------------------

1. JSON maître partiel
2. markdown brut

--------------------------------------------------
TRAITEMENT DU JSON MAÎTRE PARTIEL
--------------------------------------------------

Tu dois appliquer :
- "role"
- "rules"
- "claude_contract"

Cela implique :
- JSON = structure autoritaire
- markdown = source texte uniquement
- aucun objet créé/supprimé
- aucun id modifié
- aucune URL modifiée
- contenu des pages basé uniquement sur "source_section_ids"

--------------------------------------------------
CONCEPTS / MODES / TYPES
--------------------------------------------------

Utiliser uniquement :
- concepts existants
- modes existants
- resource_types existants
- item_types existants

Aucun ajout autorisé.

--------------------------------------------------
TAGGING
--------------------------------------------------

Tu dois conserver EXACTEMENT les "concept_tags".

Aucun ajout, suppression, déduction ou héritage.

--------------------------------------------------
RESSOURCES
--------------------------------------------------

Conserver strictement :
- id
- type
- title
- url
- concept_tags
- source_section_id

--------------------------------------------------
ITEMS
--------------------------------------------------

Types :
- notion / question / error → texte intouchable
- activity → structure intouchable

--------------------------------------------------
PAGES
--------------------------------------------------

Tu dois conserver :
- id
- concept
- mode
- title
- source_section_ids
- resource_ids
- item_ids

Tu ajoutes uniquement :
- "content"

--------------------------------------------------
RÈGLE CRITIQUE SUR LE CONTENT
--------------------------------------------------

Le content doit être :

- strictement issu des sections source
- sans ajout
- sans transformation pédagogique
- sans structuration nouvelle
- sans liste

Chaque phrase doit être traçable à une phrase du source.

--------------------------------------------------
CONTRAINTE DU LOT
--------------------------------------------------

Tu remplis uniquement le champ "content" des pages présentes.

--------------------------------------------------
FORMAT DE SORTIE
--------------------------------------------------

JSON valide.

Tu dois :
- reprendre le JSON tel quel
- ne rien modifier
- ajouter uniquement "content"

--------------------------------------------------
OBJECTIF
--------------------------------------------------

Créer une knowledge base exploitable dans une application.

Tu travailles uniquement sur ce lot.