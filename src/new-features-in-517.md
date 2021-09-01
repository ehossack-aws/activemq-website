---
layout: default_md
title: New Features in 5.17 
title-class: page-title-activemq5
type: activemq5
---

[Features](features) > [New Features](new-features) > [New Features in 5.17](new-features-in-517)


New Features in 5.17
----------------------

*   Superficial JMS 2.0 implementations [AMQ-7309](https://issues.apache.org/jira/browse/AMQ-7309)
    *    Only a high-level spec implementation is included. Most operations that rely on server-side implementation will throw an [`UnsupportedOperationException`](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/UnsupportedOperationException.html)
    *    To track JMS 2.0 implementation progress, visit [JMS 2.0 Support](./jms-20-support)

Removed Features in 5.17
----------------------

*   LevelDB was removed [AMQ-7502](https://issues.apache.org/jira/browse/AMQ-7502)

## Upgrading

While 5.17 has some significant changes, upgrading should not be a big task provided you are not using the deprecated LevelDB store.

## Configuration

### Additions

_none yet_

### Removals
      
| Config parameter | XML element/section | Jira | Notes
|-------|-------|-------|-------|
| `levelDB` | `<persistenceAdapter> <levelDB>` | [AMQ-7502](https://issues.apache.org/jira/browse/AMQ-7502) | Removed LevelDB persistence apdapter
| `passiveSlave` | `<broker>` | [AMQ-8316](https://issues.apache.org/jira/browse/AMQ-8316) | Unused field from deprecated LevelDB replication
| `waitForSlave` | `<broker>` | [AMQ-8316](https://issues.apache.org/jira/browse/AMQ-8316) | Unused field from deprecated LevelDB replication
| `waitForSlaveTimeout` | `<broker>` | [AMQ-8316](https://issues.apache.org/jira/browse/AMQ-8316) | Unused field from deprecated LevelDB replication

