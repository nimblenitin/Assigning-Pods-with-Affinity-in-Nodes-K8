# Assigning-Pods-with-Affinity-in-Nodes-K8
Node affinity is a set of rules used by the scheduler to determine where a pod can be placed.



Simple example to assign Pods to Nodes based on Node Affinity specified in YAML file-

Steps followed:

*As Root*
```
1. List the nodes in your cluster, along with their labels:
$ kubectl get nodes --show-labels

2. Chose one of your nodes, and add a label to it:
$ kubectl label nodes <Node Name> disktype=ssd
$ kubectl label nodes <Node Name> site=india

3. Apply the manifest to create a Pod that is scheduled onto your chosen node
$ kubectl apply -f Node_affinity.yaml

4. Verify that the pod is running on your chosen node:
$ kubectl get pods --output=wide

```
*As Root*
