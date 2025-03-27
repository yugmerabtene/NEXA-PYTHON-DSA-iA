### 💡 Sujet : Gestion d'une bibliothèque

Tu dois créer un programme qui permet de gérer les livres d'une bibliothèque en utilisant :
- Un **hash set** pour garder une trace des livres uniques déjà enregistrés.
- Une **hash map (dict)** pour associer chaque livre à son nombre d'exemplaires disponibles.
- Une **hash table personnalisée** (en bonus) pour bien comprendre son fonctionnement interne.

---

### 🧪 Énoncé :

1. Crée une fonction `ajouter_livre(livres_set, inventaire, titre)` qui :
   - Ajoute un livre dans le `set` s’il n’est pas déjà présent.
   - Ajoute ou incrémente le nombre d’exemplaires dans le `dict` (`inventaire`).

2. Crée une fonction `emprunter_livre(inventaire, titre)` qui :
   - Vérifie si le livre est dans l’inventaire avec un stock > 0.
   - Décrémente le stock si c’est le cas, sinon affiche un message d'erreur.

3. Crée une classe `HashTable` simple avec collisions gérées par chaînage (listes dans les buckets).
   - Méthodes : `set(key, value)` et `get(key)`.

---

### ✅ Exemple attendu :

```python
ajouter_livre(livres_set, inventaire, "Le Petit Prince")
ajouter_livre(livres_set, inventaire, "1984")
ajouter_livre(livres_set, inventaire, "Le Petit Prince")

emprunter_livre(inventaire, "Le Petit Prince")
emprunter_livre(inventaire, "Le Petit Prince")
emprunter_livre(inventaire, "Le Petit Prince")  # Doit afficher un message d'erreur
```

---

### 🔧 Squelette de code à compléter :

```python
# Hash Set et Hash Map
livres_set = set()
inventaire = {}

def ajouter_livre(livres_set, inventaire, titre):
    # À compléter

def emprunter_livre(inventaire, titre):
    # À compléter

# Hash Table personnalisée
class HashTable:
    def __init__(self, taille=10):
        self.taille = taille
        self.table = [[] for _ in range(taille)]

    def hash_function(self, key):
        return hash(key) % self.taille

    def set(self, key, value):
        # À compléter

    def get(self, key):
        # À compléter

# Test rapide
ajouter_livre(livres_set, inventaire, "Le Petit Prince")
ajouter_livre(livres_set, inventaire, "1984")
ajouter_livre(livres_set, inventaire, "Le Petit Prince")

emprunter_livre(inventaire, "Le Petit Prince")
emprunter_livre(inventaire, "Le Petit Prince")
emprunter_livre(inventaire, "Le Petit Prince")  # Doit afficher "Aucun exemplaire disponible"

# Test de la hash table custom
ht = HashTable()
ht.set("clé1", "valeur1")
print(ht.get("clé1"))  # Doit afficher "valeur1"
```
