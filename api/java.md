# Java

**Wickra ZK — for Java. `org.wickra:wickra-zk` — prebuilt native library inside the jar, no JNI, no system dependencies.**

```xml
<dependency>
  <groupId>org.wickra</groupId>
  <artifactId>wickra-zk</artifactId>
  <version>0.1.3</version>
</dependency>
```

```java
import org.wickra.zk.Prover;

try (Prover prover = new Prover()) {
    String cmd = """
        {"cmd":"prove","spec":{"strategy":{...}},
        "candles":[{"time":1,"open":100,"high":101,"low":99,"close":100,"volume":1000}]}""";
    System.out.println(prover.command(cmd));
    // {"receipt":…,"journal":{"report_hash":"…","dataset_commitment":"…","guest_id":"…",…},"version":"…"}
}
System.out.println(Prover.version());
```

## More

- [Maven Central](https://central.sonatype.com/artifact/org.wickra/wickra-zk)
- [Source & examples](https://github.com/wickra-lib/wickra-zk/tree/main/examples/java)
