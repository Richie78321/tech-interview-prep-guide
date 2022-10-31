# Yearly System Design Interview Prep Guide

## Quick links

* Open source crash course for system design: https://github.com/donnemartin/system-design-primer

## 1. Recall the structure of a system design interview (~minutes)

System design interviews are less structured than technical interviews, but they take this general form:

1. **Listen to the problem**
   * *Clarify underspecified requirements* before you start thinking about a solution
2. **Talk through a solution**
   * You will very likely have a whiteboard to sketch out your proposed system

## 2. Review the key technologies and ideas (~hours)

Below is a list containing the key technologies and ideas that I've seen in system design interviews. It is loosely ordered by importance.

* Horizontal scaling with service replicas
  * Like Elastic Kubernetes Service (EKS)
  * Requires load balancing
  * The replicated service should be mostly stateless
* Services as containers on a cluster
  * Like Docker Images, typically used within Kubernetes Pods
* Database replication
  * Like a managed SQL from a cloud provider
* Message queues
  * Like GCP Pub/Sub
  * Asynchronous, allows services to submit requests without blocking
* Content delivery networks (CDNs)
  * Enables fast and efficient serving of static files
* Data indexing and searching
  * Like ElasticSearch

## Example Questions

```
Suppose we need to build a website for ordering hats. We expect this website to experience a sudden, large surge in traffic. Users need to be able to place an order for a hat and check the status of their order in the future.

Follow-ups:
If there is a finite stock of hats, how do we inform users of the number of hats left in stock?
How can we prepare the website for the expected surge in traffic?
How would this website handle shipping?
```

```
Suppose we need to build a service that performs ML inference. In addition, this service should record the inputs that produce low-confidence predictions. These low-confidence inputs need to be served to labelers, who can add human labels and request for the ML model to be retrained.

Follow-ups:
How can the retrained model be rolled out to the live service without any downtime?
```

