# Swagger Brief

### API DOC
https://swagger.io/specification/#version-3.0.3

##### openapi
Sert à définir la version de la [spécification OpenAPI](https://swagger.io/specification/#versions) utilisé.

##### info
Sert à définir les métadonnées

##### servers
Sert à définir les informations de connectivité à un serveur cible

##### tags
Sert à définir regrouper les groupes
exemple : 
Création du tag *developers*
```
tags:
  - name: developers
    description: Operations available to regular developers
```
Attribution du tag *developers*
```
paths:
  /addAnimal:
    post:
      tags:
        - developers
```

##### paths
la route

##### components
[Les composants](https://swagger.io/docs/specification/components/)

Pour éviter de crée un doublon d'objet, on utilise une référence à un objet avec
```# Swagger Brief

### API DOC
https://swagger.io/specification/#version-3.0.3

##### openapi
Sert à définir la version de la [spécification OpenAPI](https://swagger.io/specification/#versions) utilisé.

##### info
Sert à définir les métadonnées

##### servers
Sert à définir les informations de connectivité à un serveur cible

##### tags
Sert à définir regrouper les groupes
exemple : 
Création du tag *developers*
```
tags:
  - name: developers
    description: Operations available to regular developers
```
Attribution du tag *developers*
```
paths:
  /addAnimal:
    post:
      tags:
        - developers
```

##### paths
la route

##### components
[Les composants](https://swagger.io/docs/specification/components/)

Pour éviter de crée un doublon d'objet, on utilise une référence à un objet avec
```
 /quelquechose:
    get:
      summary: Get all choses
      responses:
        '200':
          description: A list of choses.
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/Objet'
```
Définit après les paths comme ceci
```
components:
  schemas:
    Objet:
      type: object
      properties:
        id:
          type: integer
        name:
          type: string
```

##### externalDocs
Documentation externe supplémentaire


    get:
      summary: Get all choses
      responses:
        '200':
          description: A list of choses.
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/Objet'
```
Définit après les paths comme ceci
```
components:
  schemas:
    Objet:
      type: object
      properties:
        id:
          type: integer
        name:
          type: string
```

##### externalDocs
Documentation externe supplémentaire

