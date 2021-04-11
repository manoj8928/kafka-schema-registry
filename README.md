# Schema Registry Helm Chart
Confluent Schema Registry provides a serving layer for your metadata. It provides a RESTful interface for storing and retrieving Apache Avro schemas. It stores a versioned history of all schemas based on a specified subject name strategy, provides multiple compatibility settings and allows evolution of schemas according to the configured compatibility settings and expanded Avro support.

This chart bootstraps a deployment of a Confluent Schema Registry.

## Prerequisites
* Kubernetes 1.10.0+
* A healthy and accessible AWS MKS Cluster

## Docker Image Source
* [DockerHub -> ConfluentInc](https://hub.docker.com/r/confluentinc/cp-schema-registry)

## Helm Chart Components
This chart will do the following:

* Create a schema registry cluster using a [Deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/).
* Create a Service configured to connect to the available schema registry instance on the configured port.
* Optionally add an [Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/) resource.
* Optionally start a JMX Exporter container inside schema registry pods.