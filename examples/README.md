# Flux Commands

## install flux (to /usr/local/bin/flux)
```
curl -s https://toolkit.fluxcd.io/install.sh | sudo bash
```

## enable completions in ~/.bash_profile
. <(flux completion bash)

## check flux prerequisites
```
flux check --pre
```

## GitHub credentials
export GITHUB_TOKEN=<your-token>
export GITHUB_USER=<your-username>

## flux bootstrap - this is where the flux spec files are configured
```
flux bootstrap github \
  --owner=$GITHUB_USER \
  --repository=fleet-infra \
  --branch=main \
  --path=minikube \
  --personal
```

## Create a 'source' GitRepository
```
flux create source git --help
```

## Create a HelmRelease
```
flux create helmrelease --help
```
