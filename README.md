# Deprecated

OTC implemented this feature

## Usage
This is a helm charts which can be deployed to create automatically manual rds backups on otc via a cronjob.

Please make sure that you specify the necessary OTC credentials. You also need to specify the rds specific values.
All these values are provided as env variables inside the container. Otherwise python-otc-extension does not know
from which rds the backup should be created. Use the values.yaml for that.

How to install:

```shell
    export CHART_NAME=automated-manual-rds-backup
    export CHART_REPO_NAME=automated-manual-rds-backup-chart
    helm repo add $CHART_REPO_NAME https://iits-consulting.github.io/$CHART_REPO_NAME/
    helm search repo $CHART_NAME
    helm install $CHART_NAME $CHART_REPO_NAME/$CHART_NAME
```
