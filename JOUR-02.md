## BIG O

# **Explication détaillée de la notation O dans O(1) et autres complexités**
La **notation O** (prononcée **"Big O"**) est utilisée en informatique pour **analyser l'efficacité** d'un algorithme en mesurant **comment le temps d'exécution ou l'utilisation de la mémoire évolue en fonction de la taille des données**.

## **1️⃣ Qu'est-ce que O(n) signifie ?**
- `O(f(n))` décrit **le pire cas** d'un algorithme lorsque `n` (taille des données) devient très grand.
- Elle indique **combien d'opérations** sont nécessaires pour exécuter l'algorithme.
- **n** représente **la taille des entrées** (exemple : nombre d'éléments dans une liste).

---

## **2️⃣ Explication des complexités courantes**
Voici les **principales complexités** et leurs impacts :

| **Notation**  | **Nom**                        | **Explication** |
|--------------|--------------------------------|----------------|
| **O(1)**     | **Temps constant**            | L'opération s'exécute toujours en un **temps fixe**, quelle que soit la taille des données. |
| **O(log n)** | **Temps logarithmique**       | L'opération diminue progressivement le nombre de données à traiter (exemple : recherche binaire). |
| **O(n)**     | **Temps linéaire**            | Le temps d'exécution **augmente proportionnellement** à la taille des données. |
| **O(n log n)** | **Temps quasi-linéaire**    | Utilisé pour les algorithmes de tri efficaces comme **Quicksort** et **Mergesort**. |
| **O(n²)**    | **Temps quadratique**         | Les performances deviennent mauvaises lorsque les données augmentent (exemple : deux boucles imbriquées). |
| **O(2ⁿ)**    | **Temps exponentiel**         | Très lent, utilisé pour des problèmes comme les arbres de décision ou la récursion brute. |

---
![image](https://github.com/user-attachments/assets/5618bd11-8dee-488b-996d-fb08d6c6a529)


## **3️⃣ Exemples concrets de complexité avec Python**

### **🔹 O(1) – Temps constant**
✅ **Un accès direct dans un dictionnaire** est **toujours rapide**, peu importe la taille du dictionnaire.

```python
employes = {101: "Alice", 102: "Bob", 103: "Charlie"}
print(employes[102])  # Temps constant O(1)
```
**Explication** :
- L'accès à un élément d'un **dictionnaire** utilise une **table de hachage**.
- Peu importe le nombre d'éléments, l'accès **prend toujours le même temps**.

---

### **🔹 O(n) – Temps linéaire**
✅ **Une recherche dans une liste nécessite de parcourir tous les éléments**.

```python
noms = ["Alice", "Bob", "Charlie", "David"]
for nom in noms:
    if nom == "Charlie":
        print("Trouvé !")  # Temps linéaire O(n)
```
**Explication** :
- Si la liste contient `n` éléments, l’algorithme peut prendre `n` itérations dans le pire des cas.

---

### **🔹 O(log n) – Temps logarithmique**
✅ **Recherche binaire dans une liste triée** – on divise la liste par 2 à chaque itération.

```python
import bisect
nombres = [1, 3, 5, 7, 9, 11, 13]
index = bisect.bisect_left(nombres, 9)  # Recherche binaire O(log n)
print(f"Position de 9 : {index}")
```
**Explication** :
- Au lieu de **parcourir toute la liste**, on **divise la recherche par 2 à chaque étape**.

---

### **🔹 O(n²) – Temps quadratique**
✅ **Comparaison de chaque élément avec tous les autres (deux boucles imbriquées).**

```python
noms = ["Alice", "Bob", "Charlie"]
for i in range(len(noms)):
    for j in range(len(noms)):
        print(f"Comparaison : {noms[i]} et {noms[j]}")  # O(n²)
```
**Explication** :
- Chaque élément est comparé avec **tous les autres**, ce qui crée un **nombre total d'opérations égal à n²**.

---

## **4️⃣ Pourquoi le dictionnaire (`dict`) est O(1) pour l'accès et la suppression ?**
- Le **dictionnaire en Python utilise une table de hachage**.
- **Chaque clé est hachée (convertie en un index unique)** pour un accès rapide.
- Contrairement à une liste où il faut **parcourir tous les éléments** (`O(n)`), le dictionnaire accède **directement** aux valeurs (`O(1)`) grâce au hachage.

```python
employes = {101: "Alice", 102: "Bob", 103: "Charlie"}

# Accès en O(1)
print(employes[102])  # "Bob"

# Suppression en O(1)
del employes[103]
```

---

## **Conclusion : Quel impact sur le projet des employés ?**
✅ **Pourquoi utiliser un dictionnaire (`dict`) pour stocker les employés ?**  
- **Ajout d’un employé** : `employes[ID] = nom` **(O(1))**  
- **Accès à un employé** : `employes[ID]` **(O(1))**  
- **Suppression d’un employé** : `del employes[ID]` **(O(1))**  

🚀 **En résumé, le dictionnaire (`dict`) est ultra-performant** par rapport à une liste (`list`) où chaque opération prend `O(n)`.
