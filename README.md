# Terraform for Genesys Cloud

A curated collection of documentation, examples, and reference configurations for the official Genesys Cloud Terraform Provider.

This repository is designed for administrators, consultants, architects, and engineers who want practical examples of managing Genesys Cloud with Terraform without having to navigate the full provider source code repository.

## Why This Repository Exists

The official Genesys Cloud Terraform Provider repository contains:

- Provider source code
- Unit and integration tests
- Build and release tooling
- Development documentation
- Terraform examples

While that repository is the authoritative source for the provider, many users simply want to find working examples and documentation.

This repository provides a simplified experience focused on learning and implementing Terraform within Genesys Cloud environments.

## What You'll Find Here

### Documentation

The `docs/` directory contains provider documentation, including:

- Resource documentation
- Data source documentation
- Provider documentation
- Usage reference material

### Example Configurations

The `examples/` directory contains practical Terraform examples organized by category:

#### examples/common/

Reusable Terraform patterns and shared configuration examples.

#### examples/data-sources/

Examples demonstrating how to retrieve and reference existing Genesys Cloud configuration using Terraform data sources.

#### examples/provider/

Examples showing provider setup and authentication configuration.

#### examples/resources/

Examples demonstrating how to create, update, and manage Genesys Cloud resources using Terraform.

## Repository Structure

```text
docs/

examples/
├── common/
├── data-sources/
├── provider/
└── resources/
```

## Synchronization with the Official Provider

This repository is automatically synchronized with selected content from the official Genesys Cloud Terraform Provider repository:

https://github.com/MyPureCloud/terraform-provider-genesyscloud

The following content is synchronized:

```text
docs/*
examples/common/*
examples/data-sources/*
examples/provider/*
examples/resources/*
```

This approach keeps the repository lightweight and focused while ensuring examples and documentation remain aligned with the official provider project.

## Getting Started

### Prerequisites

- Terraform installed
- A Genesys Cloud organization
- A Genesys Cloud OAuth client with appropriate permissions

### Configure the Provider

Example provider configuration:

```terraform
terraform {
  required_providers {
    genesyscloud = {
      source  = "mypurecloud/genesyscloud"
      version = "~> 1.0"
    }
  }
}

provider "genesyscloud" {
  oauthclient_id     = var.client_id
  oauthclient_secret = var.client_secret
  aws_region         = "ap-southeast-2"
}
```

### Deploy Configuration

Initialize Terraform:

```bash
terraform init
```

Review planned changes:

```bash
terraform plan
```

Apply the configuration:

```bash
terraform apply
```

## Intended Audience

This repository is useful for:

- Genesys Cloud Administrators
- Technical Consultants
- Solution Architects
- DevOps Engineers
- Platform Engineers
- Cloud Engineers
- Terraform Practitioners
- Anyone learning Infrastructure as Code for Genesys Cloud

## Contributing

If you discover issues with examples, documentation, or repository structure, feel free to submit an issue or pull request.

## Official Provider Repository

For provider releases, development, issue tracking, and source code, visit:

https://github.com/MyPureCloud/terraform-provider-genesyscloud

## Disclaimer

This is an independent community repository intended to make Genesys Cloud Terraform documentation and examples easier to access and consume.

Official provider development, releases, support, and source code remain the responsibility of the Genesys Cloud Terraform Provider project.

## License

Please refer to the licenses contained within this repository and the upstream provider repository.