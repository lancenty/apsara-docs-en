Alibaba Cloud  
Terraform  
User Guide  
Document Version: 20241115

**Table of Contents**

- [1.Apsara Stack Terraform](#section-1)
    - [1.1. Terms](#section-1-1)
    - [1.2. Benefits](#section-1-2)
    - [1.3. Scenarios](#section-1-3)
    - [1.4. Supported services](#section-1-4)
- [2.Usage](#section-2)
    - [2.1. Initialize a runtime environment](#section-2-1)
    - [2.2. Initialize a working directory](#section-2-2)
        - [2.2.1. Use STS to call AlibabacloudStack Provider](#section-2-2-1)
    - [2.3. Use Terraform to destroy resources](#section-2-3)
    - [2.4. Create a VPC](#section-2-4)
    - [2.5. Create an ECS instance](#section-2-5)
    - [2.6. Create an SLB instance](#section-2-6)
    - [2.7. Create an OSS bucket](#section-2-7)
    - [2.8. Create an ApsaraDB RDS instance](#section-2-8)
    - [2.9. Create a RAM role](#section-2-9)
    - [2.10. Create a KMS key](#section-2-10)
    - [2.11. Create a Message Queue instance](#section-2-11)
    - [2.12. Create an ACK cluster](#section-2-12)
    - [2.13. Create Container Registry resources](#section-2-13)
    - [2.14. Create MaxCompute resources](#section-2-14)
    - [2.15. Create DataWorks resources](#section-2-15)
    - [2.16. Create API Gateway resources](#section-2-16)
    - [2.17. Create Message Queue for Apache Kafka resources](#section-2-17)
    - [2.18. Create AnalyticDB for MySQL resources](#section-2-18)
    - [2.19. Create an AnalyticDB for PostgreSQL instance](#section-2-19)
    - [2.20. Create a PolarDB-X V1.0 instance](#section-2-20)
    - [2.21. Create an EBS storage set](#section-2-21)
    - [2.22. Create Auto Scaling resources](#section-2-22)
    - [2.23. Create CloudMonitor resources](#section-2-23)
    - [2.24. Register a database instance and a user with DMS Enterprise](#section-2-24)
    - [2.25. Create a DNS domain name](#section-2-25)
    - [2.26. Create DTS resources](#section-2-26)
    - [2.27. Create a DBS backup schedule](#section-2-27)
    - [2.28. Create DataHub resources](#section-2-28)
    - [2.29. Create EDAS resources](#section-2-29)
    - [2.30. Create Express Connect resources](#section-2-30)
    - [2.31. Create an E-HPC job template](#section-2-31)
    - [2.32. Create an Elasticsearch cluster](#section-2-32)
    - [2.33. Create an ApsaraDB for HBase cluster](#section-2-33)
    - [2.34. Create a Simple Log Service project](#section-2-34)
    - [2.35. Create an ApsaraDB for MongoDB instance](#section-2-35)
    - [2.36. Create NAS resources](#section-2-36)
    - [2.37. Create OOS resources](#section-2-37)
    - [2.38. Create Quick BI resources](#section-2-38)
    - [2.39. Create ROS resources](#section-2-39)
    - [2.40. Create a KVStore for Redis instance](#section-2-40)
    - [2.41. Create Tablestore resources](#section-2-41)
    - [2.42. Create VPN Gateway resources](#section-2-42)
    - [2.43. Create an Apsara Stack disk](#section-2-43)

![](en-terraform-user-guide-v3.18.3-20241115.assets/86c55e7a7a046e9ec0e2cbf3d7db5558.png)

<a id="section-1"></a>

# 1.Apsara Stack Terraform

<a id="section-1-1"></a>

## 1.1. Terms

![](en-terraform-user-guide-v3.18.3-20241115.assets/4b53bce4e0056f751a6daed4fbf4b43d.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/15d7ed5185c9e8e768a6fa9e9e146ba3.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/3f040afa182b6e7c77ff7b5034ce42a2.webp)

<a id="section-1-2"></a>

## 1.2. Benefits

![](en-terraform-user-guide-v3.18.3-20241115.assets/e55fcbbe19334a58d689e330a3dc4383.webp)

<a id="section-1-3"></a>

## 1.3. Scenarios

<a id="section-1-4"></a>

## 1.4. Supported services

| Category | Hybrid cloud service | Resource |
| --- | --- | --- |
|  |  | • alibabacloudstack_instance: ECS instance<br>• alibabacloudstack_security_g roup: security group<br>• alibabacloudstack_security_g roup_rule: security group rule<br>• alibabacloudstack_disk: cloud disk<br>• alibabacloudstack_disk_attac hment: disk attachment to ECS instance<br>• alibabacloudstack_image: image creation |

![](en-terraform-user-guide-v3.18.3-20241115.assets/35b56b43e61f51e78ef5421d4fc0ec76.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/215ed0e641a36d601b2f5855dc9d463c.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/a34f08ebbc01b710f0ecfb6c20be0774.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/969e77c0baeeb75d2ae487be1007950f.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/af63a678b184cfd3e0eb33d36385b24d.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/2fd17cf6100a0bba45a44ddf38809c9d.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/c48f1e191b8084b7d26094d873027ba8.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/23043f179847f3f8851baf3549ac05a5.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/b1e18c9cfe5a3796e059bd74dd6a3aa1.webp)

<table>
  <tr>
    <td>Cloud management</td>
    <td>ASCM</td>
    <td>• alibabacloudstack_ascm_logo n_policy: access policy<br>• alibabacloudstack_ascm_org anization: organization<br>• alibabacloudstack_ascm_user: user<br>• alibabacloudstack_ascm_user _role_binding: role assignment to user<br>• alibabacloudstack_ascm_user group_user: user addition to user group<br>• alibabacloudstack_ascm_user _group: user group<br>• alibabacloudstack_ascm_user _group_resource_set_binding: resource set association with user group<br>• alibabacloudstack_ascm_user _group_role_binding: role assignment to user group<br>• alibabacloudstack_ascm_pas sword_policy: password policy for Apsara Uni-manager Management Console<br>• alibabacloudstack_ascm_quo ta: quota<br>• alibabacloudstack_ascm_reso urce_group: resource set<br>• alibabacloudstack_ascm_ram _policy: Resource Access Management (RAM) policy<br>• alibabacloudstack_ascm_ram _role: RAM role<br>• alibabacloudstack_ascm_ram _policy_for_role: RAM role policy<br>• alibabacloudstack_ascm_cust om_role: custom role</td>
  </tr>
  <tr>
    <td>Monitoring and O&amp;M</td>
    <td>CloudMonitor</td>
    <td>• alibabacloudstack_cms_alar m: threshold-triggered alert rule<br>• alibabacloudstack_cms_alar m_contact: alert contact<br>• alibabacloudstack_cms_alar m_contact_group: alert contact group<br>• alibabacloudstack_cms_site_monitor: site monitoring task</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/9da17a26fd7e07be61dd0377230edaa0.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/2416f21bda7f07be30e7c808fcc0d588.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/5b79e33be9adf7d6e337d65a6cb54ed4.webp)

<a id="section-2"></a>

# 2.Usage

<a id="section-2-1"></a>

## 2.1. Initialize a runtime environment

![](en-terraform-user-guide-v3.18.3-20241115.assets/0b9b167a3477c770d12d18127cb990d2.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/cc4d291f9246ec152b8cdb8d6ac1d313.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/9a74fb82628d8e072dbd080c1782248b.webp)

<a id="section-2-2"></a>

## 2.2. Initialize a working directory

![](en-terraform-user-guide-v3.18.3-20241115.assets/a2ccaf40becf1ecfe9ffc9cb7e7799ba.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/1ffd027468bc879ba83e56b65104f4c6.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of Apsara Stack API (ASAPI).</td>
    <td>1. Log on to the Apsara Infrastructure Management Console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column of asapi and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/649c1b8ad04a7ff2426edf6b8d9df54a.webp)

<table>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false.The value true indicates that insecure HTTPS certificates can be ignored.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/e0709f7d70b780a4912cb01495967d92.webp)

<a id="section-2-2-1"></a>

### 2.2.1. Use STS to call AlibabacloudStack Provider

![](en-terraform-user-guide-v3.18.3-20241115.assets/4a4acbfae1de9b9f92be616aacb6e245.webp)

<a id="section-2-3"></a>

## 2.3. Use Terraform to destroy resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/780e7913be183aeab1b533aa19d410a4.webp)

<a id="section-2-4"></a>

## 2.4. Create a VPC

![](en-terraform-user-guide-v3.18.3-20241115.assets/37f504cf4a732d87d9ba18a6e5d5c5c8.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| vpc_name | The name of the VPC. | The name must be 2 to 128 characters in length and can contain letters, digits, underscores (_), and hyphens (-). It must start with a letter and cannot start with http:// or https://. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/05b6dc97ac3c22f7627f8bd0dd6c0479.webp)

<table>
  <tr>
    <td>cidr_block</td>
    <td>The CIDR block of the VPC.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>. In the left-side navigation pane, click <strong>Virtual Private Clouds</strong>. On the Virtual Private Clouds page, obtain the CIDR block of the VPC.<br>2. You can define a new CIDR block for the VPC.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/324418f5074b56a154d9c0004a7682f5.webp)

<a id="section-2-5"></a>

## 2.5. Create an ECS instance

![](en-terraform-user-guide-v3.18.3-20241115.assets/dc0fc1f041c80066c5dca9844669fc21.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| vpc_name | The name of the VPC. | The name must be 2 to 128 characters in length and can contain letters, digits, underscores (_), and hyphens (-). It must start with a letter and cannot start with http:// or https://. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/051788d88c91d084556c1cb16ed58184.webp)

<table>
  <tr>
    <td>cidr_block</td>
    <td>The CIDR block of the VPC.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>. In the left-side navigation pane, click <strong>Virtual Private Clouds</strong>. On the Virtual Private Clouds page, obtain the CIDR block of the VPC.<br>2. You can define a new CIDR block for the VPC.</td>
  </tr>
</table>

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| vswitch_id | The ID of the vSwitch. | 1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>.<br>2. In the left-side navigation pane, click <strong>VSwitches</strong>.Obtain the vSwitch ID from the VSwitches page. |
| availability_zone | The zone ID of the ECS instance. | 1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Elastic</strong> Compute Service.<br>2. In the left-side navigation pane, choose Instances &amp; Images &gt; <strong>Instances</strong>. Click Create Instance and obtain the zone ID. |
| image_id | The image ID. | 1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Elastic</strong> Compute Service.<br>2. In the left-side navigation pane, choose Instances &amp; Images &gt; <strong>Images</strong>. On the Images page, obtain the image ID. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/79e43d9700298752c0c9c4fa10e60db6.webp)

<table>
  <tr>
    <td>instance_type</td>
    <td>The ECS instance type.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Elastic</strong> <strong>Compute Service</strong>.<br>2. In the left-side navigation pane, choose Instances &amp; Images &gt; <strong>Instances</strong>. On the Instances page, click Create Instance. On the Create Instance page, select an instance generation and obtain the instance type.</td>
  </tr>
  <tr>
    <td>system_disk_category</td>
    <td>The type of the system disk.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Elastic</strong> Compute Service.<br>2. In the left-side navigation pane, choose Instances &amp; Images &gt; <strong>Instances</strong>. On the Instances page, click Create Instance. On the Create Instance page, obtain the system disk type.</td>
  </tr>
  <tr>
    <td>security_groups</td>
    <td>The security groups.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Elastic</strong> Compute Service.<br>2. In the left-side navigation pane, choose Network &amp; Security &gt; <strong>Security Groups</strong>.On the Security Groups page, obtain the security group information.</td>
  </tr>
  <tr>
    <td>instance_name</td>
    <td>The name of the ECS instance.</td>
    <td>The name must be 2 to 110 characters in length and can contain letters, digits, periods (.), underscores (_), hyphens (-), and colons (:). It must start with a letter.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/dcaf013759d396511a26756507d53824.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/12dc02085b87536df3d6a00385c45334.webp)

<a id="section-2-6"></a>

## 2.6. Create an SLB instance

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| vpc_name | The name of the VPC. | The name must be 2 to 128 characters in length and can contain letters, digits, underscores (_), and hyphens (-). It must start with a letter and cannot start with http:// or https://. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/7146343a6065d1882bd0eee167c1b90d.webp)

<table>
  <tr>
    <td>cidr_block</td>
    <td>The CIDR block of the VPC.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>. In the left-side navigation pane, click <strong>Virtual Private Clouds</strong>. On the Virtual Private Clouds page, obtain the CIDR block of the VPC.<br>2. You can define a new CIDR block for the VPC.</td>
  </tr>
</table>

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| vpc_name | The name of the VPC. | The name must be 2 to 128 characters in length and can contain letters, digits, underscores (_), and hyphens (-). It must start with a letter and cannot start with http:// or https://. |
| cidr_block | The CIDR block of the VPC. | 1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>. In the left-side navigation pane, click <strong>Virtual Private Clouds</strong>. On the Virtual Private Clouds page, obtain the CIDR block of the VPC.<br>2. You can define a new CIDR block for the VPC. |

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| name | The name of the SLB instance. | The name must be 2 to 128 characters in length and can contain letters, digits, underscores (_), and hyphens (-). It must start with a letter and cannot start with http:// or https://. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/76e6b121ec6f30e0aa94d996d2d25993.webp)

<table>
  <tr>
    <td>vswitch_id</td>
    <td>The ID of the vSwitch.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>.<br>2. In the left-side navigation pane, click <strong>VSwitches</strong>.Obtain the vSwitch ID from the VSwitches page.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/822d80ec650d3189c4c26c2c2d7d2a61.webp)

<a id="section-2-7"></a>

## 2.7. Create an OSS bucket

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/e9356d6ce8da90be4d74e59a2952be3e.webp)

<table>
  <tr>
    <td>bucket</td>
    <td>The name of the bucket.</td>
    <td>The bucket name must be 3 to 63 characters in length and can contain lowercase letters, digits, and hyphens (-). The bucket name must start and end with a lowercase letter or a digit.</td>
  </tr>
  <tr>
    <td>acl</td>
    <td>The access control list (ACL) of the bucket.</td>
    <td>Valid values: private, public-read, and public-read-write.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/a4f61cbc9d7f6c20befbd967bf8e6db8.webp)

<a id="section-2-8"></a>

## 2.8. Create an ApsaraDB RDS instance

![](en-terraform-user-guide-v3.18.3-20241115.assets/c48b54b701d2f1412fe017b6d23d176c.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/974758b8fb3c657a653d9074555966c6.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of ASAPI.</td>
    <td>1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the <strong>Report</strong> column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/6222c0f01b452dd70ef2414882a2b972.webp)

<table>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>engine</td>
    <td>The database engine that the instance runs.</td>
    <td>Valid values: MySQL, SQLServer, PostgreSQL, and PPAS.</td>
  </tr>
  <tr>
    <td>engine_version</td>
    <td>The version of the database engine.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt;</strong> <strong>ApsaraDB RDS</strong>.<br>2. Click <strong>Create Instance</strong>, and obtain the database engine version from the Create Instance page.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/6e2f2150308a488a5a7820bba6cc1157.webp)

<table>
  <tr>
    <td>instance_type</td>
    <td>The instance type.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt;</strong> <strong>ApsaraDB RDS</strong>.<br>2. Click <strong>Create Instance</strong>, and obtain the instance type from the Create Instance page.</td>
  </tr>
  <tr>
    <td>instance_storage</td>
    <td>The storage capacity of the instance.</td>
    <td>Unit: GB. You can increase the storage capacity in increments of 5 GB. For information about the valid values, see the official Apsara Stack documentation at ApsaraDB for RDS Developer Guide.</td>
  </tr>
  <tr>
    <td>storage_type</td>
    <td>The storage type of the instance.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt;</strong> <strong>ApsaraDB RDS</strong>.<br>2. Click <strong>Create Instance</strong>, and obtain the storage type from the Create Instance page.</td>
  </tr>
  <tr>
    <td>instance_name</td>
    <td>The name of the instance.</td>
    <td>The name must be 2 to 64 characters in length and can contain letters, digits, underscores (_), hyphens (-), and colons (:). It must start with a letter and cannot start with http:// or https://.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/6eef08421d21e58235e800e2b1f84b53.webp)

<a id="section-2-9"></a>

## 2.9. Create a RAM role

![](en-terraform-user-guide-v3.18.3-20241115.assets/3378bbf4e5f27cb8e3644c2964e7694a.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/1b9fbcefe71ce7dfa49f6777f1de176f.webp)

<table>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/d0798c0fad733717ad0603bf12bf6dfa.webp)

<table>
  <tr>
    <td>role_name</td>
    <td>The name of the RAM role.</td>
    <td>The name can be up to 64 characters in length.</td>
  </tr>
  <tr>
    <td>description</td>
    <td>The description of the RAM role.</td>
    <td>Note that the description cannot contain spaces.</td>
  </tr>
  <tr>
    <td>organization_visibility</td>
    <td>The organization visibility.</td>
    <td>Valid values: organizationVisibility.organizati on, organizationVisibility.orgAndSu bOrgs, and organizationVisibility.global.</td>
  </tr>
</table>

<a id="section-2-10"></a>

## 2.10. Create a KMS key

![](en-terraform-user-guide-v3.18.3-20241115.assets/8de4d252dec51923adc79cb9ed05e406.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| pending_window_in_days | The number of days to wait before the key is deleted after resources are destroyed. | Valid values: 7 to 30. Default value: 30. |
| key_state | The status of the customer master key (CMK). | By default, the CMK is enabled. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/250df7eef2f792ec101975f08dfc33ca.webp)

<a id="section-2-11"></a>

## 2.11. Create a Message Queue instance

![](en-terraform-user-guide-v3.18.3-20241115.assets/d549a28472b83d2eb3f25216a22becb0.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/a4fc036b4a2f96a6b24c9c644cec813e.webp)

<table>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/57968b4892bce288572096100bd010b6.webp)

<table>
  <tr>
    <td>tps_receive_max</td>
    <td>The maximum transactions per second (TPS) for subscribing to messages from a topic within a specific period of time.</td>
    <td>Valid values: 500 to 3000.</td>
  </tr>
  <tr>
    <td>tps_send_max</td>
    <td>The maximum TPS for sending messages to a topic within a specific period of time.</td>
    <td>Valid values: 500 to 3000.</td>
  </tr>
  <tr>
    <td>topic_capacity</td>
    <td>The maximum number of topics.</td>
    <td>Valid values: 10 to 5000.</td>
  </tr>
  <tr>
    <td>cluster</td>
    <td>The name of the cluster.</td>
    <td>Specify a name for the cluster.</td>
  </tr>
  <tr>
    <td>independent_naming</td>
    <td>Specifies whether the instance has a namespace.</td>
    <td>Valid values: true and false.true: The instance has a separate namespace. Resource names must be unique within an instance but can be the same across different instances. false: The instance has no separate namespace.Resource names must be globally unique within and across all instances.</td>
  </tr>
  <tr>
    <td>name</td>
    <td>The name of the instance.</td>
    <td>The name must be unique within the same account in the same region. The name must be 3 to 64 characters in length and can contain letters, digits, hyphens (-), and underscores (_).</td>
  </tr>
  <tr>
    <td>remark</td>
    <td>The description of the instance.</td>
    <td>Specify a concise description for the instance. It must be 2 to 128 characters in length and can contain letters, digits, underscores (_), hyphens (-), and colons (:). It must start with a letter and cannot start with http:// or https://.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/c8b259a793b4fe6356b8af6bb517c904.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/0be1031f4760ae8cbfd7baf37f09c320.webp)

<a id="section-2-12"></a>

## 2.12. Create an ACK cluster

![](en-terraform-user-guide-v3.18.3-20241115.assets/cb56738e555b6c8ab3b208896ea16546.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/49395bf3f125e894e134d560d9834a84.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/cc25dc6fb6307f1d50765f955044db1d.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/fc13b5f3658a1dfc28d2dbd377b35a3c.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of ASAPI.</td>
    <td>1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/80a1698df471456ff52421f633b27f84.webp)

<table>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>vpc_name</td>
    <td>The name of the VPC.</td>
    <td>The name must be 2 to 128 characters in length and can contain letters, digits, periods (.), underscores (_), and hyphens (-). The name must start with a letter.</td>
  </tr>
  <tr>
    <td>cidr_block</td>
    <td>The CIDR block of the VPC.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Operation Console, choose Products &gt; Virtual Private <strong>Cloud</strong>. In the left-side navigation pane, click <strong>Virtual Private Clouds</strong>. On the Virtual Private Clouds page, obtain the CIDR block of the VPC.<br>2. You can define a new CIDR block for the VPC.</td>
  </tr>
  <tr>
    <td>vswitch_id</td>
    <td>The ID of the vSwitch.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>.<br>2. In the left-side navigation pane, click <strong>VSwitches</strong>.Obtain the vSwitch ID from the VSwitches page.</td>
  </tr>
  <tr>
    <td>name</td>
    <td>The name of the ACK cluster.</td>
    <td>The name must be 1 to 63 characters in length and can contain digits, letters, and hyphens (-).</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/96ebf3560aa771c23368e5b885e98c31.webp)

<table>
  <tr>
    <td>version</td>
    <td>The Kubernetes version.</td>
    <td>We recommend that you use the latest Kubernetes version. If you do not specify this parameter, the latest Kubernetes version is used.</td>
  </tr>
  <tr>
    <td>password</td>
    <td>The password that is used to log on to a cluster node over SSH.</td>
    <td>You must specify one of the <code>password, key_name, and</code><br><code>kms_encrypted_password</code> parameters.</td>
  </tr>
  <tr>
    <td>enable_ssh</td>
    <td>Specifies whether to enable SSH logon to a node.</td>
    <td>Default value: false.</td>
  </tr>
  <tr>
    <td>proxy_mode</td>
    <td>The proxy mode.</td>
    <td>Set the proxy mode for kube-proxy. Valid values: iptables and ipvs. Default value: ipvs.</td>
  </tr>
  <tr>
    <td>user_data</td>
    <td>The user data.</td>
    <td>Windows instances support batch and PowerShell scripts. If your script file is larger than 1 KB in size, we recommend that you upload the script file to an Object Storage Service (OSS) bucket and use the internal endpoint of the bucket to access the script file.</td>
  </tr>
  <tr>
    <td>is_enterprise_security_group</td>
    <td>Specifies whether to automatically create an advanced security group.</td>
    <td>You must set security_group_id or is_enterprise_security_group.</td>
  </tr>
  <tr>
    <td>pod_cidr</td>
    <td>The CIDR block of pods.</td>
    <td>You must set this parameter to a valid private CIDR block.Make sure that the specified CIDR block does not overlap with the VPC CIDR block or the CIDR block used by an existing Kubernetes cluster in the VPC.</td>
  </tr>
  <tr>
    <td>new_nat_gateway</td>
    <td>Specifies whether to create a Network Address Translation (NAT) gateway when the Kubernetes cluster is created.</td>
    <td>This parameter is optional.Default value: true. Not all Apsara Stack APIs are accessible over the internal network. Therefore, we recommend that you set this parameter to true.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/c3ff0ae7566067b709804d5ff1ff6ef1.webp)

<table>
  <tr>
    <td>service_cidr</td>
    <td>The service CIDR block.</td>
    <td>This parameter is optional.Make sure that the specified CIDR block does not overlap with the VPC CIDR block or the CIDR block used by an existing Kubernetes cluster in the VPC.You cannot modify the CIDR block after the cluster is created.</td>
  </tr>
  <tr>
    <td>node_cidr_mask</td>
    <td>The prefix length of the node CIDR block.</td>
    <td>This parameter determines the maximum number of pods that can run on a node. Valid values: 24 to 28. If you set this parameter to 24, each node can run a maximum of 255 pods. This number is calculated by using the following formula: Maximum number of pods on each node = 2 ^ (32 - 24) - 1.Default value: 24.</td>
  </tr>
  <tr>
    <td>slb_internet_enabled</td>
    <td>Specifies whether to create an Internet-facing Server Load Balancer (SLB) instance for the API server of the cluster.</td>
    <td>Default value: true.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/55f33bbcf3702facfaa2ee1376d923c4.webp)

<a id="section-2-13"></a>

## 2.13. Create Container Registry resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/8d16ab887ab94c58e2576671a51957bb.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/2e574cda3e8b891fae3ce9366ad4e5b6.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of ASAPI.</td>
    <td>1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/c8033e91b0cdeb09850df8a312c8cfca.webp)

<table>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>name</td>
    <td>The name of the namespace.</td>
    <td>The name must be 2 to 30 characters in length and can contain lowercase letters, digits, hyphens (-), and underscores (_). It cannot start or end with a hyphen (-) or an underscore (_). It cannot contain consecutive hyphens (-) or underscores (_).</td>
  </tr>
  <tr>
    <td>summary</td>
    <td>The summary.</td>
    <td>The summary must be 1 to 100 characters in length.</td>
  </tr>
  <tr>
    <td>repo_type</td>
    <td>The type of the repository.</td>
    <td>Valid values: PUBLIC and PRIVATE.</td>
  </tr>
  <tr>
    <td>namespace</td>
    <td>The namespace to which the repository belongs.</td>
    <td>The namespace must be 2 to 30 characters in length and can contain lowercase letters, digits, hyphens (-), and underscores (_). It cannot start with a hyphen (-) or an underscore (_).</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/6a3352223ed2e92ea5b6427deac763a1.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/f25304286dd697b68c43b34c11dbdc56.webp)

<a id="section-2-14"></a>

## 2.14. Create MaxCompute resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/4987102f692287ce6224997dd975585d.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |
| access_key | Your AccessKey ID. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID. |
| secret_key | Your AccessKey secret. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/59a207985a7fae8619ec34be86b7f9c3.webp)

<table>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>cu_name</td>
    <td>The name of the quota group.</td>
    <td>The name must be 3 to 32 characters in length and can contain letters, digits, and underscores (_). It must start with a letter.</td>
  </tr>
  <tr>
    <td>cu_num</td>
    <td>The number of quota groups.</td>
    <td>Set this parameter to a value greater than 0.</td>
  </tr>
  <tr>
    <td>cluster_name</td>
    <td>The name of the cluster.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt;</strong> <strong>MaxCompute</strong>.<br>2. In the left-side navigation pane, click Projects. On the Project management page, click <strong>Create Project</strong>. Then, obtain the cluster name.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/3f4e7737a303a4d594203f0e353695c9.webp)

<table>
  <tr>
    <td>user_name</td>
    <td>The name of the task account.</td>
    <td>The name can contain only letters, digits, hyphens (-), periods (.), and underscores (_).</td>
  </tr>
  <tr>
    <td>description</td>
    <td>The description of the task account.</td>
    <td>The description must be 2 to 255 characters in length, and can contain letters, digits, underscores (_), hyphens (-), periods (.), colons (:), and commas (,). It must start with a letter and cannot start with http:// or https://.</td>
  </tr>
  <tr>
    <td>disk</td>
    <td>The storage capacity.</td>
    <td>Unit: GB.</td>
  </tr>
  <tr>
    <td>aliyun_account</td>
    <td>The name of the Alibaba Cloud account.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> <strong>MaxCompute</strong>.<br>3. In the left-side navigation pane, click <strong>Task Accounts</strong>.On the page that appears, obtain the account name.</td>
  </tr>
  <tr>
    <td>pk</td>
    <td>The alias of the Apsara Stack tenant account.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>2. On the Basic Information section, obtain the alias of the Apsara Stack tenant account.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/b2f81052898ac14f5cc1389a49b597f9.webp)

<a id="section-2-15"></a>

## 2.15. Create DataWorks resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/f46746971ea0ccdec7381b624cde1b37.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/b0f73655ef51ef64828f057ab5e7b9b8.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |
| access_key | Your AccessKey ID. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/f4584c8e45da2d5c36ff73f155f04910.webp)

<table>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/9d2f361bad066612f1c66df60e984eab.webp)

<table>
  <tr>
    <td>project_id</td>
    <td>The ID of the workspace.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> <strong>DataWorks</strong>. Select an organization and a region, and click Access as Administrator to go to the DataWorks homepage.<br>3. Click the Expand icon in the upper-left corner of the page to view all products.<br>4. Choose All Products &gt; Data Integration. In the left-side navigation pane, choose Data Source &gt; Data Sources.Click <strong>Workspace</strong> <strong>Management</strong> in the left-side navigation pane, and obtain the workspace ID from the Configuration page.</td>
  </tr>
  <tr>
    <td>connection_type</td>
    <td>The connection type.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> <strong>DataWorks</strong>. Select an organization and a region, and click Access as Administrator to go to the DataWorks homepage.<br>3. Click the Expand icon in the upper-left corner of the page to view all products.<br>4. Choose All Products &gt; Data Integration. On the homepage of the Data Integration console, click Create Data <strong>Synchronization Solution</strong>.<br>5. Select the source for data synchronization from the Select Source drop-down list.The source is used as the connection type.</td>
  </tr>
  <tr>
    <td>content</td>
    <td>The details about the data source.</td>
    <td>N/A</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/320963c842906acf290581000e4dc6cc.webp)

<table>
  <tr>
    <td>env_type</td>
    <td>The environment to which the data source belongs.</td>
    <td>Valid values: 0 and 1. A value of 0 indicates the development environment, and a value of 1 indicates the production environment.</td>
  </tr>
  <tr>
    <td>sub_type</td>
    <td>The subtype of the data source.</td>
    <td>This parameter takes effect only if subtypes are available for a parent type. The following combinations are supported:<br>Parent type: rds<br>Sub-type: mysql, sqlserver, or postgresql</td>
  </tr>
  <tr>
    <td>name</td>
    <td>The name of the data source.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>description</td>
    <td>The description of the connection.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>folder_path</td>
    <td>The path of the folder.</td>
    <td>The folder path must be in the following format: Business Flow/{Business flow name}/[folderDi|folderMaxCom pute|folderGeneral|folderJdbc|fo lderUserDefined]/{Directory name}.<br>• The first part of the path must be Business Flow.<br>• The second part of the path must be the business flow name specified in the project.<br>• The third part of the path must be one of the following keywords: folderDi|folderMaxCompute|f olderGeneral|folderJdbc|folde rUserDefined.<br>• You can specify the last part of the folder path based on your needs.</td>
  </tr>
  <tr>
    <td>remind_type</td>
    <td>The trigger condition.</td>
    <td>Valid values: FINISHED, UNFINISHED, ERROR, CYCLE_UNFINISHED, and TIMEOUT.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/35f42e9856f6df29b8e2c0c454966dcf.webp)

<table>
  <tr>
    <td>remind_unit</td>
    <td>The type of the object to which the custom alert rule is applied.</td>
    <td>Valid values: NODE, BASELINE, PROJECT, and BIZPROCESS. A value of NODE indicates a node. A value of BASELINE indicates a baseline. A value of PROJECT indicates a workspace.A value of BIZPROCESS indicates a workflow.</td>
  </tr>
  <tr>
    <td>alert_methods</td>
    <td>The alert notification methods.</td>
    <td>Valid values: MAIL, SMS, and PHONE. The value PHONE is available only for DataWorks Professional Edition and more advanced editions. Separate multiple alert notification methods with commas (,).</td>
  </tr>
  <tr>
    <td>remind_name</td>
    <td>The name of the custom alert rule.</td>
    <td>The name can be up to 128 characters in length.</td>
  </tr>
  <tr>
    <td>user_id</td>
    <td>The user ID.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain the UID. The parameter value is the UID prefixed with 5.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/1370a8c5ec8331e4faed4912697c49ad.webp)

<table>
  <tr>
    <td>role_code</td>
    <td>The code of the role in the DataWorks workspace.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> <strong>DataWorks</strong>. Select an organization and a region, and click Access as Administrator to go to the DataWorks homepage.<br>3. Click the Expand icon in the upper-left corner of the page to view all products.<br>4. Choose All Products &gt; Data Integration. In the left-side navigation pane, choose Data Source &gt; Data Sources.Click User Management in the left-side navigation pane.Click Add Member. In the Add Member dialog box, view the batch role settings and obtain the role information.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/37daec4f845ce6911a56adf46cdfc2d5.webp)

<a id="section-2-16"></a>

## 2.16. Create API Gateway resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/ea9f41a8b6ec288097f759590f518e04.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| name | The name of the API group. | The group name must be globally unique. It must be 4 to 50 characters in length and can contain letters, digits, and underscores (_). It must start with a letter. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/a0a4db69bfb4eb2334862be43081aaec.webp)

<table>
  <tr>
    <td>group_id</td>
    <td>The ID of the API group.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt; API</strong> <strong>Gateway</strong>.<br>3. In the left-side navigation pane, choose Open API &gt; <strong>API</strong> <strong>Groups</strong>. On the API Groups page, click the API group that you want to manage and obtain the group ID.</td>
  </tr>
  <tr>
    <td>auth_type</td>
    <td>The authorization type.</td>
    <td>Set the value to APP.</td>
  </tr>
  <tr>
    <td>protocol</td>
    <td>The protocol type supported by the API.</td>
    <td>Valid values: HTTP, HTTPS, and WEBSOCKET.</td>
  </tr>
  <tr>
    <td>method</td>
    <td>The HTTP method.</td>
    <td>Valid values: GET, POST, DELETE, PUT, HEADER, TRACE, PATCH, CONNECT, and OPTIONS.</td>
  </tr>
  <tr>
    <td>path</td>
    <td>The API path.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>mode</td>
    <td>The request mode.</td>
    <td>Valid values: MAPPING and PASSTHROUGH.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/90c42aed73c5d6b14354b10fa2cdf225.webp)

<a id="section-2-17"></a>

## 2.17. Create Message Queue for Apache Kafka resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/b62054cc2c8fe6e6e01004980ae52efe.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/a5e978ed01b0f6a5c5d4b8ca34e9a6d8.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |
| access_key | Your AccessKey ID. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/4f0d70c82e2a84c01f7aacf232343d46.webp)

<table>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>topic</td>
    <td>The name of the topic.</td>
    <td>Two topics on a single instance cannot have the same name.The name can be up to 64 characters in length.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/b86fe379f2d82b4fb97d4f4ff3725ee0.webp)

<table>
  <tr>
    <td>local_topic</td>
    <td>The type of storage used by the topic.</td>
    <td>Valid values:<br>• false: The topic uses cloud storage.<br>• true: The topic uses local storage.</td>
  </tr>
  <tr>
    <td>compact_topic</td>
    <td>The log cleanup policy that is used for the topic. This parameter is available only when local_topic is set to true.</td>
    <td>Valid values:<br>• false: The default log cleanup policy is used for the topic.<br>• true: The log compaction policy is used for the topic.</td>
  </tr>
  <tr>
    <td>partition_num</td>
    <td>The number of partitions in the topic.</td>
    <td>Valid values: 1 to 48.</td>
  </tr>
  <tr>
    <td>remark</td>
    <td>The description of the topic.</td>
    <td>The description must be 3 to 64 characters in length.</td>
  </tr>
  <tr>
    <td>instance_id</td>
    <td>The instance ID.</td>
    <td>cluster-private-paas-default</td>
  </tr>
  <tr>
    <td>username</td>
    <td>The username of the SASL user.</td>
    <td>The name must be 1 and 64 characters in length. The name can contain only letters, digits, underscores (_), and hyphens (-).</td>
  </tr>
  <tr>
    <td>password</td>
    <td>The password of the SASL user.</td>
    <td>The password must be 1 to 64 characters in length and can contain letters, digits, and underscores (_). You must specify one of the password and kms_encrypted_password parameters.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/6293fd04e833c7dde0137416fea5a457.webp)

<table>
  <tr>
    <td>type</td>
    <td>The SASL mechanism.</td>
    <td>Valid values:<br>• plain: a simple mechanism that uses usernames and passwords to verify user identities. Message Queue for Apache Kafka provides an optimized PLAIN mechanism that allows you to dynamically create SASL users for an instance without the need to restart the instance.<br>• SCRAM: a mechanism that uses usernames and passwords to verify user identities. This mechanism provides better security protection than the PLAIN mechanism. Message Queue for Apache Kafka uses SCRAM-SHA-256.<br>Default value: plain.</td>
  </tr>
  <tr>
    <td>acl_resource_pattern_type</td>
    <td>The match mode.</td>
    <td>Valid values:<br>• LITERAL: exact match<br>• PREFIXED: prefix match</td>
  </tr>
  <tr>
    <td>acl_operation_type</td>
    <td>The operation type.</td>
    <td>Valid values:<br>• Write<br>• Read</td>
  </tr>
  <tr>
    <td>acl_resource_type</td>
    <td>The resource type.</td>
    <td>Valid values:<br>• Topic<br>• Group</td>
  </tr>
  <tr>
    <td>acl_resource_name</td>
    <td>The name of the resource.</td>
    <td>• The value can be the name of a topic or a consumer group.<br>• You can use an asterisk (*) to represent the names of all topics or consumer groups.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/63ef58bf6b6ca10c00d7f799a76e1fa2.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/6a0b43caf5fa394d85f40cb6d6520c79.webp)

<a id="section-2-18"></a>

## 2.18. Create AnalyticDB for MySQL resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/b1e5def3f953ca7021cedcb8373e1248.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/8e606ec1a4ae4c91b504fa55d48019e1.webp)

<table>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/d68e37b9f4ec634b67aa8fd7429f4246.webp)

<table>
  <tr>
    <td>cpu_type</td>
    <td>The CPU type.</td>
    <td>Set the value to Intel.</td>
  </tr>
  <tr>
    <td>db_node_count</td>
    <td>The number of nodes.</td>
    <td>Valid values: 2 to 128.</td>
  </tr>
  <tr>
    <td>compute_resource</td>
    <td>The specifications of computing resources that are used by the cluster in elastic mode.</td>
    <td>The increase in resources can speed up queries. AnalyticDB for MySQL automatically scales computing resources on demand.</td>
  </tr>
  <tr>
    <td>mode</td>
    <td>The cluster mode.</td>
    <td>Valid values: reserver and flexible.</td>
  </tr>
  <tr>
    <td>cluster_type</td>
    <td>The cluster type.</td>
    <td>Valid values: analyticdb and AnalyticdbOnPanguHybrid.</td>
  </tr>
  <tr>
    <td>db_cluster_category</td>
    <td>The cluster category.</td>
    <td>Valid values: Basic, Cluster, and MixedStorage.</td>
  </tr>
  <tr>
    <td>db_cluster_class</td>
    <td>The cluster specifications.</td>
    <td>Valid values:<br>• C8<br>• C32</td>
  </tr>
  <tr>
    <td>db_node_storage</td>
    <td>The storage capacity of a node.</td>
    <td>Unit: GB. Valid values:<br>• Valid values when db_cluster_class is set to C8: 100 to 1000<br>• Valid values when db_cluster_class is set to C32: 100 to 8000</td>
  </tr>
  <tr>
    <td>db_cluster_version</td>
    <td>The version of the AnalyticDB for MySQL Data Warehouse Edition cluster.</td>
    <td>Set the value to 3.0. Default value: 3.0.</td>
  </tr>
  <tr>
    <td>db_cluster_id</td>
    <td>The ID of the AnalyticDB for MySQL Data Warehouse Edition (V3.0) cluster.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> <strong>AnalyticDB for MySQL 3.0</strong>.<br>3. In the left-side navigation pane, click <strong>Clusters</strong>. Then, obtain the cluster ID.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/bc553f32fb781378c253d73897519776.webp)

<table>
  <tr>
    <td>account_name</td>
    <td>The name of the database account.</td>
    <td>The name can be up to 16 characters in length and can contain lowercase letters, digits, and underscores (_). It must start with a letter.</td>
  </tr>
  <tr>
    <td>account_password</td>
    <td>The password of the database account.</td>
    <td>The password must be 6 to 32 characters in length and can contain letters, digits, and underscores (_).</td>
  </tr>
</table>

<a id="section-2-19"></a>

## 2.19. Create an AnalyticDB for PostgreSQL instance

![](en-terraform-user-guide-v3.18.3-20241115.assets/7ac6190857136f90869f22cf104414ea.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/986df0b0c18164611fee703b895c899d.webp)

<table>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/6fc3beb423c76e9a34da02521d77aa8a.webp)

<table>
  <tr>
    <td>engine</td>
    <td>The database engine.</td>
    <td>Default value: gpdb.</td>
  </tr>
  <tr>
    <td>engine_version</td>
    <td>The engine version.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> AnalyticDB for <strong>PostgreSQL</strong>.<br>3. Click <strong>Create Instance</strong> and obtain the engine version.</td>
  </tr>
  <tr>
    <td>instance_class</td>
    <td>The instance type.</td>
    <td>For more information, seeInstance types.</td>
  </tr>
  <tr>
    <td>instance_group_count</td>
    <td>The number of compute nodes in the AnalyticDB for PostgreSQL instance.</td>
    <td>Valid values: 2, 4, 8, 16, and 32.</td>
  </tr>
  <tr>
    <td>description</td>
    <td>The description of the instance.</td>
    <td>Set this parameter to a string that is 2 to 256 characters in length.</td>
  </tr>
  <tr>
    <td>availability_zone</td>
    <td>The zone ID of the instance.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> AnalyticDB for <strong>PostgreSQL</strong>.<br>3. Click <strong>Create Instance</strong> and obtain the zone ID.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/b4e33a1919fc3374634aa426a6b94936.webp)

<a id="section-2-20"></a>

## 2.20. Create a PolarDB-X V1.0 instance

![](en-terraform-user-guide-v3.18.3-20241115.assets/1c4bf90dda545cc11d4c9987579b0ae0.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/1c80fa5a0da62c2ccd5eb49b606fb139.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |
| access_key | Your AccessKey ID. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID. |
| secret_key | Your AccessKey secret. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/45bab6a964e5bf9c37d4348b0eeacf52.webp)

<table>
  <tr>
    <td>region</td>
    <td>Region</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>zone_id</td>
    <td>The zone ID.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> <strong>PolarDB-X V1.0</strong>.<br>3. Click Create Instance, and obtain the zone ID from the Create PolarDB-X Instance page.</td>
  </tr>
  <tr>
    <td>instance_series</td>
    <td>The instance series.</td>
    <td>Valid values:<br>• drds.sn2.4c16g: Starter Edition<br>• drds.sn2.8c32g: Standard Edition<br>• drds.sn2.16c64g: Enterprise Edition</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/00b285f7417b0b8ccad4274a6f3d5554.webp)

<table>
  <tr>
    <td>instance_charge_type</td>
    <td>The billing method.</td>
    <td>Valid values: PrePaid and PostPaid.<br>Default value: PostPaid.</td>
  </tr>
  <tr>
    <td>vswitch_id</td>
    <td>The ID of the vSwitch.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>.<br>2. In the left-side navigation pane, click <strong>VSwitches</strong>.Obtain the vSwitch ID from the VSwitches page.</td>
  </tr>
  <tr>
    <td>specification</td>
    <td>The instance type.</td>
    <td>The value consists of the instance series and the specific instance specifications. For example, you can set the value to drds.sn2.4c16g.8c32g.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/c1cee675275e952dfd95cfa3437a43a5.webp)

<a id="section-2-21"></a>

## 2.21. Create an EBS storage set

![](en-terraform-user-guide-v3.18.3-20241115.assets/e166b8dbf3bfa715e0850a476f6ac4da.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/4b36126358c5a087082ecb6842fa5472.webp)

<table>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/574a44d149ade453be6ba7523645ef88.webp)

<table>
  <tr>
    <td>storage_set_name</td>
    <td>The name of the storage set.</td>
    <td>The name must be 2 to 128 characters in length. It must start with a letter and cannot start with <code> http:// </code> or <code> https:// </code>. It can contain letters, digits, colons (:), underscores (_), and hyphens (-).</td>
  </tr>
  <tr>
    <td>maxpartition_number</td>
    <td>The maximum number of partitions in the storage set.</td>
    <td>The value must be greater than or equal to 2.<br>Default value: 2.</td>
  </tr>
  <tr>
    <td>zone_id</td>
    <td>The zone ID of the storage set.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt; Elastic</strong> <strong>Compute Service</strong>. In the left-side navigation pane, choose Storage &amp; Snapshots &gt; Disks.<br>3. Click <strong>Create Disk</strong>, and obtain the zone ID from the Create Disk page.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/4f575ac0644a9fb878713a59b896a879.webp)

<a id="section-2-22"></a>

## 2.22. Create Auto Scaling resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/1e65a62ac0000b473dcfbb80824910eb.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/2d71fff86acc02e7eb86d0fa70eb478b.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/694e5ef18757db24267a0d5053c34ba7.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of ASAPI.</td>
    <td>1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/9222643bf679c5716278ba9391c69bc5.webp)

<table>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>min_size</td>
    <td>The minimum number of Elastic Compute Service (ECS) instances in the scaling group.</td>
    <td>If the number of ECS instances in the scaling group is less than the value of the MinSize parameter, Auto Scaling automatically creates ECS instances until the number of instances is equal to the value of the MinSize parameter.</td>
  </tr>
  <tr>
    <td>max_size</td>
    <td>The maximum number of ECS instances in the scaling group.</td>
    <td>If the number of ECS instances in the scaling group is greater than the value of the MaxSize parameter, Auto Scaling automatically removes ECS instances from the scaling group until the number of instances is equal to the value of the MaxSize parameter.</td>
  </tr>
  <tr>
    <td>scaling_group_name</td>
    <td>The name of the scaling group.</td>
    <td>The name of a scaling group must be unique in a region.<br>The name must be 2 to 64 characters in length, and can contain letters, digits, underscores (_), hyphens (-), and periods (.). The name must start with a letter or a digit.<br>The default value is the value of ScalingGroupId.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/265fa99df432ef16e1bb09defac55417.webp)

<table>
  <tr>
    <td>removal_policies</td>
    <td>The instance removal policies.</td>
    <td>Valid values:<br>• OldestInstance: removes ECS instances that are added to the scaling group at the earliest point in time.<br>• NewestInstance: removes ECS instances that are most recently added to the scaling group.<br>• OldestScalingConfiguration: removes ECS instances that are created based on the earliest scaling configuration.<br>• CustomPolicy: removes ECS instances based on the custom scale-in policy (Function).</td>
  </tr>
  <tr>
    <td>scaling_group_id</td>
    <td>The ID of the scaling group.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt; Auto</strong> <strong>Scaling</strong>.<br>3. In the left-side navigation pane, click <strong>Scaling Groups</strong>.On the Scaling Groups page, obtain the ID of the scaling group.</td>
  </tr>
  <tr>
    <td>image_id</td>
    <td>The ID of the image file.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt; Auto</strong> <strong>Scaling</strong>.<br>3. In the left-side navigation pane, click <strong>Scaling Groups</strong> to view the list of scaling groups.<br>4. Click the ID of the scaling group that you want to manage to go to the scaling group details page.<br>5. Click the Instance Configuration Sources tab and click Create Scaling Configuration. Then, obtain the image ID.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/2306e16328a30193386fc699265913d7.webp)

<table>
  <tr>
    <td>instance_type</td>
    <td>The ECS instance type.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt; Auto</strong> <strong>Scaling</strong>.<br>3. In the left-side navigation pane, click <strong>Scaling Groups</strong> to view the list of scaling groups.<br>4. Click the ID of the scaling group that you want to manage to go to the scaling group details page.<br>5. Click the Instance Configuration Sources tab and click Create Scaling Configuration. Then, obtain the ECS instance type.</td>
  </tr>
  <tr>
    <td>security_group_id</td>
    <td>The ID of the security group to which the ECS instance belongs.</td>
    <td>ECS instances in the same security group can access each other.</td>
  </tr>
  <tr>
    <td>force_delete</td>
    <td>Specifies whether to forcibly delete the last scaling configuration and its scaling group.</td>
    <td>Default value: false.</td>
  </tr>
  <tr>
    <td>adjustment_type</td>
    <td>The method used by the scaling rule to adjust the number of instances.</td>
    <td>This parameter is required and applicable only to simple scaling rules. Valid values: QuantityChangeInCapacity: adds or removes the specified number of ECS instances to or from the scaling group.PercentChangeInCapacity: adds or removes the specified percentage of ECS instances to or from the scaling group.TotalCapacity: adjusts the number of ECS instances in the scaling group to a specified number.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/80450ab7e8457d1674edf07163c049fe.webp)

<table>
  <tr>
    <td>adjustment_value</td>
    <td>The number of ECS instances to be adjusted by the scaling rule.</td>
    <td>This parameter is required and applicable only to simple scaling rules. The number of ECS instances to be adjusted in a single scaling activity cannot exceed 500.<br>• Valid values if adjustment_type is set to QuantityChangeInCapacity: -500 to 500<br>• Valid values if adjustment_type is set to PercentChangeInCapacity: -100 to 10000<br>• Valid values if adjustment_type is set to TotalCapacity: 0 to 1000</td>
  </tr>
  <tr>
    <td>cooldown</td>
    <td>The amount of time to wait after a scaling activity completes and before the next scaling activity can start.</td>
    <td>This parameter is applicable only to simple scaling rules.Valid values: 1 to 86400. Unit: seconds. This parameter is empty by default. If you do not set this parameter, the return value is 0, which is the default value of the Integer data type.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/3a000d9dba775bb92660c19ea7f23dc5.webp)

<a id="section-2-23"></a>

## 2.23. Create CloudMonitor resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/7a87f136853ec0d309fc5130320827de.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/7c661a32475e031ddc6b13729bc8622c.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/4d0d036c5ded2a664f584bb062e1d214.webp)

<table>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/af9b7a65c72a16086e3cf9913f117537.webp)

<table>
  <tr>
    <td>name</td>
    <td>The name of the alert rule.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>project</td>
    <td>The name of the monitoring project.</td>
    <td>Examples: acs_ecs_dashboard and acs_rds_dashboard.</td>
  </tr>
  <tr>
    <td>metric</td>
    <td>The name of the metric corresponding to the project.</td>
    <td>Examples: CPUUtilization and networkin_rate.</td>
  </tr>
  <tr>
    <td>dimensions</td>
    <td>The resources associated with the alert rule.</td>
    <td>Set this parameter to a set of key-value pairs. Examples of keys: instanceId, device, and port. The value of each key must be a string. Separate multiple key-value pairs with commas (,).</td>
  </tr>
  <tr>
    <td>escalations_critical</td>
    <td>The critical-level alert configurations.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>enabled</td>
    <td>Specifies whether to enable the alert rule.</td>
    <td>Default value: true.</td>
  </tr>
  <tr>
    <td>contact_groups</td>
    <td>The contact groups to which the alert rule is applied.</td>
    <td>Set this parameter to the contact groups that have been created in the console.</td>
  </tr>
  <tr>
    <td>effective_interval</td>
    <td>The interval at which the alert rule takes effect.</td>
    <td>Specify this parameter in the hh:mm-hh:mm format, such as 0:00-4:00. Default value: 00:00-23:59.</td>
  </tr>
  <tr>
    <td>describe</td>
    <td>The description of the alert contact.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>channels_mail</td>
    <td>The email address of the alert contact.</td>
    <td>After an email address is added or modified, the recipient receives an email that contains an activation link. The system adds the recipient to the alert contact list only after the email address is activated.</td>
  </tr>
  <tr>
    <td>alarm_contact_name</td>
    <td>The name of the alert contact.</td>
    <td>Specify a custom value.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/abf1b3c20a77ab651c7a52130c681bc6.webp)

<table>
  <tr>
    <td>alarm_contact_group_name</td>
    <td>The name of the alert contact group.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>address</td>
    <td>The URL or IP address monitored by the site monitoring task.</td>
    <td>Example: https://www.aliyun.com.</td>
  </tr>
  <tr>
    <td>task_name</td>
    <td>The name of the site monitoring task.</td>
    <td>The name must be 4 to 100 characters in length and can contain letters, digits, and underscores (_).</td>
  </tr>
  <tr>
    <td>task_type</td>
    <td>The protocol that is used by the site monitoring task.</td>
    <td>Protocols such as HTTP, PING, TCP, UDP, DNS, SMTP, POP3, and FTP can be used for site monitoring.</td>
  </tr>
  <tr>
    <td>interval</td>
    <td>The monitoring interval of the site monitoring task.</td>
    <td>Unit: minutes. Valid values: 1, 5, and 15. Default value: 1.</td>
  </tr>
  <tr>
    <td>isp_cities</td>
    <td>The detection points in the JSON array format.</td>
    <td>Example: [{"city":"546", "isp":"465"}, {"city":"572", "isp":"465"}, {"city":"738", "isp":"465"}]. The three city codes respectively represent Beijing, Hangzhou, and Qingdao.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/4d120433f88a3f432c0a80ad25e88f70.webp)

<a id="section-2-24"></a>

## 2.24. Register a database instance and a user with DMS Enterprise

![](en-terraform-user-guide-v3.18.3-20241115.assets/0bb20c3309f4398448c366b4bf6c8748.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/99eb13a0f942e3fc7a3636d638ea0f11.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/4281cf2105d7692637b748b9f3784f44.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of ASAPI.</td>
    <td>1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/7334df84e6972c02d0d5832753e49d45.webp)

<table>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>use_dsql</td>
    <td>Specifies whether to enable cross-instance query.</td>
    <td>Valid values:<br>• 0: disables cross-instance query.<br>• 1: enables cross-instance query.</td>
  </tr>
  <tr>
    <td>instance_alias</td>
    <td>The name of the database instance.</td>
    <td>Specify a name that uniquely distinguishes the instance.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/60b9d6632bbcfd2be982e590733d3733.webp)

<table>
  <tr>
    <td>ecs_region</td>
    <td>The region of the Elastic Compute Service (ECS) instance.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt; Elastic</strong> <strong>Compute Service</strong>.<br>3. In the left-side navigation pane, choose Instances &amp; Images &gt; Instances. On the Instances page, click <strong>Create</strong> <strong>Instance</strong>. Then, obtain the region information from the Create Instance wizard page.</td>
  </tr>
  <tr>
    <td>env_type</td>
    <td>The environment type.</td>
    <td>Valid values:<br>• product: production environment<br>• dev: development environment<br>• pre: pre-release environment<br>• test: test environment<br>• sit: system integration test environment<br>• uat: user acceptance test environment<br>• pet: stress testing environment<br>• stag: staging environment</td>
  </tr>
  <tr>
    <td>tid</td>
    <td>The tenant ID.</td>
    <td>Example: 1.</td>
  </tr>
  <tr>
    <td>instance_source</td>
    <td>The source of the database instance.</td>
    <td>Valid values: PUBLIC_OWN, RDS, ECS_OWN, and VPC_IDC.</td>
  </tr>
  <tr>
    <td>dba_uid</td>
    <td>The unique ID (UID) of the database administrator (DBA) for the database instance.</td>
    <td>Specify the UID of the DBA for the database instance.</td>
  </tr>
  <tr>
    <td>network_type</td>
    <td>The network type.</td>
    <td>Valid values: CLASSIC and VPC.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/b8627b3c608f9bdb1c15870c7cf5a4bf.webp)

<table>
  <tr>
    <td>database_user</td>
    <td>The database account.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> <strong>ApsaraDB RDS</strong>.<br>3. In the left-side navigation pane, click Instances. On the Instances page, find the instance that you want to manage and click <strong>Manage</strong> in the Actions column.<br>4. In the left-side navigation pane, click <strong>Accounts</strong>. Then, obtain the account information.</td>
  </tr>
  <tr>
    <td>export_timeout</td>
    <td>The timeout period for exporting data from the database instance.</td>
    <td>Unit: seconds.</td>
  </tr>
  <tr>
    <td>safe_rule</td>
    <td>The security rule for the database instance.</td>
    <td>Set this parameter to the name of the security rule in your enterprise.</td>
  </tr>
  <tr>
    <td>data_link_name</td>
    <td>The name of the data link for cross-database query.</td>
    <td>Cross-database query is not supported for instances whose control mode is Flexible Management or Stable Change.</td>
  </tr>
  <tr>
    <td>ddl_online</td>
    <td>Specifies whether to enable the online data definition language (DDL) service.</td>
    <td>This parameter is available only for MySQL and PolarDB. Valid values:<br>• 0: The service is disabled.<br>• 1: The native online DDL service prevails.<br>• 2: The lock-free schema change feature of DMS prevails.</td>
  </tr>
  <tr>
    <td>query_timeout</td>
    <td>The timeout period for querying data in the database instance.</td>
    <td>Unit: seconds.</td>
  </tr>
  <tr>
    <td>instance_type</td>
    <td>The database type.</td>
    <td>Valid values: MySQL, SQLServer, PostgreSQL, Oracle, DRDS, OceanBase, Mongo, and Redis.</td>
  </tr>
  <tr>
    <td>host</td>
    <td>The endpoint of the database instance.</td>
    <td>Example: dmstest.rds.aliyun.com.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/cf3669abbc32e30e0c10f4d9aab63a65.webp)

<table>
  <tr>
    <td>port</td>
    <td>The port used to connect to the database instance.</td>
    <td>Example: 3306.</td>
  </tr>
  <tr>
    <td>database_password</td>
    <td>The logon password of the database instance.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>role_names</td>
    <td>The role of the user.</td>
    <td>Valid values:<br>• USER<br>• DBA<br>• ADMIN<br>• SECURITY_ADMIN</td>
  </tr>
  <tr>
    <td>uid</td>
    <td>The UID of the user to be added.</td>
    <td>1. Use the username and password of the user account to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain the UID of the user.</td>
  </tr>
  <tr>
    <td>nick_name</td>
    <td>The name of the user.</td>
    <td>Specify a custom value.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/4d9f4d28670fd9948fd3a5e4574d8123.webp)

<a id="section-2-25"></a>

## 2.25. Create a DNS domain name

![](en-terraform-user-guide-v3.18.3-20241115.assets/11207000a2e4398d1a2c23cc68c1192d.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/1cc96c6e8fd5aa577241eda6f3ec616b.webp)

<table>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/41f043d6d37468046b40384db95d3234.webp)

<table>
  <tr>
    <td>domain_name</td>
    <td>The domain name.</td>
    <td>The domain name must meet the following requirements:<br>1. The domain name can be up to 220 characters in length.This includes the period (.) at the end.<br>2. The domain name can contain multiple domain name segments that are separated by periods (.). A domain name segment can be up to 63 characters in length. The domain name cannot contain consecutive periods (.).<br>3. The domain name can contain only letters, digits, hyphens (-), and underscores (_).<br>4. The domain name is not case-sensitive.<br>5. The domain name must end with a period (.).</td>
  </tr>
  <tr>
    <td>remark</td>
    <td>The description of the domain name.</td>
    <td>Specify a custom value.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/b2e28638b33755a647b48ea578db964e.webp)

