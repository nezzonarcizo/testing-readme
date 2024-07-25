<!-- BEGIN_TF_DOCS -->
== Requirements

[cols="a,a",options="header,autowidth"]
|===
|Name |Version
|[[requirement_spotinst]] <<requirement_spotinst,spotinst>> |1.181.0
|===

== Providers

[cols="a,a",options="header,autowidth"]
|===
|Name |Version
|[[provider_aws]] <<provider_aws,aws>> |n/a
|[[provider_spotinst]] <<provider_spotinst,spotinst>> |1.181.0
|===

== Modules

[cols="a,a,a",options="header,autowidth"]
|===
|Name |Source |Version
|[[module_ocean-aws-k8s]] <<module_ocean-aws-k8s,ocean-aws-k8s>> |spotinst/ocean-aws-k8s/spotinst |1.4.0
|[[module_ocean-controller]] <<module_ocean-controller,ocean-controller>> |spotinst/ocean-controller/spotinst |0.54.0
|===

== Resources

[cols="a,a",options="header,autowidth"]
|===
|Name |Type
|https://registry.terraform.io/providers/spotinst/spotinst/1.181.0/docs/resources/ocean_aws_launch_spec[spotinst_ocean_aws_launch_spec.dev-apps-az] |resource
|https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/eks_cluster[aws_eks_cluster.cluster] |data source
|https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/eks_cluster_auth[aws_eks_cluster_auth.cluster] |data source
|===

== Inputs

[cols="a,a,a,a,a",options="header,autowidth"]
|===
|Name |Description |Type |Default |Required
|[[input_account]] <<input_account,account>>
|The Spotinst Ocean account
|`string`
|n/a
|yes

|[[input_autoscale_is_enabled]] <<input_autoscale_is_enabled,autoscale_is_enabled>>
|Whether to enable autoscaling for the Ocean cluster
|`bool`
|n/a
|yes

|[[input_cluster_name]] <<input_cluster_name,cluster_name>>
|The name of the EKS cluster
|`string`
|n/a
|yes

|[[input_desired_capacity]] <<input_desired_capacity,desired_capacity>>
|The desired capacity of the Ocean cluster
|`number`
|n/a
|yes

|[[input_dev_apps_sgs]] <<input_dev_apps_sgs,dev_apps_sgs>>
|The security groups to associate with the Ocean Nodegroups
|`list(string)`
|n/a
|yes

|[[input_dev_apps_subnets_ids]] <<input_dev_apps_subnets_ids,dev_apps_subnets_ids>>
|The subnet IDs in which to create VNGs
|`list(string)`
|n/a
|yes

|[[input_image_id]] <<input_image_id,image_id>>
|The AMI ID to use for the Ocean cluster
|`string`
|n/a
|yes

|[[input_labels]] <<input_labels,labels>>
|List of labels to apply
|

[source]
----
list(object({
    key   = string
    value = string
  }))
----

|`[]`
|no

|[[input_max_size]] <<input_max_size,max_size>>
|The maximum size of the Ocean cluster
|`number`
|n/a
|yes

|[[input_min_size]] <<input_min_size,min_size>>
|The minimum size of the Ocean cluster
|`number`
|n/a
|yes

|[[input_region]] <<input_region,region>>
|The region in which to create the EKS cluster
|`string`
|n/a
|yes

|[[input_security_groups]] <<input_security_groups,security_groups>>
|The security groups to associate with the Ocean cluster
|`list(string)`
|n/a
|yes

|[[input_spot_percentage_az]] <<input_spot_percentage_az,spot_percentage_az>>
|Percentage of Spot AZ nodegroup
|`string`
|n/a
|yes

|[[input_subnet_ids]] <<input_subnet_ids,subnet_ids>>
|The subnet IDs in which to create the Ocean cluster
|`list(string)`
|n/a
|yes

|[[input_tags]] <<input_tags,tags>>
|List of labels to apply
|

[source]
----
list(object({
    key   = string
    value = string
  }))
----

|`[]`
|no

|[[input_taints]] <<input_taints,taints>>
|taints / toleration
|

[source]
----
list(object({
    key    = string
    value  = string
    effect = string
  }))
----

|`null`
|no

|[[input_token]] <<input_token,token>>
|The Spotinst Ocean token
|`string`
|n/a
|yes

|[[input_use_as_template_only]] <<input_use_as_template_only,use_as_template_only>>
|launch specification defined on the Ocean object will function only as a template for virtual node groups
|`bool`
|n/a
|yes

|[[input_user_data]] <<input_user_data,user_data>>
|The user data to use for the Ocean cluster
|`string`
|n/a
|yes

|[[input_vng_name_dev_apps]] <<input_vng_name_dev_apps,vng_name_dev_apps>>
|The name of the Ocean VNG
|`string`
|n/a
|yes

|[[input_whitelist]] <<input_whitelist,whitelist>>
|The instance types to whitelist for the Ocean cluster
|`list(string)`
|n/a
|yes

|[[input_worker_instance_profile_arn]] <<input_worker_instance_profile_arn,worker_instance_profile_arn>>
|The name of the IAM role to associate with the Ocean cluster
|`string`
|n/a
|yes

|===

== Outputs

No outputs.
<!-- END_TF_DOCS -->
