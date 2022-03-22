---
title:  Gcp-Bastion
---

## 描述

Bastion for GCP

## 参数说明


### 属性

 名称 | 描述 | 类型 | 是否必须 | 默认值 
 ------------ | ------------- | ------------- | ------------- | ------------- 
 name | The name of the Bastion Instance | string | false |  
 network_interface |  | map(any) | true |  
 image | Describes the base image used | map(any) | true |  
 firewall | Flag to control the creation or not of a firewall rule. Maybe not needed if you use a pre-prepared or shared set-up | number | false |  
 location |  |  | false |  
 source_cidrs | The ranges to allow to connect to the bastion | list(any) | true |  
 service_scope |  | list(any) | false |  
 nat_ip | Values set if using a Static IP |  | false |  
 keyring |  | string | false |  
 machine_type | The machine type for the Bastion | string | false |  
 tags | Hard-coded tags that associates the correct firewall to the instance | list(any) | false |  
 kms_key_name |  | string | false |  
 account_id |  |  | true |  
 project | The GCP project | string | true |  
 zone | The GCP zone | string | true |  
 service_email | Service account username | string | true |  
 writeConnectionSecretToRef | The secret which the cloud resource connection will be written to | [writeConnectionSecretToRef](#writeConnectionSecretToRef) | false |  


#### writeConnectionSecretToRef

 名称 | 描述 | 类型 | 是否必须 | 默认值 
 ------------ | ------------- | ------------- | ------------- | ------------- 
 name | The secret name which the cloud resource connection will be written to | string | true |  
 namespace | The secret namespace which the cloud resource connection will be written to | string | false |  