<a id="section-2-26"></a>

## 2.26. Create DTS resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/a8c840c60c5d8a4d53f8a10aa0ea1586.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/b144a4bc022114ab90560f36907f7cf2.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/5fee11b91465c85ed9d02594bca3847a.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/d0d35687bc03fd8365b2bf0cc8bce15f.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/8589872a83470aeee1bc413fca6effcb.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/d17c6013dca14c08a86377e4df1706d8.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of ASAPI.</td>
    <td>1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/6dba39319704534be2f55f3e8e00bbad.webp)

<table>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>source_endpoint_instance_type</td>
    <td>The type of the source instance.</td>
    <td>Valid values: RDS, PolarDB, DRDS, LocalInstance, ECS, Express, CEN, and dg.</td>
  </tr>
  <tr>
    <td>source_endpoint_password</td>
    <td>The password of the database account used to connect to the source instance.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>subscription_instance_network_type</td>
    <td>The network type for the change tracking task.</td>
    <td>Valid values: classic and vpc.</td>
  </tr>
  <tr>
    <td>payment_type</td>
    <td>The resource billing method.</td>
    <td>Valid values: Subscription and PayAsYouGo.</td>
  </tr>
  <tr>
    <td>source_endpoint_database_na me</td>
    <td>The name of the source database.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>source_endpoint_user_name</td>
    <td>The username of the database account used to connect to the source instance.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>db_list</td>
    <td>The list of databases whose data you want to track.</td>
    <td>Set this parameter to a JSON string.</td>
  </tr>
  <tr>
    <td>source_endpoint_engine_name</td>
    <td>The type of the source database.</td>
    <td>Valid values: MySQL and Oracle.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/50b55b8715398680d8f5af225bc1bb8d.webp)

