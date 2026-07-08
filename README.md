# AfriData Ready

**From Raw Data to FAIR & AI-Ready Data**

AfriData Ready est une application d'accompagnement pour transformer un fichier brut en jeu de donnees propre, documente, conforme aux principes FAIR et plus pret pour l'analyse ou l'intelligence artificielle.

Le projet contient deux interfaces :

- `index.html` : application web statique, utilisable dans le navigateur et deployable sur GitHub Pages.
- `app.py` : prototype Streamlit pour une execution Python locale.

## Fonctionnalites principales

1. Import de fichiers CSV, Excel ou JSON.
2. Diagnostic automatique de qualite : valeurs manquantes, doublons, colonnes vides, noms ambigus, formats incoherents et valeurs aberrantes.
3. Edition des donnees : cellules, colonnes, lignes, valeurs manquantes et doublons.
4. Documentation des variables : description, type, unite, format, valeurs possibles, regles de validation et role pour l'IA.
5. Metadonnees du jeu de donnees : auteur, licence, zone geographique, methode de collecte, citation, contact.
6. Evaluation FAIR et AI Readiness.
7. Score AQI interne, inspire de referentiels de qualite et de gouvernance des donnees.
8. Recommandations priorisees et actions automatiques.
9. Export d'un data product : donnees corrigees, dictionnaire, metadonnees, scores, rapport et certificat.

## Utilisation rapide

### Version web statique

Ouvrir directement `index.html` dans un navigateur moderne.

Cette version fonctionne localement, sans serveur applicatif. Les projets sauvegardes sont stockes dans le navigateur via IndexedDB.

### Version Streamlit

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Deploiement

Le workflow GitHub Pages est defini dans `.github/workflows/pages.yml`. A chaque push sur `main`, le contenu du depot peut etre publie comme site statique.

## Notes importantes

- Les scores FAIR, AI Readiness et AQI sont des evaluations internes indicatives. Ils ne constituent pas une certification officielle.
- Les donnees traitees dans la version statique restent cote navigateur, sauf action explicite d'export ou de partage.
- Les fichiers importes peuvent contenir des valeurs sensibles : verifier les colonnes personnelles avant export.

## References

- Wilkinson et al. (2016) - FAIR Principles
- Wang & Strong (1996) - Data Quality
- ISO 8000 / ISO 25012 - Data Quality
- ISO 11179 - Metadata registries
- DataCite / Dublin Core - Metadata
- Sambasivan et al. (2021) - Data Cascades in AI
- Andrew Ng - Data-Centric AI

---

Memoire DU Donnees - UCAD/EBAD - Patrick-Eudess Zatty ALLA - 2026
