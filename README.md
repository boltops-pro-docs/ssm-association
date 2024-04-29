<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-pro/ssm-association/blob/master/README.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

# Blueprint: ssm-association

## Usage

1. Configure: configs/ssm-association values
2. Deploy

## Configure

First you want to configure the `configs/ssm-association` [config files](https://lono.cloud/docs/core/configs/).  You can use [lono seed](https://lono.cloud/reference/lono-seed/) to configure starter values quickly.

    LONO_ENV=development lono seed ssm-association

For additional environments:

    LONO_ENV=production  lono seed ssm-association

The generated files in `config/ssm-association` folder look something like this:

    configs/ssm-association/
    ├── params
    │   ├── development.txt
    │   └── production.txt
    └── variables
        ├── development.rb
        └── production.rb

## Deploy

Use the [lono cfn deploy](https://lono.cloud/reference/lono-cfn-deploy/) command to deploy. Example:

    LONO_ENV=development lono cfn deploy ssm-association-development --blueprint ssm-association --sure
    LONO_ENV=production  lono cfn deploy ssm-association-production  --blueprint ssm-association --sure
