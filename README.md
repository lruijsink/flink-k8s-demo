# Flink k8s demo

This is a tutorial project demonstrating the use of Apache Flink in a locally
running Kubernetes cluster; a sandbox environment with relevant examples. This
project's code is written in Kotlin and assumes general backend/JVM familiarity.

## Examples

- **Hello World**: A very simple job, the equivalent of "hello world" in Flink,
  demonstrating a simple running cluster

## Stack

- Maven
- JDK 17 (Java 21 is experimental in Flink 2.2.x)
- Apache Flink 2.2.x
  - Flink Kubernetes Operator 1.15.0
  - RocksDB
- Kotlin
- JUnit: unit tests
- kind: test Kubernetes cluster
- Helmfile: test cluster dependencies

## Integration

- Deployment:
  - Kubernetes `FlinkDeployment` CRD (Flink in application mode)
  - 1 JobManager with UI enabled
  - 2 TaskManagers
- State:
  - Backend: RocksDB
  - Checkpoints and savepoints: `PersistentVolumeClaim`
- Monitoring: Prometheus, logs, using https://github.com/lruijsink/monitoring
- CI/CD: GitHub actions (build + test)

## How to run

TODO
