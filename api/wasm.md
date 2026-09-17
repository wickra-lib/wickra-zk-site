# WASM

**Wickra ZK — for WASM. `npm install wickra-zk-wasm` — pure WebAssembly, runs anywhere a modern JS engine does.**

```bash
npm install wickra-zk-wasm
```

```js
import init, { Verifier, version, guestId } from "wickra-zk-wasm";

await init();

const verifier = new Verifier();

// A proof file produced by the CLI or any native binding.
const outputs = JSON.parse(verifier.command(JSON.stringify({ cmd: "verify", proof })));
// { report_hash, dataset_commitment, guest_id, sharpe, pnl, n_trades }
// -- decoded from the receipt, never read from the file's own copy.

// A verifier who holds the candles checks what the proof is bound to.
const { dataset_commitment } = JSON.parse(verifier.command(JSON.stringify({ cmd: "commit", candles })));
console.log(dataset_commitment === outputs.dataset_commitment);

console.log(version(), guestId()); // the host version and the image id this build pins
```

## More

- [npm](https://www.npmjs.com/package/wickra-zk-wasm)
- [Source & examples](https://github.com/wickra-lib/wickra-zk/tree/main/examples/wasm)
