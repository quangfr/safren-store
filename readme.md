## Vision "Safren Play Store" – Boîte à outils décisionnelle (AWS)

### 🎯 Idée générale
Un portail unique, simple et rapide pour accéder à toutes les petites applications utiles aux équipes Safren : atelier, logistique, support, qualité, engineering.

---

### 🧰 Ce que propose le Safren Play Store
- Une **entrée unique** pour tous les outils du quotidien.  
- Accessible sur **PC / tablette / mobile**, même en déplacement.  
- Chaque app répond à **un besoin métier clair** : préparer, analyser, décider, prioriser, alerter, simuler.

---

### 🔧 Exemples d’applications (Fast Apps – moteur d’avion)
- Prépa workscope express  
- Tri findings critique  
- Scrap vs repair guidé  
- Suivi pièces critiques / priorités AOG  
- Mini cockpit TAT/OTD (CSV → graphs)  
- Synthèse dossier moteur  
- Déviation / concession simplifiée  
- Générateur CR incident  
- Historique moteur rapide  
- **Simulateur de calcul** (coût, délai, charge, TAT, capacité)  
- **Conversion fichier Excel → mini-app** (importer → visualiser, filtrer, résumer)  
- **App légère serverless APIsé** exposant ou collectant des données opérationnelles (pièces critiques, modules, écarts qualité…)

---

### 🔐 Auth simplifiée (AWS)
- Connexion **SSO Safren** une seule fois.  
- Le Play Store affiche uniquement les apps autorisées pour le métier / rôle.  
- Les apps n’ont pas à gérer l’authentification.

---

### ⚙️ Côté AWS (version courte)
- **S3 + CloudFront** : héberge le Play Store + les fast apps HTML/CSS/JS
- **Lambda / API Gateway** : petites APIs pour :
  - lire des données opérationnelles,  
  - exposer une vue filtrée (pièces critiques, modules…),  
  - envoyer une notification
  - transformer / faire les mappings de données (middlewares)   
- **SSO central** : Cognito / IAM Identity Center.

---

### 🧭 Pour les opérationnels Safren
- Un seul portail → tous les outils utiles.  
- Moins de liens éparpillés, moins d’Excel cachés.  
- Décisions plus rapides, plus cohérentes, même en mobilité.
