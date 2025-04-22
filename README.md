# Exercice : Créer un état avec `useState` contenant plusieurs objets

## 🌟 Objectif :
Créer une déclaration d'état (`useState`) dans l'APP contenant **un tableau de 3 objets**.

---

## 🛠️ Instructions :

1. **Utilise** la fonction `useState` pour déclarer un état.  
   - Le premier élément du tableau de déstructuration doit s'appeler **`entries`**.
   - Le deuxième élément doit s'appeler **`setEntries`**.

2. **Initialise** cet état avec un **tableau** contenant **trois objets**.

3. Chaque **objet** doit contenir exactement trois propriétés :
   - `id` : Utilise `crypto.randomUUID()` pour générer un identifiant unique.
   - `value` : Une valeur numérique :
     - Premier objet : **90.0**
     - Deuxième objet : **40.0**
     - Troisième objet : **15.5**
   - `categoryID` : Un entier :
     - Premier objet : **0**
     - Deuxième objet : **1**
     - Troisième objet : **0**

4. **Respecte la syntaxe suivante** :
   - Le tableau est entouré de crochets `[ ]`.
   - Chaque objet est entouré d’accolades `{ }`.
   - Chaque propriété dans un objet est séparée par une virgule `,`.
   - Chaque objet est séparé par une virgule dans le tableau.

5. **Écris ce code dans une fonction** (mais tu n’as pas besoin de la finir ou de faire autre chose).

6. **Respecte l'indentation** pour rendre ton code lisible :
   - Chaque objet commence sur une nouvelle ligne.
   - Les propriétés sont alignées proprement.

---

## 📋 Résumé :

| Élément à vérifier | ✅ Oui/Non |
|:---|:---|
| Le `useState` existe | |
| Il y a 3 objets dans le tableau | |
| Chaque objet a `id`, `value`, et `categoryID` | |
| Les valeurs `90.0`, `40.0`, `15.5` sont bien présentes | |
| Les `categoryID` sont `0`, `1`, `0` | |
| Le code est bien indenté et lisible | |

---

## 🧐 Question bonus :

> Pourquoi est-il important que chaque objet ait un identifiant unique (`id`) dans React ?

# Exercice 2 : Passer des données à un composant en utilisant des props

## 🌟 Objectif :
Apprendre à passer des données d'un composant parent à un composant enfant via les **props**.

---

## 🛠️ Instructions :

1. **Utilise** un composant appelé **`EntriesList`** dans ton `return` de la fonction `App`.

2. **Passe une prop** à `EntriesList` :
   - Le nom de la prop doit être **`entries`**.
   - La valeur de cette prop doit être la variable d'état **`entries`** que tu as déjà créée précédemment.

3. **Utilise la bonne syntaxe JSX** pour passer une prop de type JavaScript :
   - Utilise les accolades `{}` pour insérer une variable JavaScript.

4. **Place** ce composant `EntriesList` après les autres composants (Header, RegisterSection, ResumeSection) dans ton `return`.

5. **Respecte la syntaxe suivante** :
   - Chaque composant est sur une ligne.
   - `EntriesList` doit être écrit avec une majuscule en première lettre.
   - La prop est écrite sous la forme `entries={entries}`.

---

## 📋 Résumé :

| Élément à vérifier | ✅ Oui/Non |
|:---|:---|
| Le composant `EntriesList` est présent | |
| Le composant reçoit la prop `entries` | |
| La valeur de la prop est `entries` | |
| Les accolades `{}` sont utilisées correctement | |
| Le composant est placé après les autres dans le `return` | |

---

## 🧐 Question bonus :

> Pourquoi doit-on utiliser des accolades `{}` autour d'une variable dans JSX ?

# Exercice 3 : Recevoir une prop `entries` dans un composant existant

## 🌟 Objectif :
Comprendre comment un composant existant peut recevoir une **prop**.

---

## 🛠️ Instructions :

1. Le composant **`EntriesList`** est déjà créé.

2. **Ajoute la prop** `entries` en paramètre de la fonction du composant.

