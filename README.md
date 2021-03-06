# tfsate

This repository is responsible for creating and configuring the GCS bucket for managing Terraform state.

## Prerequisites

- Terraform ([Install Guide](https://www.terraform.io/downloads.html))

## Deployment Instructions

This GCS bucket needs to be deployed manually from a local machine.
Before running the below commands make sure you have added the path to your `credentials.json` file. See `terraform/providers.tf`.

```bash
# Change in to the terrform directory
cd terraform

# Initial Terraform
terraform init

# Initial Terraform templates
terraform validate

# Run Terraform plan to verify changes before applying
GOOGLE_CREDENTIALS=/path/to/gcloud/credentials.json terraform plan

# Apply Terraform templates
GOOGLE_CREDENTIALS=/path/to/gcloud/credentials.json terraform apply -auto-approve
```

## License

This package is distributed under the terms of the [MIT](LICENSE) License.
