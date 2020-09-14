# Gherkin

![Gitlab](/images/gitlab.svg)
![Harbor](/images/harbor.svg)
![Rancher](/images/rancher.svg)
![Buildpacks](/images/buildpacks.svg)
![Kaniko](/images/kaniko.svg)
![Kustomize](/images/kustomize.png)

## G - itlab, H - arbor, E - vents, R - ancher, K - ubernetes, I - mages, N - stuff

This repo will deploy Gitlab, Harbor, and a demo application in order to demonstrate a pipeline that reacts to repository changes by building and deploying images.

### Demonstrated Flow

* A generates an event by merging a fork.
* GitLab triggers an image build.
* GitLab pushes the newly built image to Harbor.
* Push operation reports successful
* Gitlab Redeploy's dependent kubernetes resources.

### Prerequisites

* Rancher
* DigitalOcean Account
* A Single Domain
* Terraform Knowledge

## Flow

```
build-stage:
- build
- lint
- code-coverage
- unit-test
- tag
- push

registry-stage:
- scan

deploy-staging:
- staging

integration-tests:
- test

deploy-production:
- production

```

## OSS References

- [kustomize](https://kubernetes-sigs.github.io/kustomize/guides/bespoke/)
Replaces Templates
- [buildpacks](https://buildpacks.io/docs/)
Replaces BuildConfigs
- [kaniko](https://github.com/GoogleContainerTools/kaniko)
