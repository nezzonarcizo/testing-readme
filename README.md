<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_spotinst"></a> [spotinst](#requirement\_spotinst) | 1.181.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | n/a |
| <a name="provider_spotinst"></a> [spotinst](#provider\_spotinst) | 1.181.0 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_ocean-aws-k8s"></a> [ocean-aws-k8s](#module\_ocean-aws-k8s) | spotinst/ocean-aws-k8s/spotinst | 1.4.0 |
| <a name="module_ocean-controller"></a> [ocean-controller](#module\_ocean-controller) | spotinst/ocean-controller/spotinst | 0.54.0 |

## Resources

| Name | Type |
|------|------|
| [spotinst_ocean_aws_launch_spec.dev-apps-az](https://registry.terraform.io/providers/spotinst/spotinst/1.181.0/docs/resources/ocean_aws_launch_spec) | resource |
| [aws_eks_cluster.cluster](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/eks_cluster) | data source |
| [aws_eks_cluster_auth.cluster](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/eks_cluster_auth) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_account"></a> [account](#input\_account) | The Spotinst Ocean account | `string` | n/a | yes |
| <a name="input_autoscale_is_enabled"></a> [autoscale\_is\_enabled](#input\_autoscale\_is\_enabled) | Whether to enable autoscaling for the Ocean cluster | `bool` | n/a | yes |
| <a name="input_cluster_name"></a> [cluster\_name](#input\_cluster\_name) | The name of the EKS cluster | `string` | n/a | yes |
| <a name="input_desired_capacity"></a> [desired\_capacity](#input\_desired\_capacity) | The desired capacity of the Ocean cluster | `number` | n/a | yes |
| <a name="input_dev_apps_sgs"></a> [dev\_apps\_sgs](#input\_dev\_apps\_sgs) | The security groups to associate with the Ocean Nodegroups | `list(string)` | n/a | yes |
| <a name="input_dev_apps_subnets_ids"></a> [dev\_apps\_subnets\_ids](#input\_dev\_apps\_subnets\_ids) | The subnet IDs in which to create VNGs | `list(string)` | n/a | yes |
| <a name="input_image_id"></a> [image\_id](#input\_image\_id) | The AMI ID to use for the Ocean cluster | `string` | n/a | yes |
| <a name="input_labels"></a> [labels](#input\_labels) | List of labels to apply | <pre>list(object({<br>    key   = string<br>    value = string<br>  }))</pre> | `[]` | no |
| <a name="input_max_size"></a> [max\_size](#input\_max\_size) | The maximum size of the Ocean cluster | `number` | n/a | yes |
| <a name="input_min_size"></a> [min\_size](#input\_min\_size) | The minimum size of the Ocean cluster | `number` | n/a | yes |
| <a name="input_region"></a> [region](#input\_region) | The region in which to create the EKS cluster | `string` | n/a | yes |
| <a name="input_security_groups"></a> [security\_groups](#input\_security\_groups) | The security groups to associate with the Ocean cluster | `list(string)` | n/a | yes |
| <a name="input_spot_percentage_az"></a> [spot\_percentage\_az](#input\_spot\_percentage\_az) | Percentage of Spot AZ nodegroup | `string` | n/a | yes |
| <a name="input_subnet_ids"></a> [subnet\_ids](#input\_subnet\_ids) | The subnet IDs in which to create the Ocean cluster | `list(string)` | n/a | yes |
| <a name="input_tags"></a> [tags](#input\_tags) | List of labels to apply | <pre>list(object({<br>    key   = string<br>    value = string<br>  }))</pre> | `[]` | no |
| <a name="input_taints"></a> [taints](#input\_taints) | taints / toleration | <pre>list(object({<br>    key    = string<br>    value  = string<br>    effect = string<br>  }))</pre> | `null` | no |
| <a name="input_token"></a> [token](#input\_token) | The Spotinst Ocean token | `string` | n/a | yes |
| <a name="input_use_as_template_only"></a> [use\_as\_template\_only](#input\_use\_as\_template\_only) | launch specification defined on the Ocean object will function only as a template for virtual node groups | `bool` | n/a | yes |
| <a name="input_user_data"></a> [user\_data](#input\_user\_data) | The user data to use for the Ocean cluster | `string` | n/a | yes |
| <a name="input_vng_name_dev_apps"></a> [vng\_name\_dev\_apps](#input\_vng\_name\_dev\_apps) | The name of the Ocean VNG | `string` | n/a | yes |
| <a name="input_whitelist"></a> [whitelist](#input\_whitelist) | The instance types to whitelist for the Ocean cluster | `list(string)` | n/a | yes |
| <a name="input_worker_instance_profile_arn"></a> [worker\_instance\_profile\_arn](#input\_worker\_instance\_profile\_arn) | The name of the IAM role to associate with the Ocean cluster | `string` | n/a | yes |

## Outputs

No outputs.
<!-- END_TF_DOCS -->
