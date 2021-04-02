# OPA-Gatekeeper-Demo
These are basic rego rules for demo.<br>
There are more useful rules from opa official: https://github.com/open-policy-agent/gatekeeper-library

## Requirements
+ install OPA-Gatekeeper for your Kubernetes Cluster.<br>
You can reference: https://open-policy-agent.github.io/gatekeeper/website/docs/install

## Rules
1. [denyallpod](constraints/denyallpod/denyall-rule.yaml): deny any pods creation
2. [image](constraints/image/image-rule.yaml): accept specific container registry when pod creation
3. [label](constraints/label/label-rule.yaml): accept specific label when namespace creation
4. [pod-security-context](constraints/pod-security-context/security-rule.yaml): deny root privileged container when pod creation

## Run
+ use `kubectl apply -f xxx-rule.yaml`
+ use `kubectl apply -f xxx-invalid.yaml` to test rules.