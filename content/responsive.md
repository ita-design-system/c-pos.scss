---
title: Responsive
description: Fonctionnalités responsive du composant c-pos
layout: libdoc/page-split
order: 90
separator: true
---
Si le paramètre `responsive: true` est activé, les modifieurs du composant c-pos sont adaptables à chaque design token de taille d'écran `$briks-screen-sizes` comme suit.

## Classes responsives

Un modifieur peut être appliqué sur des design tokens de tailles d'écrans via des classes CSS

```html
<!-- Avec des classes CSS -->
<HTMLTag class="c-pos m-NOM_DU_MODIFIEUR--TOKEN_TAILLE_ECRAN"></HTMLTag>
```

## Attributs responsives

En parallèle des classes CSS, la syntaxe par attribut permet d'appliquer la même fonctionnalité d'un modifieur sur plusieurs tailles d'écran en une seule fois.

```html
L'attribut responsive du modifieur
<HTMLTag class="c-pos" m-NOM_DU_MODIFIEUR="TOKEN_TAILLE_ECRAN_1, TOKEN_TAILLE_ECRAN_2, TOKEN_TAILLE_ECRAN_3"></HTMLTag>

a le même effet que les classes CSS
<HTMLTag class="c-pos m-NOM_DU_MODIFIEUR--TOKEN_TAILLE_ECRAN_1 m-NOM_DU_MODIFIEUR--TOKEN_TAILLE_ECRAN_2 m-NOM_DU_MODIFIEUR--TOKEN_TAILLE_ECRAN_3"></HTMLTag>
```

```html
<!-- Avec des classes responsives -->
<div class="c-pos m-fixed--xs m-top-50--xs m-left-0--xs">
    Je passe en position: fixed<br> top: 50%<br> left: 0%<br> sur la taille d'écran xs<br> via des classes CSS
</div>
<!-- Avec l'attribut responsive - 1 taille d'écran -->
<div class="c-pos" 
    m-fixed="xs" 
    m-top-0="xs" 
    m-right-0="xs">
    Je passe en position: fixed<br> top: 0%<br> right: 0%<br> sur la taille d'écran xs<br> via l'attribut responsive
</div>
<!-- Avec l'attribut responsive - multiples tailles d'écrans -->
<div class="c-pos m-fixed m-bottom-0" 
    m-right-0="xs,sm"
    m-left-0="md,lg,xl">
    Je passe à droite<br> sur les tailles d'écran xs et sm<br> via l'attribut responsive
</div>
<!-- DEMO UNIQUEMENT -->
<style>
    body {
        padding: var(--ita-spacing-4);
        background-color: var(--ita-color-primary-100);
        color: var(--ita-color-primary-800);
        font-family: var(--ita-font-family-mono);
        font-size: 1rem;
        line-height: 1.5rem;
        height: 100vh;
    }
    .c-pos {
        background-color: var(--ita-color-primary-500);
        color: var(--ita-color-neutral-100);
        padding: var(--ita-spacing-4);
        border: var(--ita-border-5);
    }
</style>
```
{:.playground title="Exemples responsives"}