<table>
  <tr>
    <td>source_endpoint_region</td>
    <td>The region where the source database resides.</td>
    <td>Example: cn-hangzhou.</td>
  </tr>
  <tr>
    <td>subscription_instance_vswitch_i d</td>
    <td>The ID of the vSwitch for the change tracking task.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console. In the top navigation bar, choose <strong>Products</strong> &gt; <strong>Virtual Private</strong> <strong>Cloud</strong>.<br>2. In the left-side navigation pane, click <strong>VSwitches</strong>.Obtain the vSwitch ID from the VSwitches page.</td>
  </tr>
  <tr>
    <td>source_endpoint_instance_id</td>
    <td>The ID of the source instance.</td>
    <td>ApsaraDB RDS is used as an example in the following steps:<br>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> <strong>ApsaraDB RDS</strong>.<br>3. View the instance list and obtain the ID of the instance that you want to manage.</td>
  </tr>
  <tr>
    <td>subscription_instance_vpc_id</td>
    <td>The ID of the VPC for the change tracking task.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>.<br>3. View the VPC list and obtain the ID of the VPC that you want to manage.</td>
  </tr>
  <tr>
    <td>dts_job_name</td>
    <td>The name of the change tracking task.</td>
    <td>Specify a value that is 0 to 128 characters in length.</td>
  </tr>
  <tr>
    <td>sync_architecture</td>
    <td>The synchronization mode.</td>
    <td>Valid values: bidirectional and oneway.</td>
  </tr>
  <tr>
    <td>payment_type</td>
    <td>The resource billing method.</td>
    <td>Valid values: Subscription and PayAsYouGo.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/74754c4e478eeb9d515cb62b1a1570c3.webp)

