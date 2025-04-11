# Détecteur de Discontinuités de Câbles

Application web simple pour identifier les discontinuités dans un fichier CSV de câbles.

## Accès à l'application

[https://mxmohamed.github.io/cable-discontinuity-detector/](https://mxmohamed.github.io/cable-discontinuity-detector/)

## Définition d'une discontinuité

Une discontinuité est identifiée lorsque:
- Les deux champs cb_bp1 ET cb_ba1 sont vides à l'extrémité 1, OU
- Les deux champs cb_bp2 ET cb_ba2 sont vides à l'extrémité 2

## Utilisation

1. Cliquez sur "Parcourir" pour sélectionner votre fichier CSV
2. Cliquez sur "Analyser"
3. Les câbles avec discontinuités sont affichés en rouge
4. Utilisez le bouton "Afficher uniquement les discontinuités" pour filtrer

## Format du fichier CSV

- Le fichier doit utiliser des points-virgules (;) comme séparateurs
- Doit contenir les colonnes: cb_code, cb_etiquet, cb_bp1, cb_ba1, cb_bp2, cb_ba2

## Exemple

```
cb_code;cb_etiquet;cb_bp1;cb_ba1;cb_bp2;cb_ba2
FI000016546007;Câble 1;EN000012149305;;BL000008248512;
FI000016542461;Câble 2;EN000012149297;;BL000008248252;
FI000016546011;Câble 3;;BA000010113076;EN000012149299;
FI000047496423;Câble 4;;;;EN000012565617;
```
