# Détecteur de Discontinuités de Câbles

Cette application web permet d'analyser et d'identifier les discontinuités dans un réseau de câbles à partir d'un fichier CSV contenant les informations de câblage.

## Application en ligne

L'application est accessible en ligne à l'adresse suivante :
**[https://mxmohamed.github.io/cable-discontinuity-detector/](https://mxmohamed.github.io/cable-discontinuity-detector/)**

## Qu'est-ce qu'une discontinuité ?

Dans cette application, une **discontinuité** est définie comme une situation où :
- Les champs `cb_bp1` ET `cb_ba1` sont vides à l'extrémité 1, OU
- Les champs `cb_bp2` ET `cb_ba2` sont vides à l'extrémité 2

Les discontinuités indiquent potentiellement des problèmes de connexion dans le réseau de câbles qui nécessitent une attention particulière.

## Fonctionnalités

- **Chargement de fichiers CSV** : Importez facilement vos données de câbles au format CSV
- **Analyse automatique** : Identifie automatiquement les discontinuités selon les critères définis
- **Statistiques détaillées** : Affiche des métriques claires sur le nombre total de câbles, les discontinuités et leur répartition
- **Filtrage des résultats** : Possibilité d'afficher uniquement les câbles avec des discontinuités
- **Export des données** : Exportez les résultats au format CSV pour un traitement ultérieur
- **Données d'exemple intégrées** : Testez l'application sans avoir à télécharger un fichier CSV
- **Interface réactive** : Compatible avec tous les appareils (ordinateurs, tablettes, smartphones)

## Comment utiliser l'application

1. **Accédez à l'application** en ligne via le lien : [https://mxmohamed.github.io/cable-discontinuity-detector/](https://mxmohamed.github.io/cable-discontinuity-detector/)

2. **Chargez votre fichier CSV** :
   - Cliquez sur le bouton "Parcourir" pour sélectionner le fichier CSV contenant les données de câbles
   - Le fichier doit être au format CSV avec des points-virgules comme séparateurs (`;`)
   - Les colonnes nécessaires sont : `cb_code`, `cb_etiquet`, `cb_nd1`, `cb_nd2`, `cb_bp1`, `cb_ba1`, `cb_bp2`, `cb_ba2`, `cb_typelog`, `cb_lgreel`

3. **Analysez les données** :
   - Cliquez sur le bouton "Analyser" pour lancer l'analyse du fichier
   - Les résultats s'afficheront dans le tableau en bas de la page
   - Les lignes en rouge correspondent aux câbles avec des discontinuités

4. **Consultez les statistiques** :
   - Le nombre total de câbles analysés
   - Le nombre et pourcentage de câbles avec discontinuités
   - La répartition des discontinuités par type (extrémité 1, extrémité 2, ou les deux)

5. **Filtrez les résultats** :
   - Utilisez le bouton "Afficher uniquement les discontinuités" pour filtrer le tableau
   - Cliquez à nouveau pour afficher tous les câbles

6. **Exportez les données** :
   - Cliquez sur "Exporter en CSV" pour télécharger les résultats (filtrés ou non)

## Structure des données CSV

L'application attend un fichier CSV avec les colonnes suivantes :
- `cb_code` : Identifiant unique du câble
- `cb_etiquet` : Description ou étiquette du câble
- `cb_nd1` : Identifiant du premier nœud
- `cb_nd2` : Identifiant du deuxième nœud
- `cb_bp1` : Point de branchement à l'extrémité 1
- `cb_ba1` : Point d'arrivée à l'extrémité 1
- `cb_bp2` : Point de branchement à l'extrémité 2
- `cb_ba2` : Point d'arrivée à l'extrémité 2
- `cb_typelog` : Type logique du câble
- `cb_lgreel` : Longueur réelle du câble

## Exemple de fichier CSV

```
cb_code;cb_codeext;cb_etiquet;cb_nd1;cb_nd2;cb_bp1;cb_ba1;cb_bp2;cb_ba2;cb_typelog;cb_lgreel
FI000016546007;16546007;M-174/30276-FT / PBO-SRO-BPI-11406794-047;CH000004049918;SU000004534733;EN000012149305;;BL000008248512;;DI;25.93
FI000016542461;16542461;M-229/30276-FT / PBO-SRO-BPI-11406794-011;CH000004049589;CH000004258545;EN000012149297;;BL000008248252;;DI;55.93
FI000016546011;16546011;ARM-1830041 / BPE-284/30276-FT;PE000001968054;CH000004049267;;BA000010113076;EN000012149299;;DI;128.19
FI000047496423;47496423;BPE-02/30003-FT / BPE-154/30276-FT;CH000003120961;CH000004050560;;;;EN000012565617;;TR;3070.79
```

## Technologie

Cette application est développée avec les technologies web standard :
- HTML5
- CSS3 avec Bootstrap 5
- JavaScript moderne
- PapaParse (bibliothèque d'analyse CSV)

Aucune installation n'est nécessaire puisque l'application fonctionne directement dans votre navigateur web.
