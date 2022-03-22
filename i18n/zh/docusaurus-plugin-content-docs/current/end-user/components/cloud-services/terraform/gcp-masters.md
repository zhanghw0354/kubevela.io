---
title:  Gcp-Masters
---

## 描述

Create DC/OS Master instance and have conditional DC/OS Prereqs for GCP

## 参数说明


### 属性

 名称 | 描述 | 类型 | 是否必须 | 默认值 
 ------------ | ------------- | ------------- | ------------- | ------------- 
 cluster_name | Name of the DC/OS cluster |  | true |  
 disk_size | Disk Size in GB |  | true |  
 master_subnetwork_name | Master Subnetwork Name |  | true |  
 public_ssh_key | SSH Public Key |  | true |  
 dcos_instance_os | Operating system to use. Instead of using your own AMI you could use a provided OS. |  | false |  
 image | Source image to boot from |  | true |  
 hostname_format | Format the hostname inputs are index+1, region, cluster_name |  | false |  
 labels | Add custom labels to all resources | map | false |  
 disk_type | Disk Type to Leverage The GCE disk type. Can be either 'pd-ssd', 'local-ssd', or 'pd-standard'. (optional) |  | true |  
 user_data | User data to be used on these instances (cloud-init) |  | false |  
 tags | Add custom tags to all resources | list | false |  
 num_masters | Specify the amount of masters. For redundancy you should have at least 3 |  | true |  
 machine_type | Instance Type |  | true |  
 zone_list | Element by zone list | list | false |  
 ssh_user | SSH User |  | true |  
 writeConnectionSecretToRef | The secret which the cloud resource connection will be written to | [writeConnectionSecretToRef](#writeConnectionSecretToRef) | false |  


#### writeConnectionSecretToRef

 名称 | 描述 | 类型 | 是否必须 | 默认值 
 ------------ | ------------- | ------------- | ------------- | ------------- 
 name | The secret name which the cloud resource connection will be written to | string | true |  
 namespace | The secret namespace which the cloud resource connection will be written to | string | false |  