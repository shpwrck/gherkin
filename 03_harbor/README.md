# Harbor Registry

In order to secure the harbor deployment, a default ingress controller is required.

This repo has been tested against the nginx ingress controller.

## Adding the Nginx Catalog

* Name: "nginx"
* Catalog URL: "https://github.com/kubernetes/ingress-nginx"
* Branch: "master"
* Scope: "global"
* Helm Version: "Helm v3"

## Extra Answers

The Nginx Ingress Controller does not require any additional configuration.

## Issuer

This step assumes that certmanager is already installed using gitlab.

In order to deploy secrets for the harbor ingress, apply the harbor-issuer.yaml file found in this directory prior to Harbor.

## Adding the Harbor Catalog

* Name: "nginx"
* Catalog URL: "https://github.com/goharbor/harbor-helm"
* Branch: "1.4.0"
* Scope: "global"
* Helm Version: "Helm v3"

## Extra Answers

Can be found in values.yaml
