---
layout: home
title: "Wickra ZK — Prove a backtest in zero knowledge: on-chain-verifiable performance without revealing the data or the strategy behind it"
titleTemplate: false

hero:
  name: "Wickra ZK"
  text: "Prove it without showing it."
  tagline: "Zero-knowledge, on-chain-verifiable backtest performance — without revealing your data or your strategy."
  image:
    src: /wickra-mark.svg
    alt: "Wickra ZK"
  actions:
    - theme: brand
      text: View on GitHub
      link: https://github.com/wickra-lib/wickra-zk
    - theme: alt
      text: How it works
      link: /about

features:
  - icon: 🕶️
    title: "The strategy stays private"
    details: "The proof establishes that a backtest with a given result was run, without disclosing the specification that produced it or the data it ran over."
  - icon: ⛓️
    title: "Verifiable on-chain"
    details: "The verification step is cheap enough to run where the claim matters, rather than requiring the verifier to trust a report."
  - icon: 🔁
    title: "Deterministic underneath"
    details: "A zero-knowledge proof is only as meaningful as the computation it covers. The one underneath is the deterministic Wickra engine, whose output is reproducible by construction."
  - icon: ⚙️
    title: "Built on the core"
    details: "The same engine and the same 514 indicators as the rest of the stack."
---

<script setup>
const installTabs = [
  { label: 'Python', lang: 'bash', code: 'pip install wickra-zk' },
  { label: 'Node', lang: 'bash', code: 'npm install wickra-zk' },
  { label: 'Rust', lang: 'bash', code: 'cargo add wickra-zk' },
  { label: 'WASM', lang: 'bash', code: 'npm install wickra-zk-wasm' },
  { label: 'C', lang: 'bash', code: '# prebuilt header + library from GitHub releases:\n# github.com/wickra-lib/wickra-zk/releases' },
  { label: 'C#', lang: 'bash', code: 'dotnet add package Wickra.Zk' },
  { label: 'Go', lang: 'bash', code: 'go get github.com/wickra-lib/wickra-zk-go' },
  { label: 'Java', lang: 'xml', code: '<!-- Maven Central -->\n<dependency>\n  <groupId>org.wickra</groupId>\n  <artifactId>wickra-zk</artifactId>\n  <version>0.1.3</version>\n</dependency>' },
  { label: 'R', lang: 'r', code: 'install.packages("wickrazk", repos = "https://wickra-lib.r-universe.dev")' },
]
</script>

## Install

The same engine from every language — native Rust, Python, Node.js and WASM, plus a C
ABI for C, C++, C#, Go, Java and R.

<InstallTabs :tabs="installTabs" />

The [API pages](/api/rust) carry a quick start per language; the
[repository README](https://github.com/wickra-lib/wickra-zk#readme) the same in one place.

## Built on the Wickra core

Wickra ZK is part of the [Wickra](https://wickra.org) ecosystem — one indicator core,
twenty-three products, the same ten-language binding surface in every one of them,
checked byte-for-byte by a golden corpus in every repository.

> Wickra ZK is a software library, not a trading system, and gives no financial
> advice — its outputs are deterministic transforms of the input data and do not
> predict future returns. Use it at your own risk.
