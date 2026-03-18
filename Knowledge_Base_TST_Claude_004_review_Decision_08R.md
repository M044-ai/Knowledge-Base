Bonne idée.

Pour tester le nouveau pipeline proprement, il faut prendre :

* **1 page chapeau** : `page_decouvrir_architecture_web`
* **1 page spécifique par mode**

Je recommanderais ce trio :

### Découvrir

`page_decouvrir_api_rest`
Pourquoi : plusieurs blocs proches, risque de fusion abusive, bon test d’assemblage.

### Explorer

`page_explorer_typescript`
Pourquoi : notions croisées avec JavaScript, bon test de filtrage + cohérence conceptuelle.

### Se lancer

`page_se_lancer_postgresql`
Pourquoi : plusieurs questions/erreurs, densité plus forte, bon test de tenue de structure.

Ça donne un mini-benchmark utile :

```text
1. page_decouvrir_architecture_web
2. page_decouvrir_api_rest
3. page_explorer_typescript
4. page_se_lancer_postgresql
```

Étape suivante logique :

1. je produis les **blocs** pour ces pages si besoin,
2. puis le **mapping blocs → pages**,
3. puis le **prompt d’assemblage Claude** pour ce test réduit.
