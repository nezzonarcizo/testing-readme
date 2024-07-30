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
| [spotinst_ocean_aws_launch_spec.this](https://registry.terraform.io/providers/spotinst/spotinst/1.181.0/docs/resources/ocean_aws_launch_spec) | resource |
| [aws_eks_cluster.cluster](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/eks_cluster) | data source |
| [aws_eks_cluster_auth.cluster](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/eks_cluster_auth) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_account"></a> [account](#input\_account) | The Spotinst Ocean account | `string` | n/a | yes |
| <a name="input_autoscale_is_enabled"></a> [autoscale\_is\_enabled](#input\_autoscale\_is\_enabled) | Whether to enable autoscaling for the Ocean cluster | `bool` | n/a | yes |
| <a name="input_cluster_name"></a> [cluster\_name](#input\_cluster\_name) | The name of the EKS cluster | `string` | n/a | yes |
| <a name="input_iam_instance_profile"></a> [iam\_instance\_profile](#input\_iam\_instance\_profile) | The name of the IAM role to associate with the Ocean cluster | `string` | n/a | yes |
| <a name="input_nodegroups"></a> [nodegroups](#input\_nodegroups) | List of nodegroups to create | <pre>list(object({<br>    name                   = string<br>    nodegroup_sgs          = list(string)<br>    nodegroup_subnets_ids  = list(string)<br>    user_data              = string<br>    iam_instance_profile   = string<br>    image_id               = string<br>    instance_types         = list(string)<br>    preferred_spot_types   = list(string)<br>    whitelist              = list(string)<br>    max_instance_count     = number<br>    min_instance_count     = number<br>    labels                 = list(object({<br>      key   = string<br>      value = string<br>    }))<br>    taints                 = list(object({<br>      key    = string<br>      value  = string<br>      effect = string<br>    }))<br>    tags                   = list(object({<br>      key   = string<br>      value = string<br>    }))<br>    spot_percentage        = number<br>  }))</pre> | n/a | yes |
| <a name="input_region"></a> [region](#input\_region) | The region in which to create the EKS cluster | `string` | n/a | yes |
| <a name="input_security_groups"></a> [security\_groups](#input\_security\_groups) | The security groups to associate with the Ocean cluster | `list(string)` | n/a | yes |
| <a name="input_subnet_ids"></a> [subnet\_ids](#input\_subnet\_ids) | The subnet IDs in which to create the Ocean cluster | `list(string)` | n/a | yes |
| <a name="input_token"></a> [token](#input\_token) | The Spotinst Ocean token | `string` | n/a | yes |
| <a name="input_use_as_template_only"></a> [use\_as\_template\_only](#input\_use\_as\_template\_only) | launch specification defined on the Ocean object will function only as a template for virtual node groups | `bool` | n/a | yes |

## Outputs

No outputs.
<!-- END_TF_DOCS -->
