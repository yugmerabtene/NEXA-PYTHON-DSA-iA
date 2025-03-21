# **Jour 1 : Introduction au Langage Python**

Python est un langage de programmation puissant, facile à apprendre et largement utilisé dans divers domaines, notamment le développement web, l’analyse de données, l’intelligence artificielle et l’automatisation.

---

## **1. Bases de Python**
Dans cette section, nous allons voir les fondamentaux de Python.

### **1.1 Python Syntax**
Python est un langage qui utilise l’**indentation** pour structurer le code. Il ne nécessite pas d’accolades `{}` comme en C ou Java.

Exemple :
```python
if True:
    print("Bienvenue en Python !")  # Ce bloc est indenté
```

> ⚠️ Une mauvaise indentation entraînera une erreur (`IndentationError`).

### **1.2 Python Comments**
Les commentaires permettent de documenter le code. Ils sont ignorés par l’interpréteur.

- **Commentaire sur une seule ligne** avec `#` :
  ```python
  # Ceci est un commentaire
  print("Python est génial !")  # Un autre commentaire
  ```
- **Commentaire sur plusieurs lignes** avec `""" """` :
  ```python
  """
  Ceci est un commentaire
  sur plusieurs lignes
  """
  print("Hello, World!")
  ```

### **1.3 Python Variables**
Une variable stocke une valeur et peut être réassignée.

```python
nom = "Alice"
age = 25
est_etudiant = True

print(nom, age, est_etudiant)  # Alice 25 True
```

### **1.4 Python Data Types**
Python propose plusieurs types de données :
```python
entier = 10          # int
flottant = 3.14      # float
texte = "Bonjour"    # str
booleen = True       # bool
liste = [1, 2, 3]    # list
tuple_ = (1, 2, 3)   # tuple
ensemble = {1, 2, 3} # set
dictionnaire = {"nom": "Alice", "age": 25}  # dict
```

### **1.5 Python Numbers**
Python prend en charge les **entiers**, les **flottants**, et les **nombres complexes**.

```python
x = 10    # int
y = 3.14  # float
z = 1 + 2j  # complex

print(type(x), type(y), type(z))  # <class 'int'> <class 'float'> <class 'complex'>
```

### **1.6 Python Casting**
On peut convertir les types de données :

```python
a = int(3.5)  # 3
b = float(10)  # 10.0
c = str(100)  # "100"

print(a, b, c)
```

### **1.7 Python Booleans**
Le type `bool` est utilisé pour représenter `True` ou `False`.

```python
x = 10 > 5  # True
y = bool(0)  # False

print(x, y)
```

---

## **2. Opérations et Structures de Contrôle**

### **2.1 Python Operators**
Les **opérateurs arithmétiques** :
```python
a = 10
b = 3
print(a + b)  # Addition : 13
print(a - b)  # Soustraction : 7
print(a * b)  # Multiplication : 30
print(a / b)  # Division : 3.3333
print(a // b)  # Division entière : 3
print(a % b)  # Modulo : 1
print(a ** b)  # Exponentiation : 10^3 = 1000
```

Les **opérateurs de comparaison** :
```python
print(a == b)  # False
print(a > b)   # True
print(a <= b)  # False
```

### **2.2 Python If...Else**
Les conditions permettent d'exécuter du code en fonction d'une situation donnée.

```python
age = 18
if age >= 18:
    print("Majeur")
else:
    print("Mineur")
```

### **2.3 Python While Loops**
Une boucle `while` s’exécute tant qu'une condition est `True`.

```python
i = 1
while i <= 5:
    print(i)
    i += 1  # Incrémentation
```

### **2.4 Python For Loops**
Une boucle `for` permet d’itérer sur une séquence.

```python
for i in range(5):  # De 0 à 4
    print(i)
```

---

## **3. Structures de Données**
Python fournit plusieurs structures de données.

### **3.1 Python Strings**
Les chaînes de caractères (`str`) sont utilisées pour manipuler du texte.

```python
texte = "Bonjour, Python!"
print(texte[0])  # B
print(texte[:7])  # Bonjour
print(len(texte))  # Longueur de la chaîne
```

