# 📌 Checkpoint MongoDB – CRUD Operations

## 🎯 Objectif
Dans ce checkpoint, l'idée principale est de manipuler les opérations **CRUD** (Create, Read, Update, Delete) de MongoDB.

---

## 🗄️ Étapes du projet

### 1. Créer une base de données
```js
use contact 
Créer une collection
db.createCollection("contactlist")


3. Insérer des documents
db.contactlist.insertMany([
  { nom: "Ben", prenom: "Moris", email: "ben@gmail.com", age: 26 },
  { nom: "Kefi", prenom: "Seif", email: "kefi@gmail.com", age: 15 },
  { nom: "Emilie", prenom: "brouge", email: "emilie.b@gmail.com", age: 40 },
  { nom: "Alex", prenom: "brown", age: 4 },
  { nom: "Denzel", prenom: "Washington", age: 3 }
])


📋 Instructions
🔎 Lire (Read)
- Afficher toute la liste des contacts :
db.contactlist.find()


- Afficher toutes les informations sur une seule personne en utilisant son ID :
db.contactlist.find({ _id: ObjectId("ID_DE_LA_PERSONNE") })


- Afficher tous les contacts ayant un âge > 18 :
db.contactlist.find({ age: { $gt: 18 } })


- Afficher tous les contacts ayant un âge > 18 et dont le nom contient "ah" :
db.contactlist.find({ age: { $gt: 18 }, nom: /ah/ })


✏️ Mettre à jour (Update)
- Changer le prénom du contact "Kefi Seif" en "Kefi Anis" :
db.contactlist.updateOne(
  { nom: "Kefi", prenom: "Seif" },
  { $set: { prenom: "Anis" } }
)


🗑️ Supprimer (Delete)
- Supprimer les contacts qui ont moins de 5 ans :
db.contactlist.deleteMany({ age: { $lt: 5 } })


🔎 Vérification finale
- Afficher toute la liste des contacts après suppression :
db.contactlist.find()



🖼️ Captures d'écran
👉 N'oubliez pas de sauvegarder votre travail sous forme de captures d'écran pour valider le checkpoint.

📂 Dépôt GitHub
Lien du projet : https://github.com/mokas2017/cp-MongoDB.git
