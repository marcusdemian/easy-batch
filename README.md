# Easy Batch (Jakarta fork)

Jakarta EE 10 / JDK 21 fork of [Easy Batch](https://github.com/j-easy/easy-batch) **5.3.x**, republished as `com.billing.easybatch:*:5.3.0-jakarta` for the Amdocs Billing System batch framework.

Upstream is in maintenance mode (v7.x, `org.jeasy`); this fork keeps the 5.x pipeline API and migrates javax ? **jakarta** namespaces for WildFly 34 / billing-framework.

## Maven coordinates

| Field | Value |
|---|---|
| groupId | `com.billing.easybatch` |
| artifactId | `easybatch` (parent POM) |
| version | `5.3.0-jakarta` |
| packaging | `pom` |

Core dependency for billing:

```xml
<dependency>
    <groupId>com.billing.easybatch</groupId>
    <artifactId>easybatch-core</artifactId>
    <version>5.3.0-jakarta</version>
</dependency>
```

## Modules

| Module | Role |
|---|---|
| `easybatch-core` | Job engine, record/batch pipeline |
| `easybatch-flatfile` / `xml` / `json` | File format readers/writers |
| `easybatch-jdbc` / `jpa` / `jms` | Database and messaging I/O |
| `easybatch-validation` | Bean Validation record validator |
| `easybatch-extensions` | Optional integrations (Spring, Hibernate, ?) |
| `easybatch-tools` | Reporting utilities |
| `easybatch-tutorials` | Examples |
| `easybatch-archetype` | Maven archetype |
| `easybatch-test-common` | Shared test helpers |

## Build

```bash
mvn clean install
```

Requires **JDK 21**. Consumed by `billing-framework` via the parent POM property `easybatch.version`.

## License

MIT (see `LICENSE.txt`). Original project by Mahmoud Ben Hassine.