### **3.2 Python Lists**
Une liste est une collection **modifiable** et **ordonnée**.

```python
ma_liste = [1, 2, 3, "Python"]
ma_liste.append(4)  # Ajout d'un élément
print(ma_liste)
```

### **3.3 Python Tuples**
Un tuple est une liste **immuable**.

```python
mon_tuple = (1, 2, 3)
print(mon_tuple[1])  # 2
```

### **3.4 Python Sets**
Un **set** est une collection **non ordonnée et unique**.

```python
mon_set = {1, 2, 3, 3}
print(mon_set)  # {1, 2, 3}
```

### **3.5 Python Dictionaries**
Un **dictionnaire** stocke des paires `clé: valeur`.

```python
personne = {"nom": "Alice", "âge": 25}
print(personne["nom"])  # Alice
```

### **3.6 Python Arrays**
Un **tableau** est similaire à une liste mais optimisé pour les nombres.

```python
import array
arr = array.array('i', [1, 2, 3])
print(arr[0])  # 1
```

---

## **4. Fonctions et Programmation Orientée Objet (OOP)**

### **4.1 Python Functions**
Une fonction permet de **réutiliser** du code.

```python
def saluer(nom):
    return f"Bonjour, {nom}!"

print(saluer("Alice"))
```

### **4.2 Python Lambda**
Une **fonction lambda** est une fonction anonyme.

```python
carre = lambda x: x ** 2
print(carre(5))  # 25
```

### **4.3 Python Classes/Objects**
Python est **orienté objet**.

```python
class Personne:
    def __init__(self, nom):
        self.nom = nom

    def parler(self):
        return f"Je suis {self.nom}"

p1 = Personne("Alice")
print(p1.parler())  # Je suis Alice
```

### **4.4 Python Inheritance**
L’héritage permet de créer des classes dérivées.

```python
class Etudiant(Personne):
    pass

e1 = Etudiant("Bob")
print(e1.parler())  # Je suis Bob
```

### **4.5 Python Polymorphism**
Le polymorphisme permet d’avoir plusieurs classes avec des méthodes communes.

```python
class Chat:
    def parler(self):
        return "Miaou!"

class Chien:
    def parler(self):
        return "Ouaf!"

animaux = [Chat(), Chien()]
for animal in animaux:
    print(animal.parler())
```
----
# **Modules, Gestion des Données, Erreurs et Fichiers en Python**


---

## **5. Modules et Bibliothèques**

Python est livré avec de nombreux **modules** intégrés et permet aussi d'installer des **bibliothèques externes** via `pip`.

### **5.1 Python Modules**
Un **module** est un fichier contenant du code Python (fonctions, classes, etc.) que l'on peut réutiliser.

#### **Importer un module**
Python fournit des modules natifs comme `math` :
```python
import math
print(math.sqrt(16))  # 4.0
```

#### **Créer son propre module**
Un fichier `mon_module.py` :
```python
def saluer(nom):
    return f"Bonjour, {nom}!"
```
Puis, dans un autre fichier :
```python
import mon_module
print(mon_module.saluer("Alice"))
```

#### **Importer une partie spécifique d'un module**
```python
from math import pi
print(pi)  # 3.141592653589793
```

---

### **5.2 Python PIP (Gestionnaire de paquets)**
PIP est l’outil permettant d’installer des bibliothèques tierces.

#### **Installer une bibliothèque**
```bash
pip install requests
```

#### **Lister les bibliothèques installées**
```bash
pip list
```

#### **Désinstaller une bibliothèque**
```bash
pip uninstall requests
```

---

## **6. Gestion des Données et Fichiers**

Python facilite la manipulation de formats de données tels que **JSON**, **les dates**, **les nombres mathématiques**, et les **expressions régulières**.

### **6.1 Python JSON**
Le format JSON est souvent utilisé pour **échanger des données** entre des applications.

#### **Convertir un dictionnaire en JSON**
```python
import json
data = {"nom": "Alice", "age": 25}
json_data = json.dumps(data)
print(json_data)  # {"nom": "Alice", "age": 25}
```

