# provider-transport

Opt-in JVM socket/TLS provider for the bounded Kotoba transport ABI.

This is a Chicory tender plugin, not part of `kototama` core. It converts
already-decided `HostCaps` into bounded socket host functions and re-checks
endpoint allowlists, ABAC, information flow, approvals, TLS identity, byte
budgets, and connection budgets at the native I/O boundary.

Dependency direction is intentionally one-way:

```text
provider-transport -> kototama (tender ABI)
provider-transport -> security (shared policy)
```

Run `clojure -M:test`.