<table>
  <tr>
    <td>destination_endpoint_engine_n ame</td>
    <td>The type of the destination database.</td>
    <td>Valid values: ADS, DB2, DRDS, DataHub, Greenplum, MSSQL, MySQL, PolarDB, PostgreSQL, Redis, Tablestore, as400, clickhouse, kafka, mongodb, odps, oracle, polardb_o, polardb_pg, and tidb.</td>
  </tr>
  <tr>
    <td>destination_endpoint_region</td>
    <td>The region where the destination instance resides.</td>
    <td>Example: cn-hangzhou.</td>
  </tr>
  <tr>
    <td>instance_class</td>
    <td>The instance type.</td>
    <td>Valid values: large, medium, micro, small, xlarge, and xxlarge.</td>
  </tr>
  <tr>
    <td>destination_endpoint_database _name</td>
    <td>The name of the destination database.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>destination_endpoint_password</td>
    <td>The password of the database account.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>destination_endpoint_instance_type</td>
    <td>The type of the destination instance.</td>
    <td>Valid values: ads, CEN, DATAHUB, DG, ECS, EXPRESS, GREENPLUM, MONGODB, OTHER, PolarDB, POLARDBX20, and RDS.</td>
  </tr>
  <tr>
    <td>destination_endpoint_instance_i d</td>
    <td>The ID of the destination instance.</td>
    <td>ApsaraDB RDS is used as an example in the following steps:<br>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> <strong>ApsaraDB RDS</strong>.<br>3. View the instance list and obtain the ID of the instance that you want to manage.</td>
  </tr>
  <tr>
    <td>destination_endpoint_user_nam e</td>
    <td>The username of the database account used to connect to the destination instance.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>dts_instance_id</td>
    <td>The ID of the data synchronization instance.</td>
    <td>Set this parameter to the ID of the alibabacloudstack_dts_synchro nization_instance resource.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/66647c9d32f1c46503e3fe71d52d6de8.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/0bc04d9e1e6945eec16f6ff4fee2e500.webp)

