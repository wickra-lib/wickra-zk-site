# Rust

The native crate — the same engine every other binding of Wickra ZK wraps.

```bash
cargo add wickra-zk
```

```rust
use wickra_zk_host::{commit_dataset, prove, verify, ProveOptions, ZkSpec};

// The strategy and the candles are the private inputs; the proof is bound to
// the candles through their canonical hash, which the guest recomputes.
let spec = ZkSpec { strategy, dataset_commitment: commit_dataset(&candles)? };
let proof = prove(&spec, &candles, ProveOptions::default())?;

// Anyone verifies the receipt against the pinned guest and reads the journal
// from it -- the report hash, the commitment, sharpe, pnl, the trade count.
let journal = verify(&proof)?;
println!("report_hash: {}", journal.report_hash);
```

## More

- [crates.io/crates/wickra-zk](https://crates.io/crates/wickra-zk)
- [docs.rs](https://docs.rs/wickra-zk)
- [Source & examples](https://github.com/wickra-lib/wickra-zk/tree/main/examples)
