---
subcategory: "Organizations"
layout: "aws"
page_title: "AWS: aws_organizations_delegated_services"
description: |-
  Get a list the AWS services for which the specified account is a delegated administrator 
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: aws_organizations_delegated_services

Get a list the AWS services for which the specified account is a delegated administrator

## Example Usage

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { DataAwsOrganizationsDelegatedServices } from "./.gen/providers/aws/data-aws-organizations-delegated-services";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new DataAwsOrganizationsDelegatedServices(this, "example", {
      accountId: "AWS ACCOUNT ID",
    });
  }
}

```

## Argument Reference

This data source supports the following arguments:

* `accountId` - (Required) Account ID number of a delegated administrator account in the organization.

## Attribute Reference

This data source exports the following attributes in addition to the arguments above:

* `delegatedServices` - Services for which the account is a delegated administrator, which have the following attributes:
    * `delegationEnabledDate` - The date that the account became a delegated administrator for this service.
    * `servicePrincipal` - The name of an AWS service that can request an operation for the specified service.

<!-- cache-key: cdktf-0.20.8 input-0599570da59571241937f49872d9d51984422b63b02f6137ea51f2f37f3635c7 -->