<a id="section-2-27"></a>

## 2.27. Create a DBS backup schedule

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/6c41b422ec994673957ff9d8c4f8aba6.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of ASAPI.</td>
    <td>1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/d3ff5bdec6fd0760e8f2a402089ad6cd.webp)

<table>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>database_type</td>
    <td>The database type.</td>
    <td>Valid values:<br>• MySQL<br>• Oracle<br>• MariaDB<br>• PostgreSQL<br>• PPAS<br>• DRDS<br>• MongoDB<br>• Redis<br>• File</td>
  </tr>
  <tr>
    <td>instance_class</td>
    <td>The instance type.</td>
    <td>Valid values:<br>• micro: basic specifications<br>• small: low-end specifications<br>• medium: medium-end specifications<br>• large: high-end specifications<br>• xlarge: high-end specifications with no upper limit on the amount of backup data</td>
  </tr>
  <tr>
    <td>backup_method</td>
    <td>The backup method.</td>
    <td>Valid values:<br>• logical: logical backup<br>• physical: physical backup<br>• duplication: dump backup</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/4631c686520c77358cbdaed4fc547bd6.webp)

<table>
  <tr>
    <td>backup_plan_name</td>
    <td>The name of the backup schedule.</td>
    <td>Specify a value that is 0 to 128 characters in length.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/6818c985af9fb5c788f6711a361e216e.webp)

<a id="section-2-28"></a>

## 2.28. Create DataHub resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/aeb43cc1af7dad5917b3071fcfe67a31.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/4d0d036c5ded2a664f584bb062e1d214.webp)

<table>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/12acd1ebfda8473a434cbe8a768a19f6.webp)

