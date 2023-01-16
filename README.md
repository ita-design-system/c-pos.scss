# c-pos.scss

[Démo et documentation](https://ita-design-system.github.io/c-pos.scss/)

Composant générique CSS c-pos dédié aux positionnements. 

## Typologie d'un composant générique

```scss
// SCSS map
$briks-components-generic: ( 
    // SCSS map | Nom du composant
    NOM_DU_COMPOSANT: ( 
        // Boolean | Composant activé true ou false
        enabled: true, 
        // Boolean | Responsive activé true ou false
        responsive: true, 
        // SCSS map | Liste des propriétés du composant par défaut
        defaults: (), 
        // SCSS map | Liste des modifieurs
        modifiers: () 
    )
);
```

## Configuration

Organisation et description du fichier de configuration [_sass/_pos_generic.scss](_sass/_pos_generic.scss).

```scss
/*
    C-POS
    Composant générique CSS ITADS
    https://github.com/ita-design-system/c-pos.scss
*/
// SCSS map
$briks-components-generic: ( 
    // Nom du composant
    pos: ( 
        // Composant activé true ou false
        enabled: true, 
        // Responsive activé true ou false
        responsive: true, 
        // Liste des propriétés c-pos par défaut
        defaults: (),
        // Rendu: 
        // c-pos {
        // }
        // Liste des modifieurs contenant chacun une liste de propriétés qui 
        // soit surchargent les propriétés par défaut
        // soit ajoutent des propriétés
        // soit les deux
        modifiers: ( 
            // c-pos m-absolute
            absolute: (
                position: absolute
            ),
            // c-pos m-fixed
            fixed: (
                position: fixed
            ),
            // c-pos m-sticky
            sticky: (
                position: sticky
            ),
            // c-pos m-relative
            relative: (
                position: relative
            ),
            // c-pos m-offset-50-50
            offset-50-50: (
                transform: translateX(-50%) translateY(-50%)
            ),
            // c-pos m-offset-0-50
            offset-0-50: (
                transform: translateX(0%) translateY(-50%)
            ),
            // c-pos m-offset-50-0
            offset-50-0: (
                transform: translateX(50%) translateY(0%)
            ),
            // c-pos m-top-0
            top-0: (
                top: 0%
            ),
            // c-pos m-top-50
            top-50: (
                top: 50%
            ),
            // c-pos m-top-100
            top-100: (
                top: 100%
            ),
            // c-pos m-right-0
            right-0: (
                right: 0%
            ),
            // c-pos m-right-50
            right-50: (
                right: 50%
            ),
            // c-pos m-right-100
            right-100: (
                right: 100%
            ),
            // c-pos m-bottom-0
            bottom-0: (
                bottom: 0%
            ),
            // c-pos m-bottom-50
            bottom-50: (
                bottom: 50%
            ),
            // c-pos m-bottom-100
            bottom-100: (
                bottom: 100%
            ),
            // c-pos m-left-0
            left-0: (
                left: 0%
            ),
            // c-pos m-left-50
            left-50: (
                left: 50%
            ),
            // c-pos m-left-100
            left-100: (
                left: 100%
            ),
            // c-pos m-anchor-top-left
            anchor-top-left: (
                transform: translateX(0%) translateY(0%)
            ),
            // c-pos m-anchor-top-center
            anchor-top-center: (
                transform: translateX(-50%) translateY(0%)
            ),
            // c-pos m-anchor-top-right
            anchor-top-right: (
                transform: translateX(-100%) translateY(0%)
            ),
            // c-pos m-anchor-middle-left
            anchor-middle-left: (
                transform: translateX(0%) translateY(-50%)
            ),
            // c-pos m-anchor-middle-center
            anchor-middle-center: (
                transform: translateX(-50%) translateY(-50%)
            ),
            // c-pos m-anchor-middle-right
            anchor-middle-right: (
                transform: translateX(-100%) translateY(-50%)
            ),
            // c-pos m-anchor-bottom-left
            anchor-bottom-left: (
                transform: translateX(0%) translateY(-100%)
            ),
            // c-pos m-anchor-bottom-center
            anchor-bottom-center: (
                transform: translateX(-50%) translateY(-100%)
            ),
            // c-pos m-anchor-bottom-right
            anchor-bottom-right: (
                transform: translateX(-100%) translateY(-100%)
            ),
            // c-pos m-z--1
            z--1: (
                z-index: -1
            ),
            // c-pos m-z-1
            z-1: (
                z-index: 100
            ),
            // c-pos m-z-2
            z-2: (
                z-index: 200
            ),
            // c-pos m-z-3
            z-3: (
                z-index: 300
            ),
            // c-pos m-z-4
            z-4: (
                z-index: 400
            ),
            // c-pos m-z-5
            z-5: (
                z-index: 500
            ),
            // c-pos m-z-6
            z-6: (
                z-index: 600
            )
        )
    )
);
``` 

## Extensions

Il est possible d'étendre les fonctionnalités du composant en ajoutant simplement un point d'entrée avec une déclaration `$briks-components-generic` à la typologie identique mais avec des propriétés par défaut et des modifieurs qui surchargent ou ajoutent des propriétés CSS.

Exemple.

```scss
/*
    C-POS EXTENSION
    Extension du composant générique c-pos
    https://github.com/ita-design-system/c-pos.scss
    Ce fichier doit servir à étendre ou surcharger les fonctionnalités
    du composant c-pos selon les besoins du projet
*/
$briks-components-generic: (
    // Nom du composant, obligatoirement pos
    pos: ( 
        // Extension activée true ou false
        enabled: true, 
        // Responsive activée true ou false pour l'extension
        responsive: true, 
        // Valeurs par défaut de l'extension
        defaults: (),
        // Liste des modifieurs contenant chacun une liste de propriétés qui 
        // soit surchargent les propriétés par défaut
        // soit ajoutent des propriétés
        // soit les deux
        modifiers: ( 
            // Ajout de valeurs de propriétés liées aux design tokens d'espacements
            // c-pos m-top-1
            top-1: (
                top: my-spcaing(1)
            ),
            // c-pos m-top-2
            top-2: (
                top: my-spcaing(2)
            ),
            // c-pos m-top-1
            right-1: (
                right: my-spcaing(1)
            ),
            // c-pos m-top-2
            top-2: (
                right: my-spcaing(2)
            )
            // etc
        )
    )
);
```
