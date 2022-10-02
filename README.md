# composite-Action

## Sample workflow that uses custom action

```yaml

# File: .github/workflows/workflow.yml

on: [push]

name: DeployToEks

jobs:

  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
    
    - uses: DaniaErnest/composite-Action@v3
      CLUSTER_NAME: Eks_cluster
           RELEASE_TAG: v2
           REGION:  us-east-2
           ENVIRONMENT: Eks_cluster
           AWS_ACCESS_KEY_ID: '${{ secrets.AWS_ACCESS_KEY_ID}}'
           AWS_SECRET_ACCESS_KEY: '${{ secrets.AWS_SECRET_ACCESS_KEY }}'
           SLACK_BOT_TOKEN: '${{ secrets.SLACK_BOT_TOKEN }}'

```