<table>
  <tr>
    <td>name</td>
    <td>The name of the project.</td>
    <td>The name must be 3 to 32 characters in length and can contain letters, digits, and underscores (_). The name is case-insensitive.</td>
  </tr>
  <tr>
    <td>comment</td>
    <td>The description of the project.</td>
    <td>The description can be up to 255 characters in length.</td>
  </tr>
  <tr>
    <td>record_schema</td>
    <td>The schema of the topic.</td>
    <td>This parameter takes effect only on TUPLE topics. The following data types (case-insensitive) are supported:<br>• BIGINT<br>• STRING<br>• BOOLEAN<br>• DOUBLE<br>• TIMESTAMP</td>
  </tr>
  <tr>
    <td>record_type</td>
    <td>The type of the topic.</td>
    <td>Valid values: BLOB and TUPLE.In a BLOB topic, the data is organized into binary records and encoded in Base64. In a TUPLE topic, the data has a fixed schema. Default value: TUPLE.</td>
  </tr>
  <tr>
    <td>shard_count</td>
    <td>The number of shards contained in the topic.</td>
    <td>Valid values: 1 to 10. Default value: 1.</td>
  </tr>
  <tr>
    <td>life_cycle</td>
    <td>The lifecycle of the topic.</td>
    <td>Valid values: 1 to 7. Default value: 3.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/80d5d9875ff978340b5e91aa0fdd10aa.webp)

<a id="section-2-29"></a>

## 2.29. Create EDAS resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/8a4426f984edff92c93d9e5f18733de2.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| vpc_name | The name of the VPC. | The name must be 2 to 128 characters in length and can contain letters, digits, underscores (_), and hyphens (-). It must start with a letter and cannot start with http:// or https://. |
| cidr_block | The CIDR block of the VPC. | 1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>. In the left-side navigation pane, click <strong>Virtual Private Clouds</strong>. On the Virtual Private Clouds page, obtain the CIDR block of the VPC.<br>2. You can define a new CIDR block for the VPC. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/47d0c957d46df0aa07b6ccb423c438ea.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| network_mode | The network type of the cluster. | Valid values:<br>• 1: classic network<br>• 2: virtual private cloud (VPC) |
| cluster_name | The name of the cluster. | The name can be up to 64 characters in length and can contain letters, digits, underscores (_), and periods (.). |
| cluster_type | The type of the cluster. | Valid values:<br>2: ECS cluster |

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| application_name | The name of the EDAS application. | The name can be up to 36 characters in length and can contain letters, digits, underscores (_), and hyphens (-). |
| package_type | The type of the deployment package for the application. | Valid values: WAR and JAR. |
| cluster_id | The cluster ID of the application. | If you do not configure this parameter, the default cluster ID is used. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/68ca1366089f380d2987a2ba7131e7cc.webp)

<table>
  <tr>
    <td>component_id</td>
    <td>The ID of the component in the container in which the application is deployed.</td>
    <td>If you do not configure the runtime environment when you create and deploy an application, you can set this parameter to fellow. The first time you use a WAR package to deploy a native Dubbo or Spring Cloud application, you must specify the version number of the Apache Tomcat component based on the deployed application. You can call the ListClusterOperation operation to query the component ID. The first time you use a WAR package to deploy a non-native Dubbo or Spring Cloud application, you do not need to configure this parameter.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/f0a5a417e091ff6d82355343bd952eb2.webp)

<a id="section-2-30"></a>

## 2.30. Create Express Connect resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/a0de2bebf10ead614f93986a8471789c.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/9424d1bc01619b321b99030b5b5427f6.webp)

<table>
  <tr>
    <td>device_name</td>
    <td>The name of the access device.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt; Express</strong> <strong>Connect</strong>.<br>3. In the left-side navigation pane, click Physical Connection. On the Physical Connection page, click <strong>Apply</strong> <strong>for Physical Connection</strong>.<br>4. Select an access point and obtain the name of the access device.</td>
  </tr>
  <tr>
    <td>type</td>
    <td>The type of the Express Connect circuit.</td>
    <td>Default value: VPC.</td>
  </tr>
  <tr>
    <td>description</td>
    <td>The description of the Express Connect circuit.</td>
    <td>The description must be 2 to 256 characters in length and can contain letters, digits, underscores (_), hyphens (-), periods (.), commas (,), and colons (:). It must start with a letter and cannot start with http:// or https://.</td>
  </tr>
  <tr>
    <td>access_point_id</td>
    <td>The ID of the access point.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt; Express</strong> <strong>Connect</strong>.<br>3. In the left-side navigation pane, click Physical Connection. On the Physical Connection page, click <strong>Apply</strong> <strong>for Physical Connection</strong>.<br>4. Obtain the access point ID from the <strong>Leased line</strong> <strong>configuration</strong> section.</td>
  </tr>
  <tr>
    <td>line_operator</td>
    <td>The Internet service provider (ISP).</td>
    <td>Valid values:<br>• CT: China Telecom<br>• CU: China Unicom<br>• CM: China Mobile<br>• CO: other ISPs in China<br>• Equinix<br>• Others: other ISPs outside China</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/db299b6173fcc118fefff0ffd5b1cced.webp)

<table>
  <tr>
    <td>peer_location</td>
    <td>The peer address.</td>
    <td>Enter the address of the peer data center connected by using the Express Connect circuit.</td>
  </tr>
  <tr>
    <td>port_type</td>
    <td>The port type.</td>
    <td>Valid values:<br>• 100Base-T: fast electrical port<br>• 1000Base-T: Gigabit electrical port<br>• 1000Base-LX: 10 km Gigabit single-mode optical port<br>• 10GBase-T: Gigabit electrical port<br>• 10GBase-LR: 10 km Gigabit single-mode optical port<br>• 40GBase-LR: 40 Gigabit single-mode optical port<br>• 100GBase-LR: 100,000 Gigabit single-mode optical port</td>
  </tr>
  <tr>
    <td>bandwidth</td>
    <td>The bandwidth of the port.</td>
    <td>Unit: Mbit/s. Valid values: 2 to maximum bandwidth of the port type.</td>
  </tr>
  <tr>
    <td>physical_connection_name</td>
    <td>The name of the Express Connect circuit.</td>
    <td>The name must be 2 to 128 characters in length and can contain letters, digits, underscores (_), and hyphens (-). It must start with a letter and cannot start with http:// or https://.</td>
  </tr>
  <tr>
    <td>peer_gateway_ip</td>
    <td>The IPv4 address of the gateway at the customer side.</td>
    <td>The value cannot be the same as the IPv4 address of the gateway at the Alibaba Cloud side.</td>
  </tr>
  <tr>
    <td>peering_subnet_mask</td>
    <td>The IPv4 subnet mask.</td>
    <td>Set this parameter to the subnet mask of the IPv4 addresses that you specify for the VBR and the gateway device in the data center.</td>
  </tr>
  <tr>
    <td>virtual_border_router_name</td>
    <td>The name of the VBR.</td>
    <td>The name must be 2 to 128 characters in length and can contain letters, digits, underscores (_), and hyphens (-). It must start with a letter.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/106f8c1c9242b1ac8d792bb039ad0af0.webp)

<table>
  <tr>
    <td>physical_connection_id</td>
    <td>The ID of the Express Connect circuit.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt; Express</strong> <strong>Connect</strong>.<br>3. In the left-side navigation pane, click <strong>Physical</strong> <strong>Connection</strong>. On the Physical Connection page, obtain the ID of the Express Connect circuit.</td>
  </tr>
  <tr>
    <td>vlan_id</td>
    <td>The VLAN ID of the VBR.</td>
    <td>Valid values: 0 to 2999. The value 0 indicates that no VLAN is configured.</td>
  </tr>
  <tr>
    <td>local_gateway_ip</td>
    <td>The IPv4 address of the gateway at the Alibaba Cloud side.</td>
    <td>The value cannot be the same as the IPv4 address of the gateway at the customer side.</td>
  </tr>
</table>

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| peer_gateway_ip | The IPv4 address of the gateway at the customer side. | The value cannot be the same as the IPv4 address of the gateway at the Alibaba Cloud side. |
| peering_subnet_mask | The IPv4 subnet mask. | Set this parameter to the subnet mask of the IPv4 addresses that you specify for the VBR and the gateway device in the data center. |
| virtual_border_router_name | The name of the VBR. | The name must be 2 to 128 characters in length and can contain letters, digits, underscores (_), and hyphens (-). It must start with a letter. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/c336703e36706c8ba1b657975dab8e7d.webp)

<table>
  <tr>
    <td>physical_connection_id</td>
    <td>The ID of the Express Connect circuit.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt; Express</strong> <strong>Connect</strong>.<br>3. In the left-side navigation pane, click <strong>Physical</strong> <strong>Connection</strong>. On the Physical Connection page, obtain the ID of the Express Connect circuit.</td>
  </tr>
  <tr>
    <td>vlan_id</td>
    <td>The VLAN ID of the VBR.</td>
    <td>Valid values: 0 to 2999. The value 0 indicates that no VLAN is configured.</td>
  </tr>
  <tr>
    <td>local_gateway_ip</td>
    <td>The IPv4 address of the gateway at the Alibaba Cloud side.</td>
    <td>The value cannot be the same as the IPv4 address of the gateway at the customer side.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/357de4d834d6cd247fa53b82b99734e7.webp)

<a id="section-2-31"></a>

## 2.31. Create an E-HPC job template

![](en-terraform-user-guide-v3.18.3-20241115.assets/ee6013cef6a0d33584d79ab00f04a902.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/1b79455409acbaf1e894d2f1795eb363.webp)

<table>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/0806942827fb907319918a1157c809f6.webp)

<table>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>job_template_name</td>
    <td>The name of the job template.</td>
    <td>The name must be 2 to 64 characters in length and can contain only letters, digits, hyphens (-), and underscores (_). It must start with a letter.</td>
  </tr>
  <tr>
    <td>command_line</td>
    <td>The job execution command.</td>
    <td>N/A</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/e8593ab055c506e3f0b0b747305a27a9.webp)

<a id="section-2-32"></a>

## 2.32. Create an Elasticsearch cluster

![](en-terraform-user-guide-v3.18.3-20241115.assets/61d2f63cb93fadf261eae112704beed9.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/d141c1b4d25a7ccd48860288214ee98a.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of ASAPI.</td>
    <td>1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/927213bc0bbafb14c3f971897248eb76.webp)

<table>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>instance_charge_type</td>
    <td>The billing method of the cluster.</td>
    <td>Valid values: PrePaid and PostPaid. Default value: PostPaid.</td>
  </tr>
  <tr>
    <td>data_node_amount</td>
    <td>The number of warm nodes in the Elasticsearch cluster.</td>
    <td>Valid values: 2 to 50.</td>
  </tr>
  <tr>
    <td>data_node_spec</td>
    <td>The specifications of data nodes in the Elasticsearch cluster.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> <strong>Elasticsearch</strong>.<br>3. Select an organization and a region, and then click the access button below to go to the Elasticsearch homepage.<br>4. On the Overview page, click Create Cluster. Then, obtain the data node specifications.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/583dc501a8e890983a5c21e4870b1a96.webp)

<table>
  <tr>
    <td>data_node_disk_size</td>
    <td>The storage space of each data node.</td>
    <td>The value depends on the disk type. Unit: GiB. If the disk type is SSD cloud disk, the maximum value of this parameter is 2048 GiB or 2 TB.<br>If the disk type is ultra disk, the maximum value of this parameter is 5120 GiB or 5 TB.If the volume of the data that you want to store exceeds 2,048 GiB, you can set this parameter to 2560, 3072, 3584, 4096, 4608, or 5120. If the storage space of the disk for a purchased cluster is less than 2,048 GiB, you can resize the disk to a maximum of 2,048 GiB.</td>
  </tr>
  <tr>
    <td>data_node_disk_type</td>
    <td>The storage type.</td>
    <td>Valid values: cloud_ssd and cloud_efficiency.</td>
  </tr>
  <tr>
    <td>client_node_amount</td>
    <td>The number of client nodes in the Elasticsearch cluster.</td>
    <td>Valid values: 2 to 25.</td>
  </tr>
  <tr>
    <td>client_node_spec</td>
    <td>The client node specifications.</td>
    <td>If this parameter is specified, a client node is created.</td>
  </tr>
  <tr>
    <td>protocol</td>
    <td>The protocol for the Elasticsearch cluster.</td>
    <td>Valid values: HTTP and HTTPS.Default value: HTTP.</td>
  </tr>
  <tr>
    <td>vswitch_id</td>
    <td>The ID of the vSwitch.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>.<br>2. In the left-side navigation pane, click <strong>VSwitches</strong>.Obtain the vSwitch ID from the VSwitches page.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/906cef2fcb92c89486ce5cc09df34598.webp)

<table>
  <tr>
    <td>password</td>
    <td>The password of the Elasticsearch cluster.</td>
    <td>The password must be 8 to 32 characters in length and contain at least three of the following character types: uppercase letters, lowercase letters, digits, and special characters. Special characters include ! @ # $ % ^ &amp; * ( ) _ + -=</td>
  </tr>
  <tr>
    <td>version</td>
    <td>The version of the Elasticsearch cluster.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, choose <strong>Products &gt;</strong> <strong>Elasticsearch</strong>.<br>3. Select an organization and a region, and then click the access button below to go to the Elasticsearch homepage.<br>4. On the Overview page, click Create Cluster. Then, obtain the version information.</td>
  </tr>
  <tr>
    <td>description</td>
    <td>The description of the cluster.</td>
    <td>Set this parameter to a string that is 0 to 30 characters in length.</td>
  </tr>
  <tr>
    <td>zone_count</td>
    <td>The number of zones supported by the Elasticsearch cluster.</td>
    <td>Valid values: 1 to 3. The data_node_amount value must be an integer multiple of the zone_count value.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/63a6a576cab2dcf8038744bb53f4a3bf.webp)

