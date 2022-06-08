# GitOps-Demo
Demo for Openshift GitOps

# Install the OpenShift GitOps Operator
```
$ echo 'apiVersion: operators.coreos.com/v1alpha1
kind: Subscription
metadata:
  name: openshift-gitops-operator
  namespace: openshift-operators
spec:
  channel: latest
  name: openshift-gitops-operator
  source: redhat-operators
  sourceNamespace: openshift-marketplace' |oc create -f -

```
# Create the ArgoCD application
```
$ oc create -f argocd/applications/OpenShift-ServiceMesh/operator.yaml

```