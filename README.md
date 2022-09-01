Small package for togglling everything on everywhere.

## Installation

### CDN
```html
<script src="https://unpkg.com/@amirhossein5/dropy"></script>

<script>
    document.addEventListener('DOMContentLoaded', () => {
        dropy('[toggler]');
    });
</script>
```

### npm
```sh
npm i @amirhossein5/dropy
```

And in js file:
```js
import dropy from '@amirhossein5/dropy';

dropy('[toggler]');
// or
window.dropy = dropy;
```

## Usage

There are two ways to define the target, first: append ```toggler-target``` attribute on the sibling of toggler,
```html
<section>
    <button toggler>toggle it!</button>
    <section toggler-target>will be toggle</section>
</section>
```

Or you can specify target via ```data-target```:
```html
<section>
    <button toggler data-target="#target">toggle it!</button>
</section>

<section id="target">will be toggle</section>
```

if you want to on first load target be open add attribute ```data-is-open```:

```html
<button toggler data-is-open="true">toggle it!</button>
```


## Options
```js
    dropy(togglerSelector, {
        onOpen: (target, toggler) => ..., // opening target is your responsible
        onClose: (target, toggler) => ..., // closing target is your responsible
        closeOnClickOut: true,
        closeOnAnotherTogglerClicked: true
    });
```

- ```closeOnClickOut```: when clicked out closes the target.
- ```closeOnAnotherTogglerClicked```: closes the target when another toggler clicked.


## Licence
