# R

**Wickra ZK — for R. `install.packages("wickrazk", repos = "https://wickra-lib.r-universe.dev")` — over the C ABI via `.Call`, prebuilt library fetched on install.**

```r
install.packages("wickrazk", repos = "https://wickra-lib.r-universe.dev")
```

```r
library(wickrazk)

prover <- wkzk_new()
cmd <- paste0(
  '{"cmd":"prove","spec":{"strategy":{...}},',
  '"candles":[{"time":1,"open":100,"high":101,"low":99,"close":100,"volume":1000}]}'
)
cat(wkzk_command(prover, cmd), "\n")
# {"receipt":…,"journal":{"report_hash":"…","dataset_commitment":"…","guest_id":"…",…},"version":"…"}
cat(wkzk_version(), "\n")
```

## More

- [r-universe](https://wickra-lib.r-universe.dev)
- [Source & examples](https://github.com/wickra-lib/wickra-zk/tree/main/examples/r)
