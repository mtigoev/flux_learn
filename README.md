# flux_learn

## Install flux

```shell
curl -s https://fluxcd.io/install.sh | sudo bash
```

## Bootstrap a cluster

```shell
flux bootstrap github \
  --context=minikube \
  --owner=mtigoev \
  --repository=flux_learn \
  --branch=main \
  --path=clusters/dev \
  --personal
```

## Install Weave GitOps

```shell
 PASSWORD="supassw"
gitops create dashboard ww-gitops \
  --password=$PASSWORD \
  --export > ./clusters/dev/weave/weave-gitops-dashboard.yaml
```