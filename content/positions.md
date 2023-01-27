---
title: Positions
description: Modifieurs c-pos dédiés aux positions
layout: libdoc/page-split
order: 130
---
```html
<div class="c-pos m-absolute m-left-0 m-bottom-0">m-absolute <br>position: absolute<br>Je suis sur un nouveau calque</div>
<div class="c-pos m-fixed m-right-0 m-top-0">m-fixed <br>position: fixed</div>
<div class="c-pos m-sticky m-top-0">m-sticky (1)<br>position: sticky<br>Je m'arrête en haut de l'écran</div>
<div class="c-pos m-sticky m-top-0">m-sticky (2)<br>position: sticky<br>Je m'arrête en haut de l'écran</div>
<!-- DEMO UNIQUEMENT -->
<style>
    body {
        padding: var(--ita-spacing-4);
        background-color: var(--ita-color-primary-100);
        color: var(--ita-color-primary-800);
        font-family: var(--ita-font-family-mono);
        font-size: 1rem;
        line-height: 1.5rem;
        height: 300vh;
    }
    .c-pos {
        background-color: var(--ita-color-primary-500);
        color: var(--ita-color-neutral-100);
        border: var(--ita-border-6);
        padding: var(--ita-spacing-4);
    }
    .c-pos.m-sticky {
        margin-top: 40vh;
    }
</style>
```
{:.playground title="Modifieurs pour les positions"}