3. **Utilise la déstructuration** directe dans la signature de la fonction.

4. Tu dois écrire le mot **`entries`** entre **accolades** `{}` dans les paramètres.

5. Ne modifie pas le reste du composant.

6. **N'utilise pas** `props.entries` à l'intérieur du composant, mais bien la variable `entries` directement.

7. Respecte la syntaxe de la fonction fléchée.

---

## 📋 Points à vérifier :

| Élément à vérifier | ✅ Oui/Non |
|:---|:---|
| Le paramètre est entre accolades `{ entries }` | |
| La déstructuration est directe | |
| Le mot `entries` est bien utilisé dans le composant | |
| Aucun changement inutile dans le reste du code | |

---

## 🧐 Question bonus :

> Quelle est la différence entre recevoir `entries` directement en paramètre et utiliser `props.entries` dans React ?

# Exercice 4 : Afficher une liste avec `map` et passer des props

## 🌟 Objectif :
Utiliser `map` pour parcourir une liste et afficher un composant pour chaque élément.

---

## 🛠️ Instructions :

1. Utilise la méthode **`map`** sur la liste **`entries`**.

2. Pour chaque élément appelé **`entry`** :
   - Retourne un composant **`EntryCard`**.

3. Passe deux props à `EntryCard` :
   - Une prop **`key`** qui doit recevoir la valeur **`entry.id`**.
   - Une prop **`entry`** qui doit recevoir l'objet complet **`entry`**.

4. Utilise les accolades `{}` pour insérer `entry.id` et `entry` dans les props.

5. Place le résultat à l'intérieur de la balise `<ul>`.

6. Ferme correctement le composant `EntryCard` en mode self-closing (`<EntryCard ... />`).

7. Respecte l'indentation et la lisibilité du code.

---

## 📋 Points à vérifier :

| Élément à vérifier | ✅ Oui/Non |
|:---|:---|
| La méthode `map` est utilisée correctement | |
| Le composant `EntryCard` est retourné pour chaque `entry` | |
| La prop `key` est présente et correcte (`key={entry.id}`) | |
| La prop `entry` est passée correctement (`entry={entry}`) | |
| Les accolades `{}` sont utilisées autour des variables | |
| Le composant est bien fermé avec `/>` | |

---

## 🧐 Question bonus :

> Pourquoi doit-on ajouter une prop `key` unique à chaque élément retourné par un `map` en React ?

# Exercice 5 : Utiliser la prop `entry` dans un composant existant

## 🌟 Objectif :
Apprendre à utiliser une prop reçue pour afficher des données dynamiques dans un composant.

---

## 🛠️ Instructions :

1. Le composant **`EntryCard`** est déjà créé.

2. Utilise la prop **`entry`** à l'intérieur du composant pour :
   
   - Afficher la **valeur** de `entry.value` en format monnaie.
   - Utiliser `toLocaleString` pour afficher au format "pt-BR" et avec style "currency" en "BRL".

3. Utilise la prop **`entry`** pour :
   - Vérifier si `entry.categoryID` est égal à `0`.
   - Si c'est `0`, afficher "Entrada".
   - Sinon, afficher "Saída".

4. Le formatage de la valeur doit être écrit à l'intérieur d'une balise `<p>`.

5. La condition sur `categoryID` doit être écrite à l'intérieur d'une balise `<span>`.

6. Respecte la bonne syntaxe JSX pour insérer des expressions JavaScript (avec `{}`).

---

## 📋 Points à vérifier :

| Élément à vérifier | ✅ Oui/Non |
|:---|:---|
| La valeur est formatée avec `toLocaleString` | |
| Le format utilise "pt-BR", style "currency", et devise "BRL" | |
| La vérification `categoryID === 0` est présente | |
| "Entrada" ou "Saída" s'affichent correctement | |
| L'utilisation de `{}` est correcte autour des expressions | |

---

## 🧐 Question bonus :

> Pourquoi est-il utile de formater les nombres directement dans le composant plutôt que dans l'état ou ailleurs dans l'application ?

