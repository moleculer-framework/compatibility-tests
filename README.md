# compatibility-tests
Compatibility tests between Moleculer implementations (Node.js, Java, Go, Ruby)

## Feature Matrix

### Service
| Feature		                      | Node.js | Java | Go | Ruby |
| ----------------------------------- | --- | --- | --- | --- |
| Versioned service                   | ✔️ | ✔️ | ❔ | ❔ |
| Mixins							  | ✔️ | ❌ | ️❔ | ❔ |
| Setting							  | ✔️ | ✔️ | ❔ | ❔ |
| Metadata							  | ✔️ | ❌ | ❔ | ❔ |
| Dependencies						  | ✔️ | ✔️ | ❔ | ❔ |
| Lifecycle events  			      | ✔️ | ️️️✔️ | ❔ | ❔ |
| `$node` internal service            | ✔️ | ❌ | ❔ | ❔ |
| Class-based service				  | ✔️ | ✔️ | ✔️ | ✔️ |

### Action calls
| Feature		                      | Node.js | Java | Go | Ruby |
| ----------------------------------- | --- | --- | --- | --- |
| Local call                          | ✔️ | ✔️ | ✔️ | ✔️ |
| Remote call                         | ✔️ | ✔️ | ✔️ | ✔️ |
| Nested call                         | ✔️ | ✔️ | ❔️ | ❔ |
| Direct call                         | ✔️ | ✔️ | ❔️ | ❔ |
| Request metadata                    | ✔️ | ✔️ | ❔️ | ❔ |
| Response metadata                   | ✔️ | ✔️ | ❔️ | ❔ |
| Metadata merging                    | ✔️ | ✔️ | ❔️ | ❔ |
| Parameter validation                | ✔️ | ❌ | ❔ | ❔ |
| Stream in request                   | ✔️ | ✔️ | ❔ | ❔ |
| Stream in response                  | ✔️ | ✔️ | ❔ | ❔ |
| Action visibility                   | ✔️ | ❌ | ❔ | ❔ |
| Action hooks                        | ✔️ | ❌ | ❔ | ❔ |

### Events
| Feature		                      | Node.js | Java | Go | Ruby |
| ----------------------------------- | --- | --- | --- | --- |
| Balanced events                     | ✔️ | ✔️ | ❔ | ❔ |
| Broadcast events                    | ✔️ | ✔️ | ❔️ | ❔️ |
| BroadcastLocal events               | ✔️ | ✔️ | ❔️ | ❔ |
| Context-based events                | ✔️ | ️️❌️ | ❌️ | ❌ |
| Custom group definition             | ✔️ | ️️✔️ | ❔ | ❔ |
| **Internal events**                 |  ️ | ️️  |   |   |
| `$services.changed`                 | ✔️ | ️️❌️ | ❌️ | ❌ |
| `$node.*`                           | ✔️ | ️️❌️ | ❌️ | ❌ |
| `$broker.*`                         | ✔️ | ️️❌️ | ❌️ | ❌ |
| `$transporter.*`                    | ✔️ | ️️❌️ | ❌️ | ❌ |

### Fault-tolerance
| Feature		                        | Node.js | Java | Go | Ruby |
| ------------------------------------- | --- | --- | --- | --- |
| Circuit Breaker                       | ✔️ | ✔️ | ❔ | ❔ |
| Retry                                 | ✔️ | ❌️ | ❔ | ❔ |
| Timeout                               | ✔️ | ❌️ | ❔ | ❔ |
| Bulkhead                              | ✔️ | ❌️ | ❔ | ❔ |
| Fallback                              | ✔️ | ❌️ | ❔ | ❔ |

### Transporters
| Feature		                        | Node.js | Java | Go | Ruby |
| ------------------------------------- | --- | --- | --- | --- |
| NATS                                  | ✔️ | ✔️ | ✔️ | ✔️ |
| Redis                                 | ✔️ | ✔️ | ❌ | ❌ |
| MQTT                                  | ✔️ | ✔️ | ❌ | ❌ |
| AMQP (0.9)                            | ✔️ | ✔️ | ❌ | ❌ |
| AMQP (1.0)                            | ❌ | ❌ | ❌ | ❌ |
| Kafka                                 | ✔️ | ✔️ | ❌ | ❌ |
| NATS Streaming                        | ✔️ | ❌ | ❌ | ❌ |
| TCP                                   | ✔️ | ✔️ | ❌ | ❌ |
| Google PubSub                         | ❌ | ✔️ | ❌ | ❌ |
| JMS                                 	| ❌ | ✔️ | ❌ | ❌ |
| Custom                                | ✔️ | ✔️ | ❔ | ❔ |
| Disabled balancing                    | ✔️ | ❌ | ❌ | ❌ |

