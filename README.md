# Intégration des Parcelles de l'API ULDK

Ecoute les notifications d'un canal PostgreSQL (table temp de requetage) afin d'aller chercher les informations cadastrales depuis l'[API ULDK](https://uldk.gugik.gov.pl) (Pologne) et d'intégrer les parcelles obtenues dans la base.

---

## ⚙️ Fonctionnalités principales

- **Écoute continue** du canal via `LISTEN/NOTIFY`.
- **Extraction automatique des points de requête à leur création**.
- **Interrogation de l'API ULDK** sur ces points, pour récupérer les données cadastrales (identifiants, geom...).
- **Insertion des résultats** dans la table de destination.
- **Nettoyage de la table temporaire** après traitement.

`config.txt` a été caché.

---

## 🌐 API utilisée

Le code interroge cette API publique polonaise : 
URL : `https://uldk.gugik.gov.pl/?request=GetParcelByXY`  

---
