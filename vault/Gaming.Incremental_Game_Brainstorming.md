---
id: 4iK7uWzeRolsIIV2fUcPT
title: Incremental Game Brainstorming
desc: ''
updated: 1643160349171
created: 1643160045507
---

## Economy
- Based on amount of bodies in posession
- Mass effects how much a body yields.
- Ecomony mis mineral bsed

## Example of data that can be used
```
"bodies": [
    {
      "id": "lune",
      "name": "La Lune",
      "englishName": "Moon",
      "isPlanet": false,
      "moons": null,
      "semimajorAxis": 384400,
      "perihelion": 363300,
      "aphelion": 405500,
      "eccentricity": 0.0549,
      "inclination": 5.145,
      "mass": {
        "massValue": 7.346,
        "massExponent": 22
      },
      "vol": {
        "volValue": 2.1968,
        "volExponent": 10
      },
      "density": 3.344,
      "gravity": 1.62,
      "escape": 2380,
      "meanRadius": 1737,
      "equaRadius": 1738.1,
      "polarRadius": 1736,
      "flattening": 0.0012,
      "dimension": "",
      "sideralOrbit": 27.3217,
      "sideralRotation": 655.728,
      "aroundPlanet": {
        "planet": "terre",
        "rel": "https://api.le-systeme-solaire.net/rest/bodies/terre"
      },
      "discoveredBy": "",
      "discoveryDate": "",
      "alternativeName": "",
      "axialTilt": 6.68,
      "avgTemp": 0,
      "mainAnomaly": 0,
      "argPeriapsis": 0,
      "longAscNode": 0,
      "bodyType": "Moon",
      "rel": "https://api.le-systeme-solaire.net/rest/bodies/lune"
    },
    ```
    ### Important fields
    ```
    englishName
    isPlanet
    moons
    mass
    gravity
    avgTemp
    ```