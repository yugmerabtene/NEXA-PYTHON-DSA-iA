# **Exercice : Gestion d'une liste d'employés**  

## **Contexte :**  
Une entreprise souhaite mettre en place un système simple pour gérer ses employés. Ce système doit permettre d'ajouter de nouveaux employés, d'afficher la liste complète des employés et de supprimer un employé à partir de son **nom** ou de son **numéro d’identification**.  

Le choix du meilleur format de données est crucial pour optimiser la gestion des employés et garantir une bonne performance et une utilisation efficace de la mémoire.  

### **Objectif :**  
Vous devez choisir entre une **liste, un tuple ou un dictionnaire** pour stocker les employés et justifier votre choix.  

---

## **Consignes :**  

1. **Choix du format de données**  
   - Analyser les avantages et inconvénients des **listes**, **tuples** et **dictionnaires** pour ce cas d'utilisation.  
   - Choisir le format le plus adapté et justifier ce choix.  

2. **Développement du programme**  
   - Implémenter un programme permettant :  
     - **D'ajouter un employé** en saisissant son **nom** et son **numéro d’identification**.  
     - **D'afficher la liste complète des employés**.  
     - **De supprimer un employé** en saisissant son **nom** ou son **numéro d’identification**.  

3. **Critères de validation**  
   ✅ Le programme doit permettre d'ajouter et de supprimer des employés de manière fluide.  
   ✅ L'affichage des employés doit être clair et structuré.  
   ✅ Une bonne gestion des erreurs doit être implémentée (ex. : empêcher la suppression d'un employé qui n'existe pas).  
   ✅ Justification du choix du format de données.  

---

## **Exemples de cas d'utilisation :**  

### **Ajout d'employés :**  
L'utilisateur ajoute plusieurs employés avec leur nom et leur numéro d’identification.  

**Exemple d'entrée :**  
```
Ajout d'un employé : Nom = "Dupont", Numéro = 101
Ajout d'un employé : Nom = "Martin", Numéro = 102
Ajout d'un employé : Nom = "Durand", Numéro = 103
```

### **Affichage des employés :**  
Le programme affiche la liste complète des employés.  

**Exemple de sortie :**  
```
Liste des employés :
1. Dupont (ID : 101)
2. Martin (ID : 102)
3. Durand (ID : 103)
```

### **Suppression d'un employé :**  
L'utilisateur peut supprimer un employé en saisissant son nom ou son numéro d’identification.  

**Exemple d'entrée :**  
```
Supprimer un employé (Nom ou ID) : "Martin"
```

**Exemple de sortie :**  
```
L'employé "Martin" a été supprimé.
```

### **Affichage après suppression :**  
```
Liste des employés :
1. Dupont (ID : 101)
2. Durand (ID : 103)
```

---

## **Questions de réflexion :**  
- Quel format de données est le plus adapté entre **liste, tuple et dictionnaire** ? Pourquoi ?  
- Comment gérer les cas où un employé portant le même nom existe plusieurs fois ?  
- Quelle est la complexité des opérations d'ajout, suppression et recherche pour chaque format de données ?  

---

💡 **Bonus Challenge** : Ajouter la possibilité de modifier les informations d'un employé (changement de nom ou de numéro d’identification). 🚀
