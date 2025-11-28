# Vision "Safren Play Store" – Boîte à outils décisionnelle (AWS)

## 🎯 Idée générale
Un portail unique, simple et rapide pour accéder à toutes les petites applications utiles aux équipes Safren : atelier, logistique, support, qualité, engineering.

## 🧰 Ce que propose le Safren Play Store
- Une entrée unique pour tous les outils du quotidien.  
- Accessible PC / tablette / mobile, même en déplacement.  
- Chaque app répond à un besoin métier clair : préparer, analyser, décider, prioriser, alerter, simuler.

## 🔧 Exemples d’applications (Fast Apps – moteur d’avion)
- Prépa workscope express  
- Tri findings critique  
- Scrap vs repair guidé  
- Suivi pièces critiques / AOG  
- Mini cockpit TAT/OTD (CSV → graphs)  
- Synthèse dossier moteur  
- Déviation / concession simplifiée  
- Générateur CR incident  
- Historique moteur rapide  
- Simulateur de calcul (coût, charge, capacité…)  
- Conversion Excel → mini-app (import / filtres / résumé)  
- App légère serverless exposant une donnée opérationnelle ciblée ou remontant la donnée terrain

## 🔐 Auth simplifiée (AWS)
- Connexion SSO Safren une seule fois.  
- Le Play Store affiche uniquement les apps autorisées selon métier / rôle.  
- Les apps n’ont pas à gérer l’authentification.

## ⚙️ Côté technique AWS – version courte
- **S3 + CloudFront** : hébergement Play Store + fast apps en front 
- **Lambda / API Gateway** :  
  - lecture et exposition de données opérationnelles  
  - vues filtrées métier  
  - notifications  
  - mappings / transformations  
- **SSO central** : Cognito / IAM Identity Center  

---

# 👤 Vision du nouveau Product Owner
- Va **sur le terrain** pour capter les besoins réels.  
- Porte un **périmètre d’apps** en autonomie, en coordination avec les autres PO.  
- Maîtrise **agents de coding + APIs** pour livrer vite et propre.  
- Travaille avec l’IT pour sécuriser, industrialiser, déployer.  
- Maintient une **documentation auto-générée** fidèle au code.  
- Simplifie, tranche, retire les apps qui ne servent plus.

---

# 🧭 Vision du Product Manager (portefeuille applicatif)
- Ordonne et **consolide** l’ensemble des fast apps.  
- Garantit un **écosystème cohérent**, sans redondance et à forte valeur métier.  
- Priorise les investissements : où placer les PO, où fusionner, où arrêter.  
- Unifie les pratiques : design commun, patterns, qualité, sécurité.  
- Porte la vision globale et la feuille de route transverse.

---

# 🌐 Tendances

## 🏗️ Architecture & Tech
- Serverless généralisé  
- Documentation auto-générée  
- Standardisation UX/UI  
- Gouvernance légère pour éviter la prolifération

## 👥 Métier & Produit
- Autonomisation des métiers via PO terrain + agents de coding  
- Évolutions continues, petites livraisons fréquentes  
- Sortie progressive des solutions marché → in-house

## 🔐 Data & Sécurité
- IT garante du cadre conception / qualité / sécurité / coûts / infra  
- APIs maîtrisées, data exposée de façon ciblée  
- Montée en compétence sur la qualité et l'analyse de données  
