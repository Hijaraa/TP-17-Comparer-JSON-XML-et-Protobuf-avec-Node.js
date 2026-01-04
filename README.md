# TP-17: Comparer JSON, XML et Protobuf avec Node.js

Ce projet compare les performances et les tailles de fichiers entre trois formats de sérialisation de données : JSON, XML et Protobuf.

## Description

Le projet mesure et compare :
- **Temps d'encodage** : Temps nécessaire pour convertir les données en chaque format
- **Temps de décodage** : Temps nécessaire pour reconvertir les données depuis chaque format
- **Taille des fichiers** : Taille des fichiers générés pour chaque format

## Structure du projet

- `index.js` : Script principal qui effectue les comparaisons
- `employee.proto` : Définition du schéma Protobuf pour les employés
- `package.json` : Dépendances du projet

## Installation

```bash
npm install
```

## Exécution

```bash
node index.js
```

## Résultats attendus

Le script génère trois fichiers de données :
- `data.json` : Format JSON
- `data.xml` : Format XML
- `data.proto` : Format Protobuf (binaire)

### Exemple de sortie

```
JSON encode: ~0.2ms
JSON decode: ~0.02ms
XML encode: ~0.6ms
XML decode: ~2.7ms
Protobuf encode: ~0.4ms
Protobuf decode: ~0.3ms
Taille de 'data.json' : 127 octets
Taille de 'data.xml'  : 224 octets
Taille de 'data.proto': 41 octets
```

## Observations

- **JSON** : Le plus rapide pour l'encodage et le décodage, taille moyenne
- **XML** : Plus lent, surtout pour le décodage, taille la plus grande
- **Protobuf** : Très compact (plus petite taille), performance intermédiaire

## Dépendances

- `protobufjs` : Pour la sérialisation/désérialisation Protobuf
- `xml-js` : Pour la conversion entre JSON et XML

<img width="878" height="886" alt="image" src="https://github.com/user-attachments/assets/891439d7-9a66-41b1-bde6-0c8550de1c83" />