<table>
  <tr>
    <td>tags</td>
    <td>The tags to assign to resources.</td>
    <td>• key: A key can be up to 128 characters in length. It cannot start with acs: or aliyun. It cannot contain http:// or https://. It cannot be an empty string.<br>• value: A value can be up to 128 characters in length. It cannot contain http:// or https://. It can be an empty string.</td>
  </tr>
</table>

<a id="section-2-33"></a>

## 2.33. Create an ApsaraDB for HBase cluster

![](en-terraform-user-guide-v3.18.3-20241115.assets/ad8de86d68097665005693826dfc7c57.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/c26d11e99df996ba3eae58723723ab14.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |
| access_key | Your AccessKey ID. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/105cdf9ebbc5183ba343f5089de5ad41.webp)

<table>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>cold_storage_size</td>
    <td>The cold storage capacity of the cluster.</td>
    <td>Unit: GB. Valid values:<br>• 0: indicates that cold storage is disabled.<br>• 800 to 1000000: indicates that cold storage is enabled.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/24860772772af786ffd13eaef3b0b38d.webp)

<table>
  <tr>
    <td>password</td>
    <td>The password of the account used to connect to the cluster.</td>
    <td>The password must be 0 to 128 characters in length.</td>
  </tr>
  <tr>
    <td>immediate_delete_flag</td>
    <td>Specifies whether to immediately delete the cluster.</td>
    <td>A value of true specifies to immediately delete the cluster.A value of false specifies to delay the deletion of the cluster.</td>
  </tr>
  <tr>
    <td>account</td>
    <td>The username of the account used to connect to the cluster.</td>
    <td>The username must be 0 to 128 characters in length.</td>
  </tr>
  <tr>
    <td>maintain_end_time</td>
    <td>The end time of the instance maintenance window.</td>
    <td>Specify the time in the HH:mmZ format, such as 02:00Z. The time must be in UTC.</td>
  </tr>
  <tr>
    <td>core_instance_type</td>
    <td>The core node specifications.</td>
    <td>For more information, visitNode specifications.</td>
  </tr>
  <tr>
    <td>master_instance_type</td>
    <td>The master node specifications.</td>
    <td>For more information, visit<br>Node specifications .</td>
  </tr>
  <tr>
    <td>engine_version</td>
    <td>The database engine version of the cluster.</td>
    <td>• Valid values when the engine type is set to hbase: 1.1 and 2.0.<br>• Valid value when the engine type is set to hbaseue: 2.0.<br>• Valid value when the engine type is set to bds: 1.0.</td>
  </tr>
  <tr>
    <td>name</td>
    <td>The name of the ApsaraDB for HBase cluster.</td>
    <td>The name must be 2 to 128 characters in length and can contain letters, digits, periods (.), underscores (_), and hyphens (-).</td>
  </tr>
  <tr>
    <td>deletion_protection</td>
    <td>Specifies whether to enable deletion protection for the cluster.</td>
    <td>A value of true specifies to enable deletion protection. A value of false specifies to disable deletion protection. If you want to delete a cluster, you must set this parameter to false.</td>
  </tr>
  <tr>
    <td>core_disk_type</td>
    <td>The disk type.</td>
    <td>Valid values: cloud_efficiency, cloud_ssd, local_hdd_pro, and local_ssd_pro. When the engine type is set to bds, you do not need to specify the disk type.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/7d6c26fa2dc66434d726cb2064a143ae.webp)

<table>
  <tr>
    <td>maintain_start_time</td>
    <td>The start time of the instance maintenance window.</td>
    <td>Specify the time in the HH:mmZ format, such as 02:00Z. The time must be in UTC.</td>
  </tr>
  <tr>
    <td>tags</td>
    <td>The tags to assign to resources.</td>
    <td>N/A</td>
  </tr>
  <tr>
    <td>core_disk_size</td>
    <td>The disk size of a core node.</td>
    <td>Unit: GB.</td>
  </tr>
  <tr>
    <td>ip_white</td>
    <td>The IP address whitelist.</td>
    <td>If you add 127.0.0.1 to the whitelist, no IP addresses are allowed to access the cluster. If you add CIDR blocks such as 192.168.0.0/24 to the whitelist, all IP addresses that are in the 192.168.0.X format are allowed to access the cluster. Separate multiple IP addresses with commas (,).</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/4ecaaa5ad848fbc0861b26bfde3bed39.webp)

<a id="section-2-34"></a>

## 2.34. Create a Simple Log Service project

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/5faddad3e2231497c15415a2779f671f.webp)

<table>
  <tr>
    <td>name</td>
    <td>The name of the Simple Log Service project.</td>
    <td>1. The name can contain lowercase letters, digits, and hyphens (-).<br>2. The name must start and end with a lowercase letter or a digit.<br>3. The name must be 3 to 63 characters in length.</td>
  </tr>
  <tr>
    <td>description</td>
    <td>The description of the Simple Log Service project.</td>
    <td>The description cannot contain angle brackets &lt;&gt;, apostrophes ('), backslashes (\), double quotation marks ("), or double backslashes (\\). It can be up to 64 characters in length.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/fb78592554d57aeffa29ddee6b984008.webp)

<a id="section-2-35"></a>

## 2.35. Create an ApsaraDB for MongoDB instance

![](en-terraform-user-guide-v3.18.3-20241115.assets/8f917f8832a70cfe179d43ac4fd1cfef.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/ba0a62ee9ece6bc732ef41490cbb865e.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |
| access_key | Your AccessKey ID. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID. |
| secret_key | Your AccessKey secret. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/96d3279eebc257fe8c81a7317bc759ca.webp)

<table>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>engine_version</td>
    <td>The database engine version.</td>
    <td>Valid values:<br>• 6.0<br>• 5.0<br>• 4.4<br>• 4.2<br>• 4.0</td>
  </tr>
  <tr>
    <td>db_instance_storage</td>
    <td>The instance storage capacity.</td>
    <td>Unit: GB.<br>Valid values: 10 to 3000. The value must be a multiple of 10.</td>
  </tr>
  <tr>
    <td>db_instance_class</td>
    <td>The instance type.</td>
    <td>For more information about specific instance specifications, see the following topics:<br>Replica set instance types<br>Sharded cluster instance types</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/2277519a794039ca80af86ce54966c99.webp)

<table>
  <tr>
    <td>name</td>
    <td>The name of the instance.</td>
    <td>The name must be 2 to 256 characters in length.</td>
  </tr>
  <tr>
    <td>account_password</td>
    <td>The password of the root account.</td>
    <td>The password must meet the following requirements:<br>• The password must contain at least three of the following character types: uppercase letters, lowercase letters, digits, and special characters.<br>• Special characters include ! # $ % ^ &amp; * ( ) _ + - =<br>• The password must be 8 to 32 characters in length.</td>
  </tr>
  <tr>
    <td>security_ip_list</td>
    <td>The IP address whitelist of the instance.</td>
    <td>Separate multiple IP addresses with commas (,). Ensure that each IP address is unique in a whitelist. The following types of values are supported:<br>• 0.0.0.0/0<br>• IP addresses, such as 10.23.12.24.<br>• CIDR blocks, such as 10.23.12.0/24. In this case, 24 indicates that the prefix of each IP address is 24-bit long. You can replace 24 with a value within the range of 1 to 32.</td>
  </tr>
  <tr>
    <td>backup_period</td>
    <td>The day of a week on which to back up data of the ApsaraDB for MongoDB instance.</td>
    <td>This parameter is required if backup_time is specified. Valid values:<br>Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, and Sunday.</td>
  </tr>
  <tr>
    <td>backup_time</td>
    <td>The backup window of the ApsaraDB for MongoDB instance.</td>
    <td>This parameter is required if backup_period is specified.Specify the window in the HH:mmZ-HH:mmZ format. Set the time interval to 1 hour. If this parameter is not specified, the system returns a default value, such as 23:00Z-24:00Z.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/e65377b92fd427563541642b47906226.webp)

<table>
  <tr>
    <td>SSL_action</td>
    <td>The operation on the SSL feature.</td>
    <td>Valid values:<br>• Open: enables SSL encryption.<br>• Close: disables SSL encryption.<br>• Update: updates the SSL certificate.</td>
  </tr>
  <tr>
    <td>shard_list</td>
    <td>The number of available shard nodes.</td>
    <td>Valid values: 2 to 32.</td>
  </tr>
  <tr>
    <td>node_class</td>
    <td>The node type.</td>
    <td>For more information about the specifications of shard or mongos nodes, see the following topics:<br>Replica set instance types<br>Sharded cluster instance types</td>
  </tr>
  <tr>
    <td>node_storage</td>
    <td>The storage capacity of a node.</td>
    <td>Valid values: 10 to 1000.</td>
  </tr>
  <tr>
    <td>mongo_lis</td>
    <td>The number of available mongos nodes.</td>
    <td>Valid values: 2 to 32.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/36a803ff59a1c529bd52f5935e3ff5bd.webp)

<a id="section-2-36"></a>

## 2.36. Create NAS resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/5d84813d47a6dbf77d3f961da748e0c0.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/75aaa0632e585036c0e8e06ffa139e46.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of ASAPI.</td>
    <td>1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/22831eaa1288beef3ee355be1910f00d.webp)

<table>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>access_group_name</td>
    <td>The name of the permission group.</td>
    <td>The name must be 3 to 64 characters in length and can contain letters, digits, and hyphens (-).</td>
  </tr>
  <tr>
    <td>access_group_type</td>
    <td>The type of the permission group.</td>
    <td>Valid values: Vpc and Classic.</td>
  </tr>
  <tr>
    <td>source_cidr_ip</td>
    <td>The IP address or CIDR block of the authorized object.</td>
    <td>You can specify only a single IP address or CIDR block, such as 10.10.1.123 or 192.168.3.0/24.</td>
  </tr>
  <tr>
    <td>rw_access_type</td>
    <td>The read/write permission type.</td>
    <td>Valid values: RDWR and RDONLY. Default value: RDWR.</td>
  </tr>
  <tr>
    <td>user_access_type</td>
    <td>The type of access permissions for different types of users.</td>
    <td>Valid values: no_squash, root_squash, and all_squash.Default value: no_squash.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/7734d35615f998a96371129e46601979.webp)

<table>
  <tr>
    <td>priority</td>
    <td>The priority.</td>
    <td>Valid values: 1 to 100. Default value: 1.</td>
  </tr>
  <tr>
    <td>protocol_type</td>
    <td>The protocol type of the file system.</td>
    <td>Valid values: NFS and SMB. The value SMB is available when file_system_type is set to standard.</td>
  </tr>
  <tr>
    <td>storage_type</td>
    <td>The storage type of the file system.</td>
    <td>Valid values:<br>Performance: This value is available when file_system_type is set to standard.<br>Capacity: This value is available when file_system_type is set to standard.<br>standard: This value is available when file_system_type is set to extreme.<br>advance: This value is available when file_system_type is set to extreme.</td>
  </tr>
  <tr>
    <td>file_system_type</td>
    <td>The type of the file system.</td>
    <td>Valid values: standard and extreme. Default value: standard. Note that extreme is available only for file systems in virtual private clouds (VPCs).</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/e7db22266e342a9b11ddbf7fe1b67811.webp)

<a id="section-2-37"></a>

## 2.37. Create OOS resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/06bdd9e794e439b31b87b2876a7c72cc.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/5ecc89311e3bd53965d6668bd4588cbd.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/96b05da02043c60737ae63749b0d10f6.webp)

<table>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/fa2ae9b1405fa5ea68ed0ec62d3cfce5.webp)

<table>
  <tr>
    <td>Description</td>
    <td>The description of the OOS execution.</td>
    <td>The description can be up to 200 characters in length.</td>
  </tr>
  <tr>
    <td>Parameters</td>
    <td>The parameters required by the template.</td>
    <td>Default value: {}.</td>
  </tr>
  <tr>
    <td>template_name</td>
    <td>The name of the template.</td>
    <td>The name can be up to 128 characters in length, and can contain letters, digits, hyphens (-), and underscores (_). It cannot start with ALIYUN, ACS, ALIBABA, or ALICLOUD.</td>
  </tr>
  <tr>
    <td>version_name</td>
    <td>The name of the template version.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>tags</td>
    <td>The tags to assign to the resources.</td>
    <td>Specify a custom value.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/87ebe1ea01d417ea8175df711c8d22d9.webp)

<a id="section-2-38"></a>

## 2.38. Create Quick BI resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/9a976831eb2eaf8849327f3ec235f212.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/7cc1c6a2b004b2dfff7b462d8594dfd6.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of ASAPI.</td>
    <td>1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/e605d4e57fd5dda8496049e5548a1f29.webp)

