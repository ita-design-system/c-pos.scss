---
title: z-index
description: Modifieurs c-pos dédiés au z-index
layout: libdoc/page-split
order: 140
---
```html
<div class="c-pos m-absolute m-z--1">m-z--1 <br>z-index: -1</div>
<div class="c-pos m-absolute m-z-1">m-z-1 <br>z-index: 1</div>
<div class="c-pos m-absolute m-z-2">m-z-2 <br>z-index: 2</div>
<div class="c-pos m-absolute m-z-3">m-z-3 <br>z-index: 3</div>
<div class="c-pos m-absolute m-z-4">m-z-3 <br>z-index: 4</div>
<div class="c-pos m-absolute m-z-5">m-z-5 <br>z-index: 5</div>
<div class="c-pos m-absolute m-z-6">m-z-6 <br>z-index: 6</div>
<!-- DEMO UNIQUEMENT -->
<style>
    body {
        padding: var(--ita-spacing-4);
        background-color: var(--ita-color-primary-100);
        color: var(--ita-color-primary-800);
        font-family: var(--ita-font-family-mono);
        font-size: 1rem;
        line-height: 1.5rem;
        height: 200vh;
    }
    .c-pos.m-absolute {
        background-color: var(--ita-color-primary-100);
        color: var(--ita-color-neutral-100);
        border: var(--ita-border-6);
        padding: var(--ita-spacing-4);
        width: 400px;
        height: 200px;
    }
    .c-pos.m-absolute:nth-child(1) {
        top: 0%;
        left: 0%;
        background-color: var(--ita-color-primary-200);
    }
    .c-pos.m-absolute:nth-child(2) {
        top: 15%;
        left: 15%;
        background-color: var(--ita-color-primary-300);
    }
    .c-pos.m-absolute:nth-child(3) {
        top: 30%;
        left: 30%;
        background-color: var(--ita-color-primary-400);
    }
    .c-pos.m-absolute:nth-child(4) {
        top: 45%;
        left: 45%;
        background-color: var(--ita-color-primary-400);
    }
    .c-pos.m-absolute:nth-child(5) {
        top: 60%;
        left: 60%;
        background-color: var(--ita-color-primary-600);
    }
    .c-pos.m-absolute:nth-child(6) {
        top: 75%;
        left: 75%;
        background-color: var(--ita-color-primary-700);
    }
    .c-pos.m-absolute:nth-child(7) {
        top: 90%;
        left: 90%;
        background-color: var(--ita-color-primary-800);
    }
</style>
```
{:.playground title="Modifieurs pour z-index"}