### Serializers
| Feature		                        | Node.js | Java | Go | Ruby |
| ------------------------------------- | --- | --- | --- | --- |
| JSON                                  | ✔️ | ✔️ | ✔️ | ✔️ |
| MsgPack/Notepack                      | ✔️ | ✔️ | ❔ | ❔ |
| Avro                                  | ✔️ | ❌ | ❔ | ❔ |
| Protocol Buffer                       | ✔️ | ❌ | ❔ | ❔ |
| Thrift                                | ✔️ | ❌ | ❔ | ❔ |
| CBOR                                	| ❌ | ✔️ | ❌ | ❌ |
| Amazon Ion                           	| ❌ | ✔️ | ❌ | ❌ |
| BSON                                	| ❌ | ✔️ | ❌ | ❌ |
| SMILE                                	| ❌ | ✔️ | ❌ | ❌ |
| Custom                                | ✔️ | ✔️ | ❔ | ❔ |

### Strategies
| Feature		                        | Node.js | Java | Go | Ruby |
| ------------------------------------- | --- | --- | --- | --- |
| Round-Robin                           | ✔️ | ✔️ | ✔️ | ️️✔️ |
| Random                                | ✔️ | ✔️ | ❔ | ❔ |
| CPU usage                             | ✔️ | ✔️ | ❌️ | ❌️ |
| Latency-based                         | ✔️ | ✔️ | ❌️ | ❌️ |
| Sharding                              | ✔️ | ❌ | ❌ | ❌ |
| Custom                                | ✔️ | ✔️ | ❔ | ❔ |

### Caching
| Feature		                        | Node.js | Java | Go | Ruby |
| ------------------------------------- | --- | --- | --- | --- |
| Caching support                       | ✔️ | ✔️ | ❌ | ❌ |
| Time-To-Live                          | ✔️ | ✔️ | ❌ | ❌ |
| Custom key generator                  | ✔️ | ✔️ | ❌ | ❌ |
| Manual caching                        | ✔️ | ✔️ | ❌ | ❌ |
| Cache locking                         | ✔️ | ✔️ | ❌ | ❌ |
| **Cachers**                           |  |  |  |  |
| - Memory                              | ✔️ | ✔️ | ❌ | ❌ |
| - Memory LRU                          | ✔️ | ❌ | ❌ | ❌ |
| - Redis                               | ✔️ | ✔️ | ❌ | ❌ |
| - JCache                              | ❌ | ✔️ | ❌ | ❌ |
| - Off-heap                            | ❌ | ✔️ | ❌ | ❌ |
| - Custom                              | ✔️ | ✔️ | ❌ | ❌ |

### Middlewares
| Feature		                        | Node.js | Java | Go | Ruby |
| ------------------------------------- | --- | --- | --- | --- |
| Middleware support                    | ✔️ | ✔️ | ❌ | ❌ |
| **Hooks**                             |  |  |  |  |
| - `localAction`                       | ✔️ | ✔️ | ❌ | ❌ |
| - `remoteAction`                      | ✔️ | ✔️ | ❌ | ❌ |
| - `localEvent`                        | ✔️ | ❌ | ❌ | ❌ |
| - `createService`                     | ✔️ | ❌ | ❌ | ❌ |
| - `destroyService`                    | ✔️ | ❌ | ❌ | ❌ |
| - `call`                              | ✔️ | ❌ | ❌ | ❌ |
| - `mcall`                             | ✔️ | ❌ | ❌ | ❌ |
| - `emit`                              | ✔️ | ❌ | ❌ | ❌ |
| - `broadcast`                         | ✔️ | ❌ | ❌ | ❌ |
| - `broadcastLocal`                    | ✔️ | ❌ | ❌ | ❌ |
| - `serviceCreated`                    | ✔️ | ❌ | ❌ | ❌ |
| - `serviceStarting`                   | ✔️ | ❌ | ❌ | ❌ |
| - `serviceStarted`                    | ✔️ | ❌ | ❌ | ❌ |
| - `serviceStopping`                   | ✔️ | ❌ | ❌ | ❌ |
| - `serviceStopped`                    | ✔️ | ❌ | ❌ | ❌ |
| - `registerLocalService`              | ✔️ | ❌ | ❌ | ❌ |
| - `serviceCreating`                   | ✔️ | ❌ | ❌ | ❌ |
| - `transitPublish`                    | ✔️ | ❌ | ❌ | ❌ |
| - `transitMessageHandler`             | ✔️ | ❌ | ❌ | ❌ |
| - `transporterSend`                   | ✔️ | ❌ | ❌ | ❌ |
| - `transporterReceive`                | ✔️ | ❌ | ❌ | ❌ |
| - `created`                           | ✔️ | ❌ | ❌ | ❌ |
| - `starting`                          | ✔️ | ❌ | ❌ | ❌ |
| - `started`                           | ✔️ | ❌ | ❌ | ❌ |
| - `stopping`                          | ✔️ | ❌ | ❌ | ❌ |
| - `stopped`                           | ✔️ | ❌ | ❌ | ❌ |

