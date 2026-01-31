# 🎓 Plateforme d'Acculturation IA - Module 1

Plateforme e-learning gamifiée avec tracking central pour former vos 1500 collaborateurs aux bases de l'Intelligence Artificielle.

## ✨ Fonctionnalités

### Pour les apprenants (index.html)
- ✅ **5 leçons progressives** (15 min) sur les bases de l'IA
- 🎮 **Gamification complète** : points, badges, progression
- 🔒 **Déverrouillage séquentiel** des leçons
- 📝 **Quiz interactifs** avec feedback immédiat
- 💾 **Sauvegarde automatique** de la progression
- ⏱️ **Tracking du temps** passé sur chaque leçon
- 🏆 **Système de badges** à débloquer

### Pour les administrateurs (admin.html)
- 📊 **Dashboard complet** avec statistiques en temps réel
- 👥 **Vue détaillée** de chaque apprenant
- 📈 **Analytics avancés** (par département, leçon, quiz)
- 🔍 **Filtres et recherche** puissants
- 📥 **Export Excel** des données
- 🎯 **Insights détaillés** sur l'engagement et la performance

## 🚀 Déploiement sur GitHub Pages (GRATUIT)

### Étape 1 : Préparer le repository GitHub

1. **Créez un compte GitHub** (si vous n'en avez pas) : https://github.com/signup

2. **Créez un nouveau repository**
   - Cliquez sur "New repository"
   - Nom : `acculturation-ia` (ou autre nom de votre choix)
   - Sélectionnez "Public"
   - Cochez "Add a README file"
   - Cliquez sur "Create repository"

### Étape 2 : Uploader les fichiers

1. Sur la page de votre repository, cliquez sur "Add file" → "Upload files"

2. Glissez-déposez ces 3 fichiers :
   - `index.html` (module e-learning)
   - `admin.html` (dashboard admin)
   - `README.md` (ce fichier)

3. Cliquez sur "Commit changes"

### Étape 3 : Activer GitHub Pages

1. Dans votre repository, allez dans **Settings** (⚙️ en haut)

2. Dans le menu de gauche, cliquez sur **Pages**

3. Sous "Source" :
   - Sélectionnez `main` (branche)
   - Sélectionnez `/ (root)` (dossier)
   - Cliquez sur "Save"

4. ✅ **Votre site sera accessible en 2-3 minutes à** :
   ```
   https://VOTRE-USERNAME.github.io/acculturation-ia/
   ```

### Étape 4 : Accès aux pages

- **Page apprenants** : `https://VOTRE-USERNAME.github.io/acculturation-ia/`
- **Dashboard admin** : `https://VOTRE-USERNAME.github.io/acculturation-ia/admin.html`

## 📋 Utilisation

### Pour les apprenants

1. Allez sur l'URL principale
2. Remplissez le formulaire d'inscription (prénom, nom, email, département)
3. Commencez le module !
4. La progression est sauvegardée automatiquement

### Pour les administrateurs

1. Allez sur l'URL `/admin.html`
2. Visualisez les statistiques en temps réel
3. Filtrez par département, statut, ou recherchez un apprenant
4. Exportez les données en CSV pour Excel

## 🔒 Sécurité & Confidentialité

### Stockage des données

Les données sont stockées de deux manières :

1. **Progression individuelle** : Dans le navigateur de chaque utilisateur (localStorage)
2. **Tracking central** : Via le système de stockage persistant de Claude (pour le dashboard admin)

### Protection des données personnelles

- ✅ Pas de serveur externe
- ✅ Données hébergées sur GitHub (infrastructure sécurisée)
- ✅ Conforme RGPD (données minimales collectées)
- ✅ Les utilisateurs peuvent effacer leurs données à tout moment

### Accès au dashboard admin

**Important** : Le dashboard admin est public. Pour le protéger :

**Option 1 : Protection par mot de passe (simple)**

Ajoutez ce code au début du fichier `admin.html`, juste après `<body>` :

```html
<script>
const ADMIN_PASSWORD = "votre-mot-de-passe-ici";
const entered = prompt("Mot de passe administrateur :");
if (entered !== ADMIN_PASSWORD) {
    alert("Accès refusé");
    window.location.href = "/";
}
</script>
```

**Option 2 : Repository privé (recommandé)**

1. Allez dans Settings → Change visibility → Make private
2. Invitez uniquement les personnes autorisées (Settings → Collaborators)

**Option 3 : Hébergement interne**

Pour une sécurité maximale, hébergez sur l'intranet de votre entreprise.

## 📊 Données collectées

### Par apprenant
- Prénom, Nom
- Email professionnel
- Département
- Progression (% de complétion)
- Points gagnés
- Scores aux quiz
- Nombre de tentatives par quiz
- Temps passé
- Badges débloqués
- Date/heure de dernière activité

### Statistiques globales
- Nombre total d'apprenants
- Taux de complétion moyen
- Score moyen aux quiz
- Temps moyen passé
- Performance par département
- Performance par leçon

## 🎨 Personnalisation

### Changer les couleurs

Dans le fichier `index.html` ou `admin.html`, modifiez les variables CSS (ligne ~10) :

```css
:root {
    --primary: #1a4d7a;        /* Couleur principale */
    --accent: #d4af37;         /* Couleur d'accentuation */
    --success: #10b981;        /* Couleur succès */
}
```

### Changer le logo ou le titre

Modifiez le titre dans la section `<h1>` du fichier HTML.

### Ajouter/Modifier les départements

Dans `index.html`, ligne ~500, modifiez la liste des départements dans le `<select>`.

## 🔄 Mise à jour du contenu

Pour modifier le contenu des leçons :

1. Éditez le fichier `index.html`
2. Trouvez la section `const lessons = [...]` (ligne ~1100 environ)
3. Modifiez le texte, les quiz, etc.
4. Re-uploadez sur GitHub
5. Les changements seront visibles immédiatement

## 📈 Évolutions futures possibles

- [ ] Modules 2 à 12
- [ ] Certificats PDF générés automatiquement
- [ ] Notifications par email des progressions
- [ ] Leaderboard visible par les apprenants
- [ ] Quiz en temps limité
- [ ] Ressources téléchargeables
- [ ] Forum de discussion intégré

## 🆘 Support

### Problèmes courants

**"Le site ne s'affiche pas"**
- Attendez 3-5 minutes après activation de GitHub Pages
- Vérifiez que l'URL est correcte
- Videz le cache de votre navigateur (Ctrl+F5)

**"Les données ne se sauvegardent pas"**
- Vérifiez que le navigateur autorise le stockage local
- Vérifiez que JavaScript est activé
- Essayez un autre navigateur

**"Le dashboard admin est vide"**
- Vérifiez qu'au moins un utilisateur a commencé le module
- Actualisez la page (bouton 🔄 Actualiser)
- Vérifiez la console développeur (F12) pour les erreurs

### Contact

Pour toute question ou amélioration, créez une "Issue" sur GitHub.

## 📄 Licence

Ce projet est fourni "tel quel" pour usage interne d'entreprise.

---

**Fait avec ❤️ pour l'acculturation IA de vos équipes** 🚀
