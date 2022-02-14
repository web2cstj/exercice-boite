# Des boîtes en vrac

## Objectifs
- Explorer chaque propriété affectant la boîte individuellement avant de la mettre en contexte réel.

## Préparation
1. Créer un fichier `index.html`
1. Ajouter le squelette de la page avec `html:5`
1. Lier la feuille de style `base.css`
1. Lier la feuille de style `style.css`
1. Ajouter le contenu de la page dans le `body` à l'aide de la commande _Emmet_ suivante(`copier-coller`⇒`CTRL-Espace`⇒`Enter`):
    ```css
    div.interface>h1+div.groupe.flex>h2+p*26[tabindex=0][id][class]>lorem
    ```
    - L'attribut `tabindex` sert à pouvoir utiliser la pseudo-classe `:focus` dans notre CSS.
    - Par défaut, les éléments vont se placer les uns à côté des autres. Vous pouvez enlever la classe ``"flex"`` au `<div class="group flex">` pour éviter ce comportement.
    - Vous pouvez cacher un élément en lui ajoutant la classe `"fait"`;
    - Lorsqu'un élément est cliqué (focus), un contour pointillé rouge apparaît pour le différencier des autres.
    - Tant qu'un élément n'a pas de id, il sera semi-transparent.

## Règles
Tour à tour, il faudra créer 4 règles CSS pour chaque élément HTML en utilisant son id et des pseudo-classes. On utilisera les lettres majuscules comme id.
```css
#A {...}    /* L'état de départ de l'élément. */
#A:hover {...}    /* L'état de l'élément lorsque la souris passe au-dessus. */
#A:hover:focus {...}    /* L'état de l'élément lorsque la souris passe au-dessus et qu'il vient d'être cliqué.  */
#A:focus {...}    /* L'état de l'élément lorsqu'il vient d'être cliqué, mais que la souris ne passe pas au-dessus.  */
```

## Transition
Il se peut que la transition d'un état à l'autre donne un affichage un peu cahotique par moment. Vous pouvez augmenter ou réduire la vitesse de transition en changeant la valeur de propriété `transition-duration`dans le fichier `base.css`.