<table>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>account_name</td>
    <td>The name of the Apsara Stack tenant account.</td>
    <td>The name cannot contain colons (:).</td>
  </tr>
  <tr>
    <td>admin_user</td>
    <td>Specifies whether the user is an administrator.</td>
    <td>Valid values: true and false.</td>
  </tr>
  <tr>
    <td>auth_admin_user</td>
    <td>Specifies whether the user is a permission administrator.</td>
    <td>Valid values: true and false.</td>
  </tr>
  <tr>
    <td>nick_name</td>
    <td>The alias of the user.</td>
    <td>The alias can contain only letters, digits, underscores (_), hyphens (-), forward slashes (/), backslashes (\), vertical bars (|), parentheses (), and brackets [].The alias can contain a maximum of 50 characters in length.</td>
  </tr>
  <tr>
    <td>user_type</td>
    <td>The type of the user.</td>
    <td>Valid values: Analyst, Developer, and Visitor.</td>
  </tr>
  <tr>
    <td>user_group_name</td>
    <td>The name of the user group.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>user_group_description</td>
    <td>The description of the user group.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>parent_user_group_id</td>
    <td>The ID of the parent user group.</td>
    <td>You can add new user groups to this group. If you enter -1, a newly created user group is added to the root directory.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/0f8027b114301b31c825ec495c755554.webp)

<table>
  <tr>
    <td>workspace_name</td>
    <td>The name of the workspace.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>workspace_desc</td>
    <td>The description of the workspace.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>use_comment</td>
    <td>Specifies whether to use table comments.</td>
    <td>Valid values: true and false.</td>
  </tr>
  <tr>
    <td>allow_share</td>
    <td>Specifies whether the work can be shared.</td>
    <td>Valid values: true and false.</td>
  </tr>
  <tr>
    <td>allow_publish</td>
    <td>Specifies whether the work can be published.</td>
    <td>Valid values: true and false.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/82cd23d0fab3a430ef1195a732f289ed.webp)

<a id="section-2-39"></a>

## 2.39. Create ROS resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/9ce8aebe026e3f4ff8b86c97ab6ac6c7.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/624cb019bc7b22458300dc112d919e74.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of ASAPI.</td>
    <td>1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/c4d1c8baed5d41b44c1f8432328af7fd.webp)

<table>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>stack_name</td>
    <td>The name of the stack.</td>
    <td>The name can be up to 255 characters in length and can contain digits, letters, hyphens (-), and underscores (_). It must start with a digit or letter.</td>
  </tr>
  <tr>
    <td>template_body</td>
    <td>The template body.</td>
    <td>The template body must be 1 to 524,288 bytes in length. If the template body is longer than required, we recommend that you add parameters to the HTTP POST request body to avoid request failures due to excessive length of URLs.</td>
  </tr>
  <tr>
    <td>stack_policy_body</td>
    <td>The stack policy body.</td>
    <td>The stack policy body must be 1 to 16,384 bytes in length.</td>
  </tr>
  <tr>
    <td>template_name</td>
    <td>The name of the template.</td>
    <td>The name can be up to 255 characters in length, and can contain digits, letters, hyphens (-), and underscores (_). It must start with a digit or letter.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/f6cb19f38b37c5267695a11f6439e4b8.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/b90f929ab52da703693fbbc43e5bd530.webp)

<a id="section-2-40"></a>

## 2.40. Create a KVStore for Redis instance

![](en-terraform-user-guide-v3.18.3-20241115.assets/38b6b5030053535cfabc76d9999e08a9.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |
| access_key | Your AccessKey ID. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID. |
| secret_key | Your AccessKey secret. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/7b36d513a75503f6a8ac39bdf00538b9.webp)

<table>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>instance_class</td>
    <td>The instance type.</td>
    <td>You can query the instance type from the alibabacloudstack_kvstore_inst ance_classes data source.</td>
  </tr>
  <tr>
    <td>instance_name</td>
    <td>The name of the instance.</td>
    <td>The name must be 2 to 128 characters in length and can contain letters, digits, underscores (_), and hyphens (-). It must start with a letter.</td>
  </tr>
  <tr>
    <td>private_ip</td>
    <td>The private IP address.</td>
    <td>Specify a value such as 172.16.0.***.</td>
  </tr>
  <tr>
    <td>security_ips</td>
    <td>The IP address whitelist.</td>
    <td>To allow all IP addresses to access the instance, add 0.0.0.0/0 to the whitelist. To block access from all IP addresses, add 127.0.0.1 to the whitelist. Separate multiple IP addresses with commas (,).</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/467cf57c57be367696583ef0f2d38a73.webp)

<table>
  <tr>
    <td>instance_type</td>
    <td>The instance category.</td>
    <td>Valid values: Redis and Memcache. Default value: Redis.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/7249e1e0c2bdeaaa527b0e0ca7ce9ad9.webp)

<a id="section-2-41"></a>

## 2.41. Create Tablestore resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/04d8c4a3b9a0460d9221c6b1162aa104.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/7feb7b1dedd7309a9a076d8e5e3d45e6.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| domain | The domain name of ASAPI. | 1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint. |
| access_key | Your AccessKey ID. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID. |
| secret_key | Your AccessKey secret. | 1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/36d9dfb304d1c629522ba48756a3e85c.webp)

<table>
  <tr>
    <td>region</td>
    <td>The region.</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>name</td>
    <td>The name of the Tablestore instance.</td>
    <td>The name must be 3 to 16 characters in length and can contain letters, digits, and hyphens (-). It can start with a letter and cannot start with case-insensitive string ali or ots.</td>
  </tr>
  <tr>
    <td>description</td>
    <td>The description of the instance.</td>
    <td>The description must be 0 to 256 characters in length.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/fd63669804aa4818a4255c4b76205e3f.webp)

<table>
  <tr>
    <td>accessed_by</td>
    <td>The networks over which you can access the instance.</td>
    <td>Valid values:<br>Any: allows access to the instance over any network.<br>Vpc: allows access to the instance only over the VPC bound to the instance.<br>ConsoleOrVpc: allows access to the instance over the KVStore for Redis console or the VPC bound to the instance.</td>
  </tr>
  <tr>
    <td>tags</td>
    <td>The tags to assign to the instance.</td>
    <td>Specify a custom value.</td>
  </tr>
  <tr>
    <td>vpc_name</td>
    <td>The name of the VPC.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>. In the left-side navigation pane, click Virtual Private Clouds. Then, obtain the name of the VPC.</td>
  </tr>
  <tr>
    <td>vswitch_id</td>
    <td>The ID of the vSwitch.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, choose <strong>Products &gt; Virtual</strong> <strong>Private Cloud</strong>.<br>2. In the left-side navigation pane, click <strong>VSwitches</strong>.Obtain the vSwitch ID from the VSwitches page.</td>
  </tr>
  <tr>
    <td>table_name</td>
    <td>The name of the table in the Tablestore instance.</td>
    <td>1. The name can contain only letters, digits, and underscores (_).<br>2. The name must start with a letter or underscore (_).<br>The name must be 1 to 255 characters in length.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/b1fcd2fb8c486d9bb19a4a053259f912.webp)

<table>
  <tr>
    <td>primary_key</td>
    <td>The primary keys of the table.</td>
    <td>A table can have a maximum of four primary keys.<br>1. A primary key can contain only letters, digits, and underscores (_).<br>2. A primary key must start with a letter or underscore (_).<br>3. A primary key must be 1 to 255 characters in length.<br>4. A primary key cannot be modified after it is created.</td>
  </tr>
  <tr>
    <td>primary_key (type)</td>
    <td>The type of the primary key.</td>
    <td>Valid values: Integer, String, and Binary.</td>
  </tr>
  <tr>
    <td>time_to_live</td>
    <td>The time-to-live (TTL) of data.</td>
    <td>The TTL must be at least 86,400 seconds (one day) or -1.A value of -1 specifies that the data never expires.</td>
  </tr>
  <tr>
    <td>max_version</td>
    <td>The maximum number of versions of data.</td>
    <td>Data versions cannot be 0.</td>
  </tr>
  <tr>
    <td>deviation_cell_version_in_sec</td>
    <td>The maximum version offset of data.</td>
    <td>Valid values: 1 to 9223372036854775807.Default value: 86400.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/7ed58bf914458d3bb6c8f8b65d0f7a5e.webp)

<a id="section-2-42"></a>

## 2.42. Create VPN Gateway resources

![](en-terraform-user-guide-v3.18.3-20241115.assets/af0af4ed03e7ef2af00717eb17665f66.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |

![](en-terraform-user-guide-v3.18.3-20241115.assets/5d0c702c79f9d0ebc0e9d01f4f8892b4.webp)

<table>
  <tr>
    <td>domain</td>
    <td>The domain name of ASAPI.</td>
    <td>1. Log on to the Apsara Infrastructure Management console 1.0.<br>2. In the top navigation bar, choose <strong>Reports</strong> &gt; System Reports.<br>3. Click <strong>Registration Vars of</strong> <strong>Services</strong> in the Report column.<br>4. Click the filter icon next to Service, enter asapi, and then click Apply Filter.<br>5. Right-click the item in the Service Registration column corresponding to asapi, and select Show More.<br>6. View the details to obtain the value of asapi.gateway.endpoint.</td>
  </tr>
  <tr>
    <td>access_key</td>
    <td>Your AccessKey ID.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey ID.</td>
  </tr>
  <tr>
    <td>secret_key</td>
    <td>Your AccessKey secret.</td>
    <td>1. Use your account username and password to log on to the Apsara Uni-manager Management Console.<br>2. Click the cloud logo in the upper-right corner of the homepage and select User Information.<br>3. Obtain your AccessKey secret.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/9e423a1166ae0916a9148c681ab482c8.webp)

<table>
  <tr>
    <td>region</td>
    <td>Region</td>
    <td>1. Log on to the Apsara Uni-manager Management Console.<br>2. In the top navigation bar, click Enterprise. Then, choose <strong>Resources &gt;</strong> <strong>Regions</strong> in the left-side navigation pane.<br>3. Select the organization that you want to manage and obtain the name of the region.</td>
  </tr>
  <tr>
    <td>proxy</td>
    <td>The proxy endpoint that is used to access the environment.</td>
    <td>If you do not need to use a proxy endpoint to access the environment, you do not need to configure this parameter.</td>
  </tr>
  <tr>
    <td>insecure</td>
    <td>Specifies whether to ignore insecure HTTPS certificates.</td>
    <td>Valid values: true and false. A value of true specifies to ignore insecure HTTPS certificates.</td>
  </tr>
  <tr>
    <td>resource_group_set_name</td>
    <td>The name of the resource set.</td>
    <td>1. In the top navigation bar of the Apsara Uni-manager Management Console, click <strong>Enterprise</strong>.<br>2. Choose Resources &gt; Resource Sets in the left-side navigation pane, and obtain the name of the resource set.</td>
  </tr>
  <tr>
    <td>name</td>
    <td>The name of the VPN gateway.</td>
    <td>The name must be 2 to 100 characters in length and can contain letters, digits, underscores (_), and hyphens (-). It must start with a letter and cannot start with http:// or https://.</td>
  </tr>
  <tr>
    <td>instance_charge_type</td>
    <td>The billing method.</td>
    <td>Valid values: PostPaid and PrePaid.<br>Default value: PostPaid.</td>
  </tr>
  <tr>
    <td>bandwidth</td>
    <td>The bandwidth.</td>
    <td>Valid values: 5, 10, 20, 50, and 100.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/7b584fd89c263e49de189fa6dafdf793.webp)

<table>
  <tr>
    <td>enable_ssl</td>
    <td>Specifies whether to enable SSL-VPN.</td>
    <td>Valid values: true and false.Default value: false.</td>
  </tr>
  <tr>
    <td>ip_address</td>
    <td>The IP address of the customer gateway.</td>
    <td>Specify a custom value.</td>
  </tr>
</table>

<a id="section-2-43"></a>

## 2.43. Create an Apsara Stack disk

![](en-terraform-user-guide-v3.18.3-20241115.assets/7c55303d490d658f61a6d03611388cc0.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/a4ee50edd88a2f13b8b784e86bc8d658.webp)

![](en-terraform-user-guide-v3.18.3-20241115.assets/69843a8ff6effc8d21119a05f3834407.webp)

| Parameter | Description | Method to obtain the parameter value |
| --- | --- | --- |
| availability_zone | The zone. | This parameter specifies the zone in which a disk is created. |

![](en-terraform-user-guide-v3.18.3-20241115.assets/afbe3bd1996e557d806865a7e78b4a8f.webp)

<table>
  <tr>
    <td>name</td>
    <td>The name of the disk.</td>
    <td>The name can be 2 to 128 characters in length and can contain only letters, hyphens (-), periods (.), and underscores (_). It cannot start or end with a hyphen (-), http://, or https://.Default value: null.</td>
  </tr>
  <tr>
    <td>category</td>
    <td>The category of the disk.</td>
    <td>Valid values: cloud, cloud_efficiency, and cloud_ssd.Default value: cloud.</td>
  </tr>
  <tr>
    <td>size</td>
    <td>The size of the disk.</td>
    <td>When you resize a disk, the new size must be greater than the original size. Otherwise, the error message "InvalidDiskSize.TooSmall" is returned.</td>
  </tr>
  <tr>
    <td>encrypted</td>
    <td>Specifies whether to encrypt a disk.</td>
    <td>If you set this parameter to true, the disk is encrypted.</td>
  </tr>
  <tr>
    <td>disk_count</td>
    <td>The number of disks.</td>
    <td>This parameter specifies the number of disks that you want to start.</td>
  </tr>
  <tr>
    <td>tag</td>
    <td>The tag of the disk.</td>
    <td>This parameter is used to tag a specific ECS data disk. The name is automatically incorporated into the tag.</td>
  </tr>
</table>

![](en-terraform-user-guide-v3.18.3-20241115.assets/e09841bfeb6f1d43dd5a7d7759315a76.webp)
