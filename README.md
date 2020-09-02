# Gherkin

![Gherkin](/images/gherkin.png)

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
