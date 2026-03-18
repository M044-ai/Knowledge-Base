Je vais être direct :
👉 **le test 2 est nettement meilleur que le test 1… mais pas encore conforme à ton contrat.**

Je te fais une revue **opérationnelle et exploitable**, sans dilution.

---

# 1. Verdict global

### ✔️ Ce qui est bon

* Structure respectée → **OK**
* Aucun objet ajouté/supprimé → **OK**
* IDs / URLs intactes → **OK**
* Remplissage des pages → **OK**

👉 progrès réel

---

### ❌ Ce qui ne passe PAS le contrat

Il y a encore des violations **critiques mais discrètes** :

---

# 2. Problème central : dérive sémantique

## Exemple 1 — API REST

Dans le JSON :

> “Les notions à apprendre sont : API REST, endpoints, JSON.” 

👉 **NON conforme**

Pourquoi :

* formulation synthétique
* structure ajoutée (“les notions à apprendre…”)
* regroupement pédagogique non garanti dans le raw

➡️ Claude **structure → donc interprète**

---

## Exemple 2 — AWS

> “Les services AWS à connaître sont : EC2, S3, RDS, Lambda” 

👉 même problème

* liste structurée
* vocabulaire pédagogique ajouté
* hiérarchisation implicite

---

## Exemple 3 — JavaScript

> “Les points à voir en priorité sont…” 

👉 formulation **non neutre**

* “priorité” = ajout de valeur
* → violation directe du contrat

---

# 3. Diagnostic réel (important)

Claude a respecté :

✔️ la structure
✔️ les interdictions visibles

Mais il a contourné :

❌ **l’interdiction implicite d’organisation pédagogique**

---

👉 Traduction :

> Il n’ajoute pas de contenu
> MAIS il change la nature du contenu

---

# 4. Type d’erreur

Ce n’est pas une hallucination.

C’est :

> **une compression + pédagogisation**

---

👉 catégorie :

* empirique très fréquente sur LLM
* difficile à détecter sans rigueur (ce que tu fais ici)

---

# 5. Gravité

👉 **élevée dans TON système**

Pourquoi :

Tu veux :

* un JSON = source de vérité
* une traçabilité RAW → JSON

Or ici :

* le lien n’est plus bijectif
* tu ne peux plus remonter à la source exacte

---

# 6. Point positif majeur

Claude a **respecté les limites structurelles strictes**

👉 donc :

> ton prompt durci fonctionne partiellement

---

# 7. Ce qu’il manque encore dans le prompt

Ton prompt interdit :

* ajout d’info
* ajout d’exemples
* ajout de techno

Mais il n’interdit PAS explicitement :

> ❌ structuration pédagogique implicite

---

# 8. Correction minimale (critique)

Tu dois ajouter UNE règle :

---

### 🔴 RÈGLE MANQUANTE

```text
Tu ne dois jamais :
- introduire une structuration pédagogique absente du texte source
- regrouper des éléments sous forme de listes ou catégories si cette organisation n’est pas explicitement présente dans les sections source
- introduire des formulations comme :
  - "les points à voir"
  - "les notions à apprendre"
  - "les éléments clés"
  - "il faut comprendre"
  - toute hiérarchisation implicite
```

---

### 🔴 Test obligatoire à ajouter

```text
Si une structure (liste, regroupement, hiérarchie) n'existe pas explicitement dans le texte source, elle est interdite.
```

---

# 9. Autre point subtil (mais maîtrisé)

Le reste est propre :

* pas d’invention technique
* pas d’ajout métier
* pas de dérive de concepts

👉 donc le problème est **localisé et corrigeable**

---

# 10. Conclusion opérationnelle

### État du système

| Élément             | Statut     |
| ------------------- | ---------- |
| JSON structure      | ✅ stable   |
| Respect des objets  | ✅          |
| Respect des sources | ⚠️ partiel |
| Dérive pédagogique  | ❌ présent  |

---

### Décision recommandée

👉 **NE PAS valider ce test en PRD**

👉 faire :

**TST_Claude_003 avec prompt durci (ajout règle anti-structuration)**

---

# 11. Lecture stratégique (important)

Tu es très proche du bon système.

Ce qui reste à corriger :

> **le comportement naturel d’un LLM à "organiser pour aider"**

---

👉 ton système devient robuste quand :

* structure = verrouillée (OK)
* contenu = strictement traçable (presque OK)

---

# 12. Fiabilité de cette analyse

* détection d’erreur : **élevée (déductif + comparaison directe)**
* impact sur pipeline : **élevé**
* correction proposée : **élevée (minimal change, fort effet)**

---

Si tu veux, je peux te fournir directement :

👉 **le prompt complet V3 prêt à coller pour TST_003** (intégrant cette règle sans casser le reste)

Ce serait le vrai point de bascule vers un système stable.
