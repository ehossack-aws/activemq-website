---
layout: default_md
title: JMS 2.0 Support 
title-class: page-title-activemq5
type: activemq5
---

[Connectivity](connectivity) > [JMS 2.0 Support](jms-20-support)


Work is ongoing to provide a full JMS 2.0 spec implementation in ActiveMQ 5.X

As always, the best way to stay updated with progress is to follow the main Jira: [AMQ-7309](https://issues.apache.org/jira/browse/AMQ-7309)

The approach is gradual:
1. Implement the JMS spec interfaces, while throwing [`UnsupportedOperationException`](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/UnsupportedOperationException.html) for actions that require further implementations
2. Add slowly in the remaining functionality as implemented

Here is an outline of the remaining work as of Sept. 2021:

| JMS Feature | Target Release | Jira | Notes
|-------|-------|-------|-------|
| `Message.deliveryDelay` | 5.18+ | [AMQ-8320](https://issues.apache.org/jira/browse/AMQ-8320) | 
| `Message getBody isBodyAssignable` | 5.18+ | [AMQ-8321](https://issues.apache.org/jira/browse/AMQ-8321) | 
| `Connection createContext` | 5.18+ | [AMQ-8322](https://issues.apache.org/jira/browse/AMQ-8322) | 
| `Session` topic consumer methods | 5.18+ | [AMQ-8323](https://issues.apache.org/jira/browse/AMQ-8323) | 
| `MessageProducer` send methods | 5.18+ | [AMQ-8324](https://issues.apache.org/jira/browse/AMQ-8324) | 
| `XAConnection createXAContext` methods | 5.18+ | [AMQ-8325](https://issues.apache.org/jira/browse/AMQ-8325) | 
| `pool-jms` fork | 5.18+ | [AMQ-8366](https://issues.apache.org/jira/browse/AMQ-8366) | 