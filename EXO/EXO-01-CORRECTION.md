# **Correction : Gestion d'une liste d'employés avec `match-case` (switch-case)**  

## **Meilleur choix de structure de données :**  
Le **dictionnaire** (`dict`) est la meilleure structure pour gérer les employés.  

### **Pourquoi le dictionnaire ?**  
✅ **Accès rapide (`O(1)`)** : Permet d’accéder directement aux employés par leur **ID**.  
✅ **Facilité de suppression et modification** : Supprimer un employé est instantané avec `del employes[id]`.  
✅ **Structure évolutive** : Facile d’ajouter d’autres informations (ex. : poste, salaire).  
✅ **Unicité des clés** : L’ID étant une clé unique, pas de doublons possibles.  

---
## **Implémentation en Python :**  

```python
# Gestion des employés avec un dictionnaire et un menu optimisé avec match-case (switch-case)
import sys

# Dictionnaire pour stocker les employés {ID: Nom}
employes = {}

def ajouter_employe(id, nom):
    """Ajoute un employé avec un ID unique."""
    if id in employes:
        print(f"❌ Erreur : L'ID {id} est déjà utilisé.")
        return
    employes[id] = nom
    print(f"✅ Employé ajouté : {nom} (ID: {id})")

def afficher_employes():
    """Affiche la liste des employés."""
    if not employes:
        print("📜 La liste des employés est vide.")
        return
    print("\n📋 Liste des employés :")
    for id, nom in employes.items():
        print(f"🔹 {nom} (ID: {id})")

def supprimer_employe(valeur):
    """Supprime un employé par ID ou par nom."""
    if valeur.isdigit():  # Suppression par ID
        id = int(valeur)
        if id in employes:
            print(f"🗑️ Suppression de {employes[id]} (ID: {id}).")
            del employes[id]
        else:
            print("❌ Aucun employé trouvé avec cet ID.")
    else:  # Suppression par nom
        found = False
        for id, nom in list(employes.items()):
            if nom.lower() == valeur.lower():
                print(f"🗑️ Suppression de {nom} (ID: {id}).")
                del employes[id]
                found = True
                break
        if not found:
            print("❌ Aucun employé trouvé avec ce nom.")

def menu():
    """Affiche le menu et gère les interactions utilisateur."""
    while True:
        print("\n--- Menu Gestion des Employés ---")
        print("1️⃣ Ajouter un employé")
        print("2️⃣ Afficher la liste des employés")
        print("3️⃣ Supprimer un employé")
        print("4️⃣ Quitter")

        choix = input("👉 Votre choix : ").strip()

        match choix:
            case "1":
                nom = input("👤 Nom de l'employé : ").strip()
                id = input("🔢 Numéro d'identification : ").strip()
                if id.isdigit():
                    ajouter_employe(int(id), nom)
                else:
                    print("❌ Erreur : L'ID doit être un nombre.")

            case "2":
                afficher_employes()

            case "3":
                valeur = input("🗑️ Entrez le nom ou l'ID de l'employé à supprimer : ").strip()
                supprimer_employe(valeur)

            case "4":
                print("👋 Au revoir !")
                sys.exit()

            case _:
                print("❌ Choix invalide. Veuillez entrer un chiffre entre 1 et 4.")

# Lancer le programme
menu()
```

---

## **Pourquoi utiliser `match-case` ? (switch-case en Python)**  
✅ **Plus rapide et plus lisible** qu’une suite de `if-elif-else`.  
✅ **Facilite l'ajout de nouvelles options** dans le menu.  
✅ **Plus efficace** car chaque case est évaluée **une seule fois**.  

---

## **Exemples d’utilisation :**  

### **Ajout d’employés :**  
```
👤 Nom de l'employé : Martin
🔢 Numéro d'identification : 102
✅ Employé ajouté : Martin (ID: 102)

👤 Nom de l'employé : Dupont
🔢 Numéro d'identification : 105
✅ Employé ajouté : Dupont (ID: 105)
```

### **Affichage des employés :**  
```
📋 Liste des employés :
🔹 Martin (ID: 102)
🔹 Dupont (ID: 105)
```

### **Suppression d’un employé par ID :**  
```
🗑️ Entrez le nom ou l'ID de l'employé à supprimer : 102
🗑️ Suppression de Martin (ID: 102).
```

### **Affichage après suppression :**  
```
📋 Liste des employés :
🔹 Dupont (ID: 105)
```

---

## **Résumé du choix optimal :**
✅ **Dictionnaire (`dict`)** pour accès rapide et suppression efficace.  
✅ **Utilisation de l'ID comme clé unique** pour éviter les doublons.  
✅ **Interface console simple et claire avec `match-case`**.  
✅ **Gestion des erreurs pour éviter les crashs**.  

---