### Metrics
| Feature		                        | Node.js | Java | Go | Ruby |
| ------------------------------------- | --- | --- | --- | --- |
| Metrics support                       | ✔️ | ❌ | ❌ | ❌ |
| OS metrics                            | ✔️ | ❌ | ❌ | ❌ |
| Process metrics                       | ✔️ | ❌ | ❌ | ❌ |
| Moleculer metrics                     | ✔️ | ❌ | ❌ | ❌ |
| User-defined metrics                  | ✔️ | ❌ | ❌ | ❌ |
| **Metric types**                      |  |  |  |  |
| - Counter type                        | ✔️ | ❌ | ❌ | ❌ |
| - Gauge type                          | ✔️ | ❌ | ❌ | ❌ |
| - Info type                           | ✔️ | ❌ | ❌ | ❌ |
| - Histogram type                      | ✔️ | ❌ | ❌ | ❌ |
| -  - Quantiles                        | ✔️ | ❌ | ❌ | ❌ |
| -  - Buckets                          | ✔️ | ❌ | ❌ | ❌ |
| -  - Rates                            | ✔️ | ❌ | ❌ | ❌ |
| **Reporters**                         |  |  |  |  |
| - Console                             | ✔️ | ❌ | ❌ | ❌ |
| - CSV                                 | ✔️ | ❌ | ❌ | ❌ |
| - Event                               | ✔️ | ❌ | ❌ | ❌ |
| - Datadog                             | ✔️ | ❌ | ❌ | ❌ |
| - Prometheus                          | ✔️ | ❌ | ❌ | ❌ |
| - StatsD (UDP)                        | ✔️ | ❌ | ❌ | ❌ |
| - Custom reporter                     | ✔️ | ❌ | ❌ | ❌ |
| Multi reporters                       | ✔️ | ❌ | ❌ | ❌ |

### Tracing
| Feature		                        | Node.js | Java | Go | Ruby |
| ------------------------------------- | --- | --- | --- | --- |
| Tracing support                       | ✔️ | ❌ | ❌ | ❌ |
| Nested spans                          | ✔️ | ❌ | ❌ | ❌ |
| Action span                           | ✔️ | ❌ | ❌ | ❌ |
| Event span                            | ✔️ | ❌ | ❌ | ❌ |
| User-defined span                     | ✔️ | ❌ | ❌ | ❌ |
| **Exporters**                         |  |  |  |  |
| - Console                             | ✔️ | ❌ | ❌ | ❌ |
| - Datadog                             | ✔️ | ❌ | ❌ | ❌ |
| - Event                               | ✔️ | ❌ | ❌ | ❌ |
| - Jaeger                              | ✔️ | ❌ | ❌ | ❌ |
| - Zipkin                              | ✔️ | ❌ | ❌ | ❌ |
| - Custom exporter                     | ✔️ | ❌ | ❌ | ❌ |
| Multi exporters                       | ✔️ | ❌ | ❌ | ❌ |

### Errors
| Feature		                        | Node.js | Java | Go | Ruby |
| ------------------------------------- | --- | --- | --- | --- |
| `MoleculerError`                      | ✔️ | ️️✔️ | ❔ | ❔ |
| `MoleculerRetryableError`             | ✔️ | ❔ | ❔ | ❔ |
| `MoleculerServerError`                | ✔️ | ❔ | ❔ | ❔ |
| `MoleculerClientError`                | ✔️ | ❔ | ❔ | ❔ |

### Additional features
| Feature		                        | Node.js | Java | Go | Ruby |
| ------------------------------------- | --- | --- | --- | --- |
| Hot-reload                            | ✔️ | ❌ | ❔ | ❔ |
| Runner/Starter                        | ✔️ | ✔️ | ❔ | ❔ |
| API Gateway                           | ✔️ | ✔️ | ❔ | ❔ |
| DB access service                     | ✔️ | ✔️ | ❔ | ❔ |

