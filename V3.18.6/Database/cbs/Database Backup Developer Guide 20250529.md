Alibaba Cloud  
Apsara Stack  
Database Backup  
Developer Guide  
Product Version: V3.18.6  
Document Version: 20250529

**Table of Contents**

- [1.What is DBS?](#section-1)
- [2.Technical advantages](#section-2)
- [3.Feature matrix](#section-3)
    - [3.1. MySQL](#section-3-1)
    - [3.2. PPAS](#section-3-2)
    - [3.3. Redis](#section-3-3)
    - [3.4. PostgreSQL](#section-3-4)
    - [3.5. Oracle](#section-3-5)
    - [3.6. PolarDB-X](#section-3-6)
    - [3.7. MongoDB](#section-3-7)
- [4.Features](#section-4)
    - [4.1. Configure the backup source and destination](#section-4-1)
    - [4.2. Configure backup objects](#section-4-2)
    - [4.3. Configure the backup time](#section-4-3)
    - [4.4. Configure the lifecycle](#section-4-4)
    - [4.5. Backup Schedules page](#section-4-5)
    - [4.6. Full Data page](#section-4-6)
    - [4.7. Transaction Log Backup page](#section-4-7)
    - [4.8. Configure the restoration time](#section-4-8)
    - [4.9. Configure the objects to restore](#section-4-9)
    - [4.10. Restore tasks](#section-4-10)
    - [4.11. Download backup sets](#section-4-11)

<a id="section-1"></a>

# 1.What is DBS?

Database Backup (DBS) is a cost-effective backup service for continuous data protection. The service offers strong protection for data stored in multiple environments, such as on-premises data centers, cloud offerings from other vendors, hybrid clouds, and Alibaba Cloud public cloud.

<a id="section-2"></a>

# 2.Technical advantages

Database Backup (DBS) supports databases that are deployed in various environments. By using Express Connect and VPN Gateway, it supports the backup of databases deployed in on-premises data centers, Elastic Compute Service (ECS) instances, and third-party cloud environments. DBS also allows you to back up ApsaraDB RDS databases at a different location. You can use DBS to perform full data backup, incremental data backup, and data restoration with a few clicks.

**Cost-effectiveness**

- The pay-as-you-go billing method ensures 100% resource utilization and avoids a large amount of upfront asset investment.

- Cold data is separated from hot data for tiered storage. This is suitable for the long-term archiving of backup data.

- DBS reduces storage costs by using compression, compact backup, and incremental backup.

- Investments in hiring maintenance personnel or hosting databases are not required.

**High security**

- DBS uses Secure Sockets Layer (SSL) and AES-256 encryption to ensure security during the transmission and storage of backup data.

- Resources are isolated between different users, and geo-disaster recovery is supported.

- DBS provides a variety of authentication and authorization methods, such as whitelist configuration, hotlink protection, and Resource Access Management (RAM) user management.

- DBS allows you to verify the validity of backups at any time, and notifies you of the task status.

- Custom authentication is supported.

**Ease of use**

- The process of activating DBS to configuring a backup schedule and running a backup task takes only five minutes.

- Fine-grained backup is supported. You can back up data at different granularities based on your business requirements, including an entire instance, a single database, multiple tables, or a single table.

- DBS supports global rules for the lifecycle management of backup data. You can customize rules to automatically dump, clean up, duplicate, and distribute backup data.

- DBS provides a web-based GUI for you to perform backup and restore operations with ease.

**High performance**

- DBS captures in-memory logs in real time and achieves per-second recovery point objective (RPO). DBS allows you to restore backup data to any point in time.

- DBS allows you to select a single table as the object to restore. This greatly reduces the recovery time objective (RTO).

- DBS supports streaming backup. Data is not flushed to disks. The entire backup window is unlocked. The backup speed can be adjusted based on the concurrency configuration.

- DBS uses a multi-line Border Gateway Protocol (BGP) backbone network that has no bandwidth limits. This allows a large number of users to perform backup and restore operations simultaneously.

**High reliability**

- DBS uses Apsara Distributed File System to provide a distributed storage service with high reliability.

- DBS uses a redundant storage design to deliver a designed durability of at least 99.999999999%.

- During the backup process, data integrity is verified in real time.

- Tested by a large number of users, DBS is able to efficiently detect and fix vulnerabilities.

<a id="section-3"></a>

# 3.Feature matrix

<a id="section-3-1"></a>

## 3.1. MySQL

**Logical backup**

| MySQL version | Full backup | Incremental backup | Data restoration | Backup set download |
| --- | --- | --- | --- | --- |
| RDS MySQL 5.6 | Supported | Supported | Supported | Supported |
| RDS MySQL 5.7 | Supported | Supported | Supported | Supported |

| MySQL version | Full backup | Data restoration | Backup set download |
| --- | --- | --- | --- |
| RDS MySQL 8.0 | Supported | Supported | Supported |

<a id="section-3-2"></a>

## 3.2. PPAS

**Logical backup**

| PPAS version | Full backup | Incremental backup | Data restoration |
| --- | --- | --- | --- |
| 9.3 | Supported | Not supported | Supported |

<a id="section-3-3"></a>

## 3.3. Redis

**Logical backup**

| Redis version | Full backup | Incremental backup | Data restoration |
| --- | --- | --- | --- |
| ApsaraDB for Redis 4.0 | Supported | Not supported | Supported |

<a id="section-3-4"></a>

## 3.4. PostgreSQL

**Logical backup**

| PostgreSQL version | Full backup | Incremental backup | Data restoration |
| --- | --- | --- | --- |
| Self-managed PostgreSQL 9.4 | Supported | Not supported | Supported |
| Self-managed PostgreSQL 10 | Supported | Not supported | Supported |
| RDS PostgreSQL 9.4 | Supported | Not supported | Supported |
| RDS PostgreSQL 10 | Supported | Not supported | Supported |

<a id="section-3-5"></a>

## 3.5. Oracle

**Physical backup**

| Oracle version | Full backup | Incremental backup | Data restoration |
| --- | --- | --- | --- |
| 10g | Supported | Not supported | Supported |
| 11g | Supported | Not supported | Supported |
| 12c | Supported | Not supported | Supported |
| 18c | Supported | Not supported | Supported |
| 19c | Supported | Not supported | Supported |

<a id="section-3-6"></a>

## 3.6. PolarDB-X

**Logical backup**

| PolarDB-X version | Full backup | Incremental backup | Data restoration | Backup set download |
| --- | --- | --- | --- | --- |
| PolarDB-X 1.0 | Supported | Not supported | Supported | Supported |

<a id="section-3-7"></a>

## 3.7. MongoDB

**Logical backup**

| MongoDB version | Full backup | Incremental backup | Data restoration | Backup set download |
| --- | --- | --- | --- | --- |
| Replica set instances that run MongoDB 4.0 | Supported | Supported | Supported | Supported |

<a id="section-4"></a>

# 4.Features

<a id="section-4-1"></a>

## 4.1. Configure the backup source and destination

**Database location**

- Self-managed databases that are connected by using public IP addresses and port numbers

- Self-managed databases that are hosted on Elastic Compute Service (ECS) instances

- On-premises databases that are connected to Alibaba Cloud by using Express Connect

- Databases on ApsaraDB RDS instances

**Objective**

Service logic: the DBS built-in storage and the purchased backup schedules reside in the same region.

<a id="section-4-2"></a>

## 4.2. Configure backup objects

**Databases and tables**

- An entire instance

- Multiple databases

- A single database

- Multiple tables

- A single table

**Others**

- Views

- Stored procedures

- Triggers

<a id="section-4-3"></a>

## 4.3. Configure the backup time

**Full backup cycle**

We recommend that you perform a full backup at least once a week.

**Incremental log backup**

We recommend that you enable the incremental log backup feature.

<a id="section-4-4"></a>

## 4.4. Configure the lifecycle

**Retention period**

Backup sets can be retained for up to two years and are automatically deleted upon expiration.

**Transit to Infrequent Access (IA) After**

The number of days before you transit the storage class from Standard to IA.

**Transit to Archive After**

The number of days before you transit the storage class from IA or Standard to Archive.

<a id="section-4-5"></a>

## 4.5. Backup Schedules page

The **Backup Schedules** page display the configuration details of backup schedules and allows you to modify the backup schedule configurations.

<a id="section-4-6"></a>

## 4.6. Full Data page

The **Full Data** page displays all backup sets of backup schedules. You can click the ID of a full backup set to go to the details page.

<a id="section-4-7"></a>

## 4.7. Transaction Log Backup page

The **Transaction Log Backup** page displays all the incremental backup sets of backup schedules. You can click the ID of an incremental backup set to go to the details page.

<a id="section-4-8"></a>

## 4.8. Configure the restoration time

Database Backup (DBS) provides a calendar and a timeline so that you can select a point in time to which data is restored.

<a id="section-4-9"></a>

## 4.9. Configure the objects to restore

Database Backup (DBS) provides the schema mapping feature. You can select a database and modify the name of the database schema.

DBS also provides the following solutions to schema name conflicts:

- **Fail When Object with the Same Name Exists**: If an object that uses the same name exists when you run a restore task, the task fails. You must manually specify a different name for the database schema that you want to restore.

  For example, if an object that uses the **DB1.table1** name exists and you select the **Fail When Object with the Same Name Exists** option, the restoration fails. The database instance that you want to restore has only one object named as **DB1.table1**. In this case, you must manually change the name of the object from **DB1.table1** to another name and re-initiate a DBS restore task.

- **Skip Object with the Same Name**: If an object that uses the same name exists when you run a restore task, the existing object skips the restoration. Other objects that use different names are restored as expected.

  For example, if an object that uses the **DB1.table1** name exists and you select the **Skip Object with the Same Name** option, the restoration of the existing **DB1.table1** object fails. The database instance that you want to restore has only one object named as **DB1.table1**. In this case, you must manually change the name of the object from **DB1.table1** to another name and re-initiate a DBS restore task.

- **Rename Object with the Same Name**: If an object that uses the same name exists when you run a restore task, the object that you want to restore will still use the name. The existing object that uses the same name remains unchanged. We recommend that you do not use this option.

  For example, if an object that uses the **DB1.table1** name exists and you select the **Rename Object with the Same Name** option, the restore task succeeds. The database instance that you want to restore has the existing object **DB1.table1** and a new object <strong>DB1</strong><em><strong>xxx</strong></em><strong>.table1</strong><em><strong>xxx</strong></em>. You must specify ***x*** based on the naming rule.

  > **Important**
  >
  > If you select the **Rename Object with the Same Name** option, the incremental data may fail to be restored. If you encounter the issue, we recommend that you manually modify the name of the object that uses the same name on the destination database instance.

<a id="section-4-10"></a>

## 4.10. Restore tasks

**Restore process**

- Schema restoration before full data restoration

- Full data restoration

- Schema restoration after full data restoration

- Incremental log restoration

**Abnormal tasks**

- Exception causes are displayed.

- You can restart abnormal tasks.

<a id="section-4-11"></a>

## 4.11. Download backup sets

You can download specific backup sets.
