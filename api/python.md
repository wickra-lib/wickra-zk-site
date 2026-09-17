# Python

**Wickra ZK — for Python. `pip install wickra-zk` — prebuilt wheels for Linux, macOS and Windows, nothing to compile.**

```bash
pip install wickra-zk
```

```python
import json
import wickra_zk

prover = wickra_zk.Prover()
print(json.loads(prover.command(json.dumps({"cmd": "version"}))))
```

## More

- [PyPI](https://pypi.org/project/wickra-zk/)
- [Source & examples](https://github.com/wickra-lib/wickra-zk/tree/main/examples/python)
