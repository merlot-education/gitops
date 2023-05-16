# Argo CD GitOps Repository
This repository is the GitOps state reference repository for all environments managed by ArgoCD.
All custom charts are contained in the `charts` directory. All environemnts are defined inside the `environments` directory.

We use the [app-of-apps pattern](https://argo-cd.readthedocs.io/en/stable/operator-manual/cluster-bootstrapping/#app-of-apps-pattern) to configure full environments and track all necessary depedencies between services via Argo CD. 
This is possible with the [app-of-apps chart](https://github.com/merlot-education/gitops/tree/main/charts/app-of-apps). New environments can be defined inside the `global-configuration.yaml` and the environment specific configuration is done with `environments/{env}/configuration.yaml` respectively.
