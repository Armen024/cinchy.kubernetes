# Reference Document
https://github.com/nabsul/k8s-ecr-login-renew

Update secrets.yaml with AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY and AWS_REGION.

# Environment Variables
The tool is mainly configured through environment variables. These are:

AWS_ACCESS_KEY_ID (required): AWS access key used to create the Docker credentials.
AWS_SECRET_ACCESS_KEY (required): AWS secret needed to fetch Docker credentials from AWS.
AWS_REGION (required): The AWS region where your ECR instance is created.
DOCKER_SECRET_NAME (required): The name of the Kubernetes secret where the Docker credentials are stored.
TARGET_NAMESPACE (optional): Comma, semicolon or newline separated list of namespaces. A Docker secret is created in each of these. If this environment variable is not set, a value of default is assumed.
DOCKER_REGISTRIES (optional): Comma-separated list of registry URL. If none is provided, the default URL returned from AWS is used.
Example: DOCKER_REGISTRIES=https://321321.dkr.ecr.us-west-2.amazonaws.com,https://123123.dkr.ecr.us-east-2.amazonaws.com