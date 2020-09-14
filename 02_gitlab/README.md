# GitLab

The material in this directory does not represent a full GitLab solution.

Only features relevant to the demonstration will be configured and leveraged.

This demonstration will replace the built in GitLab registry with harbor.

# Installing GitLab

The GitLab quickstart documentation [here](https://docs.gitlab.com/charts/#gitlab-helm-chart-quick-start-guide) will suffice for this demonstration.

The provisioning of Layer 4 Load Balancers can take some time. :)

Add the DNS A Record to your Domain ( e.g. gitlab.stateofk8s.com )

## Adding the GitLab Catalog

* Name: "GitLab"
* Catalog URL: "https://charts.gitlab.io"
* Branch: "master"
* Scope: "global"
* Helm Version: "Helm v3"

## Additional Answers

Can be found in the `values.yaml`

## Importing the demo application

[Instructions](https://docs.gitlab.com/ee/user/project/import/repo_by_url.html)
