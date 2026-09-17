# Node

**Wickra ZK — for Node.js. `npm install wickra-zk` — prebuilt native binary, no system dependencies.**

```bash
npm install wickra-zk
```

```js
const { Prover } = require("wickra-zk");

const prover = new Prover();
console.log(JSON.parse(prover.command(JSON.stringify({ cmd: "version" }))));
```

## More

- [npm](https://www.npmjs.com/package/wickra-zk)
- [Source & examples](https://github.com/wickra-lib/wickra-zk/tree/main/examples/node)
