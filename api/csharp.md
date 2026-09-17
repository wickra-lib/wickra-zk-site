# C#

**Wickra ZK — for C#. `dotnet add package Wickra.Zk` — prebuilt native library, no system dependencies.**

```bash
dotnet add package Wickra.Zk
```

The binding is a thin, faithful surface over the same command boundary every other binding drives, so a request built here produces the same canonical bytes it would in Rust, Python or Go.

```csharp
using Wickra.Zk;

using var handle = new Prover();
string response = handle.Command("""{"cmd":"version"}""");
Console.WriteLine(response);
```

## More

- [NuGet](https://www.nuget.org/packages/Wickra.Zk)
- [Source & examples](https://github.com/wickra-lib/wickra-zk/tree/main/examples/csharp)
