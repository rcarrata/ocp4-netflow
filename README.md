# Openshift 4 Network Flow Collector

Network Flow collector in Openshift4

## Deploy the ElastiFlow in Openshift 4

* Deploy the ElastiFlow with kustomize:

```
oc apply -k elastiflow/overlay
```

* Assign privileged scc to the SA of elastiflow

```
oc adm policy add-scc-to-user privileged -z default -n elastiflow
```

IMPORTANT: this is NOT recommended for productive environment, neither other environments. It's just a PoC, so please DON'T do it in prod. Use the proper SAs with the proper rbac :)

## Credits

The dashboard and the elastiflow is a very nice job from Rob Cowart in their repo [Elastiflow](https://github.com/robcowart/elastiflow). Kudos Rob!