#### **Convertir JSON en dictionnaire**
```python
json_text = '{"nom": "Alice", "age": 25}'
dict_data = json.loads(json_text)
print(dict_data["nom"])  # Alice
```

---

### **6.2 Python Dates**
Le module `datetime` permet de travailler avec les dates et heures.

```python
from datetime import datetime
now = datetime.now()
print(now)  # 2025-03-21 10:15:30.123456
```

#### **Formater une date**
```python
formatted_date = now.strftime("%Y-%m-%d %H:%M:%S")
print(formatted_date)  # 2025-03-21 10:15:30
```

#### **Calculer une date dans le futur**
```python
from datetime import timedelta
future_date = now + timedelta(days=10)
print(future_date)
```

---

### **6.3 Python Math**
Le module `math` propose des fonctions mathématiques avancées.

```python
import math
print(math.sqrt(25))  # 5.0
print(math.pow(2, 3))  # 8.0
print(math.pi)  # 3.141592653589793
```

---

### **6.4 Python RegEx (Expressions Régulières)**
Les **expressions régulières** permettent de rechercher des motifs dans des chaînes de caractères.

```python
import re
texte = "Mon email est contact@email.com"
match = re.search(r'\S+@\S+', texte)  # Recherche d'un email
print(match.group())  # contact@email.com
```

---

## **7. Gestion des Erreurs et Sécurité**

### **7.1 Python Try...Except**
Python permet de gérer les erreurs avec `try...except` pour éviter les plantages.

```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Erreur : Division par zéro !")
```

#### **Gestion de plusieurs erreurs**
```python
try:
    x = int("texte")  # Erreur de conversion
except (ZeroDivisionError, ValueError) as e:
    print(f"Erreur : {e}")
```

---

### **7.2 Python User Input**
Python permet de **demander une entrée utilisateur** avec `input()`.

```python
nom = input("Entrez votre nom : ")
print(f"Bonjour, {nom} !")
```

> ⚠️ **Les entrées utilisateur doivent être validées** pour éviter les failles de sécurité.

#### **Vérifier une entrée numérique**
```python
while True:
    try:
        age = int(input("Entrez votre âge : "))
        break
    except ValueError:
        print("Veuillez entrer un nombre valide.")
```

---

### **7.3 Python String Formatting**
Il existe plusieurs méthodes pour formater des chaînes.

#### **Utilisation de `f-strings` (Python 3.6+)**
```python
nom = "Alice"
age = 25
print(f"Bonjour, je suis {nom} et j'ai {age} ans.")
```

#### **Utilisation de `.format()`**
```python
print("Bonjour, je suis {} et j'ai {} ans.".format(nom, age))
```

---

## **8. File Handling (Gestion des Fichiers)**

Python permet de **lire, écrire, créer et supprimer des fichiers**.

---

### **8.1 Python File Handling**
Le mode d'ouverture d'un fichier :
| Mode | Description |
|------|------------|
| `r` | Lecture seule |
| `w` | Écriture (écrase le contenu existant) |
| `a` | Ajout à la fin du fichier |
| `x` | Création du fichier (échec si le fichier existe déjà) |

---

### **8.2 Python Read Files**
Lire un fichier :
```python
f = open("fichier.txt", "r")
print(f.read())  # Affiche le contenu du fichier
f.close()
```

Lire une seule ligne :
```python
f = open("fichier.txt", "r")
print(f.readline())  # Lit la première ligne
f.close()
```

---

### **8.3 Python Write/Create Files**
Écrire dans un fichier (écrase le contenu existant) :
```python
f = open("fichier.txt", "w")
f.write("Bonjour, ceci est un test.")
f.close()
```

Ajouter du texte sans écraser :
```python
f = open("fichier.txt", "a")
f.write("\nAjout d'une nouvelle ligne.")
f.close()
```

---

### **8.4 Python Delete Files**
Supprimer un fichier avec `os.remove()`.

```python
import os
if os.path.exists("fichier.txt"):
    os.remove("fichier.txt")
    print("Fichier supprimé.")
else:
    print("Le fichier n'existe pas.")
```

---
