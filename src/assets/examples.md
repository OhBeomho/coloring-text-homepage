# Examples

<details>
  <summary><strong>Color function</strong></summary>

```js
const { color } = require("coloring-text")

console.log(color("Colored text!", "red"))
console.log(color("Background too!", "magenta", "gray"))
```

</details>
<details>
  <summary><strong>Style function</strong></summary>

```js
const { style } = require("coloring-text")

console.log(color("Blinking text!", "blink"))
console.log(color("Multiple styles!", "underscore", "dim", "blink"))
```

</details>
