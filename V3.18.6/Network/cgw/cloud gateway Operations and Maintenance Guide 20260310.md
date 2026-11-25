Alibaba Cloud  
Apsara Stack  
cloud gateway  
Operations and Maintenance  
Guide  
Product Version: V3.18.6  
Document Version: 20260310

**Table of Contents**

- [1.Log on to the Apsara Uni-manager Operations Console](#section-1)
- [2.Basic network](#section-2)
    - [2.1. HPN management](#section-2-1)
        - [2.1.1. HPN network elements](#section-2-1-1)
        - [2.1.2. RDMA network interface O&M](#section-2-1-2)
        - [2.1.3. HPN performance analysis](#section-2-1-3)
        - [2.1.4. HPN instant diagnostics](#section-2-1-4)
    - [2.2. CPN](#section-2-2)
        - [2.2.1. CPN diagnosis](#section-2-2-1)
        - [2.2.2. CPN performance analysis](#section-2-2-2)
        - [2.2.3. CPN alert center](#section-2-2-3)
        - [2.2.4. CPN access gateways](#section-2-2-4)
            - [2.2.4.1. Manage RDMA devices](#section-2-2-4-1)
            - [2.2.4.2. Manage RDMA device policies](#section-2-2-4-2)
            - [2.2.4.3. Manage policies for the RDMA device interface](#section-2-2-4-3)
        - [2.2.5. RDMA NIC O&M](#section-2-2-5)
        - [2.2.6. CPN management](#section-2-2-6)
            - [2.2.6.1. CPN topology](#section-2-2-6-1)
            - [2.2.6.2. CPN network element](#section-2-2-6-2)
        - [2.2.7. CPN network monitoring](#section-2-2-7)
            - [2.2.7.1. CPN host monitoring dashboard](#section-2-2-7-1)
            - [2.2.7.2. CPN switch dashboard](#section-2-2-7-2)
            - [2.2.7.3. NAK packet analysis tool](#section-2-2-7-3)
            - [2.2.7.4. High-precision monitoring dashboard](#section-2-2-7-4)
            - [2.2.7.5. High-precision vSwitch monitoring dashboard](#section-2-2-7-5)
            - [2.2.7.6. Job monitoring](#section-2-2-7-6)
            - [2.2.7.7. CPN stream monitoring](#section-2-2-7-7)
    - [2.3. CGW](#section-2-3)
    - [2.4. Computing access gateways](#section-2-4)
- [3.Networking products](#section-3)
    - [3.1. CGW O&M](#section-3-1)
        - [3.1.1. CGW cluster management](#section-3-1-1)
        - [3.1.2. CGW management](#section-3-1-2)
- [4.Traffic visualization](#section-4)
    - [4.1. Visual settings](#section-4-1)

<a id="section-1"></a>

# 1.Log on to the Apsara Uni-manager Operations Console

This topic describes how users such as O&M engineers log on to the Apsara Uni-manager Operations Console.

**Prerequisites**

- The endpoint of the Apsara Uni-manager Operations Console and the username and password that are used to log on to the console are obtained from a deployment engineer or an administrator.

  The endpoint of the Apsara Uni-manager Operations Console is in the following format: *regi on-id*.ops.console.*intranet-domain-id*.

- A web browser is available. We recommend that you use Google Chrome.

**Procedure**

1. Open your browser.

2. In the address bar, enter the endpoint of the Apsara Uni-manager Operations Console. Press the ENTER key.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/a6a399b2786854c9e08e44ae44c5434b.webp)

   > **Note**
   >
   > You can click the current language in the upper-right corner to switch to another language. Simplified Chinese, English, and traditional Chinese are supported.

3. Enter the username and password.

   > **Note**
   >
   > - Obtain the username and password that are used to log on to the Apsara Uni-manager Operations Console from a deployment engineer or an administrator.
   >
   > - If you enter an invalid password for three consecutive times, the system enables the image verification logon feature. If you enter an invalid password for five consecutive times, the account is locked. Contact the administrator to activate the account.

   If this is the first time you log on to the Apsara Uni-manager Operations Console, you must change the password as prompted.

   To enhance security, your password must meet the following requirements:

   - The password contains uppercase and lowercase letters.

   - The password contains digits.

   - The password contains at least one of the following special characters: ! @ # $ %

   - The password is 10 to 20 characters in length.

4. Click **Log In**.

<a id="section-2"></a>

# 2.Basic network

<a id="section-2-1"></a>

## 2.1. HPN management

> **Note**
>
> By default, the HPN Management module is not displayed. To use this module, perform the following operations: Log on to the Apsara Uni-manager Operations Console. In the top navigation bar, choose More > **User Authorities**. In the left-side navigation pane, click **Menu Management**. On the Menu management page, modify the menu settings to display the HPN Management module.

<a id="section-2-1-1"></a>

### 2.1.1. HPN network elements

This topic describes how to view High Performance Network (HPN) network device assets and monitoring and O&M information in the Apsara Uni-manager Operations Console.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **HPN Management** > **HPN Network Elements**.

4. On the HPN Network Element page, configure the **Select IDC** parameter and specify the name of a network element to search for the network element.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/762a0962974737bdb83eea2691bd5138.webp)

5. Click the name of the network element or click **Details** in the **Operation** column of the network element to view the details of the network element.

   - On the details page of the network element, view the basic information about the network element.

     ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/8b2423d22ea7c2b7bdd86d65fe5b7855.webp)

   - On the **Port** tab, view port information.

     Click the name of the port that you want to view or click **View** in the **Details** column of the port to view the port details.

     ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/f1286ee74938ac1c6e77aab269961719.webp)

   - On the **CPU Utilization** tab, view CPU utilization.

     ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/2b6e89e7ed5b1c51e2bca4341e532957.webp)

   - On the **Memory Utilization** tab, view memory usage.

     ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/7b669a3af4e658bb2247ba3f35d84e73.webp)

   - On the **Aggregation Port Management** tab, view the information about aggregation ports.

     Find the aggregation port that you want to view and click **View** in the **Actions** column to view the usage data charts of the aggregation port.

     ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/df176537f643058a804c794df2a03e42.webp)

   - On the **Alert** tab, view the alert information about the network element.

     Find the alert that you want to view and click **View** in the **Alert Details** column to view the alert details.

     ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/fcb42d29d3d3c93c423781bf9d3b947d.webp)

**Delete a network element**

1. On the HPN Network Element page, find the network element that you want to delete and click **Delete** in the **Operation** column.

2. In the message that appears, click **OK**.

   > **Note**
   >
   > Deleted network elements cannot be restored. Proceed with caution.

<a id="section-2-1-2"></a>

### 2.1.2. RDMA network interface O&M

The remote direct memory access (RDMA) network interface O&M feature can regularly check the performance metrics of an RDMA network interface by using performance monitoring. This helps you identify issues at the earliest opportunity, quickly troubleshoot and resolve issues, and ensure network stability and reliability.

**Terms**

**RDMA** is a high-speed network technology used to resolve delays in server-side data processing during network transmission. RDMA directly sends data to the storage area of a computer over the network. During the process, data is quickly transmitted from one system to the memory of a remote system. RDMA implements direct memory access between hosts without affecting the operating system, accelerates data transmission, and reduces CPU load.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **HPN Management** > **RDMA Card O&M**.

4. In the upper-right corner of the RDMA Card O&M page, select a data source from the **Data Source** drop-down list. The following data sources are available:

   - **Bare Metal Server (BMS)**

   - **Platform of Artificial Intelligence (PAI)**

   - **Cloud Parallel File System (CPFS)**

   - **Super Computing Cluster (SCC)**

   > **Note**
   >
   > - If you select **PAI**, you must configure the **Cluster** and **ViewType** parameters.
   >
   > - If you select **CPFS** or **SCC**, you must configure the **Cluster** parameter.

5. On the **Cluster** tab, view the monitoring data of a cluster.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/9ac6506c97fcc78ee73e53b466c8b018.webp)

   | Section | Description |
   | --- | --- |

   <table>
     <tr>
       <td>Average QP</td>
       <td>The average number of queue pairs (QPs) in the RDMA network. If you select PAI as the data source, this metric is not displayed.<br>• If the QPs are insufficient, the communication queue in the RDMA network may be congested, which compromises the efficiency and stability of data transmission.<br>• Excessive QPs may increase the overhead, complexity, and failure rate of the system.<br>Note<br>QP is a key term of the RDMA network. It refers to the communication queue between a pair of endpoints.</td>
     </tr>
     <tr>
       <td>Abnormal Networks</td>
       <td>The number of times that network device or traffic exceptions occur in the RDMA network.</td>
     </tr>
     <tr>
       <td>Average Throughput Sent by RDMA (Mbit/s)</td>
       <td>The average amount of data that is sent by all nodes in the RDMA network per second.</td>
     </tr>
     <tr>
       <td>Average Throughput Received by RDMA (Mbit/s)</td>
       <td>The average amount of data that is received by all nodes in the RDMA network per second.</td>
     </tr>
     <tr>
       <td>Monitoring Chart</td>
       <td>i. On the right side of the monitoring chart, specify a time range to view the corresponding monitoring data.<br>ii. In the <strong>Throughput Dashboard</strong> section, view the data of the RDMA_TX_BYTES and RDMA_RX_BYTES metrics within the specified time range.<br>• The RDMA_TX_BYTES metric specifies the number of bytes that are sent over the RDMA network per second.<br>• The RDMA_RX_BYTES metric specifies the number of bytes that are received over the RDMA network per second.iii. In the <strong>Display the Basic Data of RDMA Network</strong> section, view the data of the following metrics within the specified time range.<br>• The <strong>RDMA_IGNORE_CNP_AVG</strong> metric specifies the average number of congestion notification packets (CNPs) that are ignored in the RDMA network per second.<br>Note<br>A CNP is used for network congestion control. When network congestion occurs, CNPs are sent to notify the sender to decrease the sending rate to prevent network congestion and packet loss.<br>• The <strong>RDMA_OOB_AVG</strong> metric specifies the average number of Out-of-Band (OOB) packets that are processed in the RDMA network per second.<br>Note<br>OOB data is a special type of data transmitted over the RDMA network.<br>• The <strong>RDMA_OOS_AVG</strong> metric specifies the average number of Out-of-Order (OOS) packets that are processed in the RDMA network per second.<br>Note<br>OOS data is a special type of data transmitted over the RDMA network. OOS data is generated when packet loss or delay occurs during data transmission.<br>• The <strong>RDMA_SENT_CNP_AVG</strong> metric specifies the average number of CNPs that are sent over the RDMA network per second.<br>• The <strong>RDMA_HANDLE_CNP_AVG</strong> metric specifies the average number of CNPs that are processed in the RDMA network per second.<br>• The <strong>RDMA_TX_BYTES_AVG</strong> metric specifies the average number of bytes that are sent over the RDMA network per second.<br>• The <strong>RDMA_RX_BYTES_AVG</strong> metric specifies the average number of bytes that are received over the RDMA network per second.</td>
     </tr>
     <tr>
       <td>RDMA Network Overview</td>
       <td>You can view the node information in the following columns: <strong>Node</strong>, <strong>Outbound Throughput</strong>, <strong>Inbound Throughput</strong>, <strong>Network QP</strong>, <strong>CNP</strong> <strong>Processed by Network</strong>, <strong>Out-of-order Data Packets</strong>, and <strong>Network</strong> <strong>Buffer Overflow</strong>.</td>
     </tr>
   </table>

6. On the **Node** tab, view the monitoring data of nodes.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/4607e7f3f874eb5b9b2d7ec7be77e16e.webp)

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>QP in RDMA Network</td>
       <td rowspan="5">The monitoring data of a node in the RDMA network. For more information about these metrics, see the description of them in the previous step.</td>
     </tr>
     <tr>
       <td>Abnormal Networks</td>
     </tr>
     <tr>
       <td>Throughput Sent by RDMA Network (Mbit/s)</td>
     </tr>
     <tr>
       <td>Throughput Received by RDMA Network (Mbit/s)</td>
     </tr>
     <tr>
       <td>Monitoring Chart</td>
     </tr>
   </table>

<a id="section-2-1-3"></a>

### 2.1.3. HPN performance analysis

The Apsara Uni-manager Operations Console provides the High Performance Network (HPN) performance analysis feature. This feature analyzes the maximum load and pressure resistance of the software and hardware by testing the performance of a machine under stress conditions. This helps you identify the pressure resistance limit of the machine and provides data support for O&M personnal to improve network performance.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **HPN Management** > **HPN Performance Analysis**.

4. On the HPN performance analysis page, click **Create a test** to create an analysis task.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/1c0bedfa77eaa8843fc883e6f20fee5d.webp)

   The following table describes the parameter combinations for an analysis task.

   <table>
     <tr>
       <th>Test cluster</th>
       <th>Protocol type</th>
       <th>Test type</th>
       <th>Required parameters</th>
       <th>Traffic model</th>
       <th>Node</th>
     </tr>
     <tr>
       <td rowspan="5">All</td>
       <td rowspan="3">RDMA</td>
       <td rowspan="2">Traffic test</td>
       <td rowspan="2">• Number of QPS tested<br>• Node Port<br>• Test duration (s)<br>• GDR</td>
       <td>MtoN</td>
       <td>• Server<br>• Client</td>
     </tr>
     <tr>
       <td>FullMesh</td>
       <td>• Server</td>
     </tr>
     <tr>
       <td>Latency test</td>
       <td>• Node Port</td>
       <td>N/A</td>
       <td>• Server</td>
     </tr>
     <tr>
       <td rowspan="2">TCP</td>
       <td rowspan="2">Traffic test</td>
       <td rowspan="2">• Node Port<br>• Test duration (s)<br>• Concurrent connections</td>
       <td>MtoN</td>
       <td>• Server<br>• Client</td>
     </tr>
     <tr>
       <td>FullMesh</td>
       <td>• Server</td>
     </tr>
   </table>

   The following table describes the parameters.

   | Parameter | Description |
   | --- | --- |
   | Number of QPS tested | The number of test processes. This parameter determines the test bandwidth. |
   | Node Port | The port number used for the test. |
   | Test duration (s) | The duration of the test. Unit: seconds. |
   | GDR | Specifies whether to enable direct communication between GPUs If you turn on this switch, the system associates the Remote Direct Memory Access (RDMA) network interface controller (NIC) with the corresponding GPU for traffic testing. Make sure that the machine supports this feature before you turn on the switch. |
   | Concurrent connections | The number of connections that can be processed at the same time. |
   | MtoN | The many-to-many relationship model. This model is used to test the one-way connectivity between <strong>Client</strong> nodes and <strong>Server</strong> nodes, including the one-way connectivity between a single <strong>Client</strong> node and a single <strong>Server</strong> node and between multiple <strong>Client</strong> nodes and multiple <strong>Server</strong> nodes. |
   | FullMesh | All nodes in the network topology are connected to each other. This option allows you to test the two-way connectivity between all destination nodes. |
   | Client | The sender of the test traffic. |
   | Server | The receiver of the test traffic. |

5. Click **Submit**. Then, the analysis task is created.

   - Click **Cancel** to go back to the page for creating an analysis task. You can modify the parameters based on your business requirements.

   - Click **View task details** to go to the **Analysis Task details** page.

**What to do next**

**View task details**

1. On the **HPN performance analysis** page, click Advanced Filter and filter tasks by **Start and end time**, **Task ID**, **Test type**, **Protocol Type**, **Traffic model**, **Task Status**, or their combinations.

2. Click **Details** in the Actions column of a task.

3. On the **Analysis Task details** page, view the task information and analysis results.

**Refresh a task**

Click **Refresh** in the Actions column of a task to refresh the task.

<a id="section-2-1-4"></a>

### 2.1.4. HPN instant diagnostics

High Performance Network (HPN) instant diagnostics refer to a diagnosis on HPN nodes. During the diagnosis, the system software, network, and GPU of nodes are checked. After the diagnosis, the diagnostic results and details are provided to help administrators troubleshoot network performance issues.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **HPN Management** > **HPN Instant Diagnostics**.

4. On the HPN instant diagnosis page, select a test cluster and one or more nodes from the drop-down lists and then click **Diagnosis**.

   > **Note**
   >
   > You can select multiple nodes at a time.

5. View the diagnostic results.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/dd9144fe0c9724de0b94a769c21abbda.webp)

   | Diagnostic result | Description |
   | --- | --- |
   | Diagnostic Item | Displays the diagnostic items, including <strong>OS Release Version</strong>, <strong>OS Kernel</strong> <strong>Version</strong>, <strong>Server CPU Model</strong>, <strong>Server Disk Space</strong>, <strong>RDMA NIC Drive</strong> <strong>Installation</strong>, <strong>RDMA NIC Drive Load</strong>, <strong>bonding Module Installation</strong>, <strong>GDR</strong> <strong>Module Installation</strong>, <strong>GDR Module Load</strong>, <strong>Number of RDMA Devices</strong>, <strong>RDMA</strong> <strong>Device Firmware Version</strong>, <strong>RDMA Device Aggregation Mode</strong>, <strong>RDMA</strong> <strong>Device Aggregation Status</strong>, <strong>RDMA Device Hash Policy</strong>, <strong>RDMA Device</strong> <strong>Port Rate</strong>, <strong>RDMA Device MTU Settings</strong>, <strong>PCIe MRR Configuration</strong>, <strong>PCIe</strong> <strong>Link Details</strong>, <strong>PCIe Link Rate</strong>, <strong>PCIe Link Width</strong>, and <strong>GPU Online Check</strong>. |
   | Diagnostic Result | Displays the diagnostic result of each diagnostic item. The result can be <strong>Passed</strong> or <strong>Failed</strong>. |
   | Diagnostic Details | Displays the diagnostic details of each diagnostic item. For example, the RDMA device port rates are consistent. |
   | Current Value | Displays the diagnostic value corresponding to each diagnostic item. |

<a id="section-2-2"></a>

## 2.2. CPN

<a id="section-2-2-1"></a>

### 2.2.1. CPN diagnosis

The Computing Platform Network (CPN) diagnosis feature checks the nodes in CPN and displays information such as the diagnostic items, diagnostic details, and diagnostic results to help administrators better understand and manage network performance and troubleshoot issues.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Diagnostics**.

4. On the CPN Quick Diagnostics page, click **Create Diagnostics Task**.

   In the Create Diagnostics Task dialog box, configure the parameters that are described in the following table.

   | Parameter | Description |
   | --- | --- |
   | Task Name | The name of the diagnostic task. |
   | Resource Pool | Default value: No. This indicates the Elastic Compute Service (ECS) Bare Metal Instances that are not added to compute clusters. |
   | Cluster | The cluster on which the diagnostic task is performed. |
   | Group | The hosts within the cluster that are grouped based on the CIDR block of the connected vSwitch. Each group can contain up to 100 hosts. |
   | Diagnostics node | The node on which the diagnostic task is performed. |

   > **Note**
   >
   > You can select multiple nodes.

5. Click **OK**. The diagnostic task starts running immediately.

**View diagnostic results**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Diagnostics**.

4. On the CPN Quick Diagnostics page, find the diagnostic task that you want to manage and click **Details** in the **Operation** column.

   | Tab | Description |
   | --- | --- |
   | Diagnostics Result | Displays the diagnostic results of the nodes on which the diagnostic task is performed. |
   | Overview view | Displays the cluster, the total number of instances, the number of normal items, and the number of abnormal items. |
   | Detailed View | Displays the diagnostic details by <strong>node</strong> or <strong>diagnostic item</strong>. |

5. Click the **Diagnostics Result** tab. On the Diagnostics Result tab, click **Details** in the Actions column of an abnormal diagnostic result. In the **Abnormal Diagnostic Details** panel, view the detailed information. Click **Details** in the Actions column of a diagnostic item. In the **Abnormal Diagnostic Result Details** dialog box, view the detailed information.

6. Click the **Overview View** tab to view the cluster, IP addresses, the total number of instances, the number of normal items, and the number of abnormal items.

7. Click the **Detailed View** tab to query diagnostic details by **node** or **diagnostic item**. You can view information such as the diagnostic results, diagnostic details, and error messages.

**What to do next**

The following table describes the operations that you can perform on the **CPN Quick Diagnostics** page.

| Operation | Procedure |
| --- | --- |
| Filter diagnostic tasks | • Basic filter<br>i. Select <strong>Start and End Time</strong> or <strong>Status</strong> from the drop-down list.<br>ii. Select a time range or state. The tasks that meet the filter condition are displayed.<br>• Advanced filter<br>i. Click <strong>Advanced Filter</strong>.<br>ii. Configure the <strong>Start and End Time</strong> and <strong>Status</strong> parameters and click <strong>Search</strong>. |
| Retry a diagnostic task | 1. Find the diagnostic task that you want to manage and click <strong>Retry</strong> in the <strong>Operation</strong> column.<br>2. In the message that appears, click <strong>OK</strong>. |
| Delete a diagnostic task | 1. Find the diagnostic task that you want to manage and click <strong>Delete</strong> in the <strong>Operation</strong> column.<br>2. In the message that appears, click <strong>OK</strong>. |

<a id="section-2-2-2"></a>

### 2.2.2. CPN performance analysis

You can perform a Computing Platform Network (CPN) performance analysis task to test the performance of machines under stress conditions. The task analyzes the maximum load and pressure resistance of the existing software and hardware. This helps identify the pressure limits of the machines and provides sufficient data for the O&M team to improve network performance.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Performance Analysis**.

4. On the CPN Performance Analysis page, click **Create Test**. On the Create Analysis Task page, create an analysis task.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/731bc96227fed5c8f0d1ffc242bb6afe.webp)

   The following table describes the parameter combinations of an analysis task for which the Protocol Type parameter is set to RDMA.

   <table>
     <tr>
       <th>Test cluster</th>
       <th>Protoc ol Type</th>
       <th>Test type</th>
       <th>Required parameter</th>
       <th>Traffic model value</th>
       <th>Node</th>
     </tr>
     <tr>
       <td rowspan="4"><em>Arbitrary</em></td>
       <td rowspan="4">RDMA</td>
       <td rowspan="3">Traffic test</td>
       <td rowspan="3">• Number of QPS tested<br>• Node Port<br>• Test duration (s)<br>• GDR</td>
       <td>MtoN</td>
       <td>• Server<br>• Client</td>
     </tr>
     <tr>
       <td>FullMesh</td>
       <td>Server</td>
     </tr>
     <tr>
       <td>Ring</td>
       <td>Server</td>
     </tr>
     <tr>
       <td>Latency Test</td>
       <td>• Node Port<br>• Test duration (s)</td>
       <td>N/A</td>
       <td>Server</td>
     </tr>
   </table>

   The following table describes the parameters you must configure to create an analysis task for which the Protocol Type parameter is set to RDMA.

   | Parameter | Description |
   | --- | --- |
   | Number of QPS tested | The number of test processes. This parameter determines the test bandwidth.<br>• If the queue pairs (QPs) are insufficient, the communication queue in the RDMA network may be congested, which compromises the efficiency and stability of data transmission.<br>• If the number of QPs is excessively large, the system overheads, complexity, and failure rate are increased.<br>Note<br>QP is a key term of the RDMA network. It refers to the communication queue between a pair of endpoints. |
   | Node Port | The port number used for the test. |
   | Test duration (s) | The duration of the test. Unit: seconds. |
   | GDR | Specifies whether to enable direct communication between GPUs If you turn on this switch, the system associates the RDMA network interface controller (NIC) with the corresponding GPU for traffic testing. Make sure that the machine supports this feature before you turn on the switch. |
   | MtoN | The many-to-many relationship model. This model is used to test the one-way connectivity between <strong>Client</strong> nodes and <strong>Server</strong> nodes, including the one-way connectivity between a single <strong>Client</strong> node and a single <strong>Server</strong> node and between multiple <strong>Client</strong> nodes and multiple <strong>Server</strong> nodes. |
   | FullMesh | All nodes in the network topology are connected to each other. This option allows you to test the two-way connectivity between all destination nodes. |
   | Ring | Multiple nodes in the network topology form a closed loop. Data packets are sent from one node to the next node in sequence and finally returned to the original node. This option allows you to test the actual available network bandwidth. |
   | Client | The sender of the test traffic. |
   | Server | The receiver of the test traffic. |

   The following table describes the parameters you must configure to create an analysis task for which the Protocol Type parameter is set to Communication Library.

   | Test clust er | Protocol Type | Test type | Communicati on Library | Required parameter |
   | --- | --- | --- | --- | --- |
   | <em>Arbitr</em> <em>ary</em> | Commun ication Library | Communi cation library test | • NCCL<br>• CPN-CCL<br>• RCCL<br>• PCCL | • <strong>Algorithm</strong>: the algorithm of the task. The algorithm bandwidth, bus bandwidth, and execution time of a task vary based on the algorithm.<br>• <strong>Communication Primitive</strong>: The data transmission and processing methods vary based on the communication primitive. Select a value from the drop-down list.<br>• <strong>Timeout Period (Seconds)</strong>: If the execution time of performance analysis test is greater than the specified timeout period plus 1 minute, the test task fails.<br>• <strong>Data Type</strong>: the data type of the performance analysis test. Select a value from the drop-down list.<br>• <strong>Iterations</strong>: the number of times the current task is executed.<br>• <strong>Minimum Bytes</strong>: the minimum amount of data to start the task.<br>• <strong>Maximum Bytes</strong>: the maximum amount of data to stop the task.<br>• <strong>Step Factor</strong>: Specify an integer greater than 1. If you set the parameter to 2, the data specification increases by two times. The first row corresponds to the value of the Start bytes parameter and the last row corresponds to the value of the Number of cut-off bytes parameter.<br>• <strong>Hosts</strong>: Click <strong>Select a node</strong> to add hosts.<br>• <strong>mpirun Custom Parameters</strong>: Specify custom parameters in the <code> --mca ... -</code><code>-mca ... </code> format. Example: <code> --mca </code> <code>pml ob1 --mca coll ^hcoll --mca btl</code><br><code>tcp,self --mca btl_tcp_if_include</code><br><code>bond0 --mca oob_tcp_if_include</code> <code>bond0 --bind-to none </code>.<br>• <strong>NCCL Parameters</strong>: the custom properties and values. |

5. Click **Submit**.

**What to do next**

The following table describes the operations that you can perform on the **CPN Performance Analysis** page.

| Operation | Procedure |
| --- | --- |
| Query a test task | • Basic filter<br>After you specify the start time and end time, the test tasks that meet the filter condition are displayed.<br>• Advanced filter<br>i. Click <strong>Advanced Filter</strong>.<br>ii. Configure the Start and end time, Test Type, Protocol Type, and Status parameters.<br>iii. Click <strong>Search</strong>. |
| View performance analysis details | 1. Find the test task that you want to manage and click <strong>Details</strong> in the <strong>Operation</strong> column.<br>2. On the Analysis Task Details page, view the basic information, analysis results, and device information of the task. |
| Export performance analysis details | Note<br>You can export the performance analysis details of a test task of the traffic test or latency test type.<br>1. Find the test task that you want to manage and click <strong>Details</strong> in the <strong>Operation</strong> column.<br>2. On the <strong>Analysis Task Details</strong> page, click <strong>Export</strong> to the right of <strong>Analysis Results</strong>.<br>3. View the exported Excel file on your computer. |
| Retry a test task | 1. Find the test task that you want to manage and click <strong>Retry</strong> in the <strong>Operation</strong> column.<br>2. In the message that appears, click <strong>OK</strong>. The value in the <strong>Task Status</strong> column changes to <strong>Running</strong>. |
| Delete a test task | 1. Find the test task that you want to manage and click <strong>Delete</strong> in the <strong>Operation</strong> column.<br>2. In the message that appears, click <strong>OK</strong>. |
| Terminate a test task | 1. Find the test task that you want to manage and click <strong>Stop</strong> in the <strong>Operation</strong> column.<br>2. In the message that appears, click <strong>OK</strong>. The value in the <strong>Task Status</strong> column changes to <strong>Stopping</strong>. If the value in the <strong>Task Status</strong> column changes to <strong>Stopped</strong>, the task is terminated. |

<a id="section-2-2-3"></a>

### 2.2.3. CPN alert center

The CPN Alarm Center module displays alerts, including real-time alerts that are not closed and closed historical alerts.

**Alert Distribution Overview**

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Alarm Center**.

4. On the **CPN Alerts** page, click the **Alert Distribution Overview** tab to view the statistics of various types of CPN alerts. By default, the statistics of **Not Closed** alerts are displayed. You can click **Closed** to view the statistics of closed alerts.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/168bc3b4ef65041c58059237c963144b.webp)

   - You can set **Start and End Time** to filter and view the alerts in the specified time range.

   - CPN alerts are classified into two types: **Client** and **Network**. Network-side alert types include **RASW**, **RDSW**, **EHSW**, **EDSW**, and **CHSW**.

   - You can click **Details** in the **Actions** column to go to the list of alerts of a specified type or a specified alert item.

**Host Alert**

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Alarm Center**.

4. On the **CPN Alerts** page, click the **Host Alert** tab to view real-time CPN alerts on the **Client** side. By default, **Not Closed** alerts are displayed. You can click **Closed** to view the closed alerts.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/9c1487acf4900bc03dcd0f5eb9875ca7.webp)

   - You can click the up or down arrow next to **Alert Level** or **Last Alert Time/Duration** to sort alerts.

   - The alert information includes **Alert Level**, **Alert Item ID**, **Resource Owner**, **Alert Information**, **Alert Status**, **Alert Start Time**, **Last Alert Time/Duration**, **Alerts**, **Alert Details**, and **Alert Object Name/ID**.

   - Click **Advanced Filter** and filter alerts by **Alert Item ID**, **Alert Start Time**, **Alert Level**, **Alert Object Name**, or any combination of them.

   - Click an alert item ID in the **Alert Item ID** column to go to the **Alert Details** page and view the details of the alert. For more information, see Alert details.

   - Move the pointer over **Details** in the **Alert Details** column of an alert to view the details of the alert.

**Switch Alert**

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Alarm Center**.

4. On the **CPN Alerts** page, click the **Switch Alert** tab to view real-time CPN alerts on the **Network** side. By default, **Not Closed** alerts of the **RASW** type are displayed. You can click **Closed** to view the closed alerts.

   You can also switch between tabs to view the real-time alerts of the **RASW**, **RDSW**, **EHSW**, **EDSW**, and **CHSW** types on the Network side.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/7c9a2cba522193c892375d1b595d4706.webp)

   - You can click the up or down arrow next to **Alert Level** or **Last Alert Time/Duration** to sort alerts.

   - The alert information includes **Alert Level**, **Alert Item ID**, **Resource Owner**, **Alert Information**, **Alert Status**, **Alert Start Time**, **Last Alert Time/Duration**, **Alerts**, **Alert Details**, and **Alert Object Name/ID**.

   - Click **Advanced Filter** and filter alerts by **Alert Item ID**, **Alert Start Time**, **Alert Level**, **Alert Object Name**, or any combination of them.

   - Click an alert item ID in the **Alert Item ID** column to go to the **Alert Details** page and view the details of the alert. For more information, see Alert details.

   - Move the pointer over **Details** in the **Alert Details** column of an alert to view the details of the alert.

<a id="section-2-2-4"></a>

### 2.2.4. CPN access gateways

<a id="section-2-2-4-1"></a>

#### 2.2.4.1. Manage RDMA devices

This topic describes how to manage Remote Direct Memory Access (RDMA) devices, including how to scan for and delete RDMA devices.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Access Gateway**.

4. Select the **RDMA Device Management** tab.

5. Manage RDMA devices.

   - Scan for new devices

     Click **Scan New Devices** to add new RDMA devices to the system.

   - Query new devices

     - Basic filter

       <ol type="a">

       <li>

       Select **Device Name**, **Equipment manufacturer**, **Equipment model**, **Device role**, **Device Management IP**, **Serial Number**, or **Device status** from the drop-down list.

       </li>

       <li>

       In the search box, enter the device name or manufacturer, or select the status of the

       device, and click <img src="en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/c6ab62fe7ac13625e69e35414cdbc510.webp" width="16" alt=""> .

       </li>

       </ol>

     - Advanced filter

       <ol type="a">

       <li>

       Click **Advanced Filter**.

       </li>

       <li>

       Enter the device name, device manufacturer, device model, device role, device management IP address, and serial number, and select the device status.

       </li>

       </ol>

       <ol type="i" start="100">

       <li>

       Click **Search**.

       </li>

       </ol>

   - Delete a new device

     <ol type="a">

     <li>

     Click **Delete** in the **Actions** column.

     </li>

     <li>

     In the message that appears, click **OK**.

     </li>

     </ol>

<a id="section-2-2-4-2"></a>

#### 2.2.4.2. Manage RDMA device policies

This topic describes how to configure policies for Remote Direct Memory Access (RDMA) devices to manage RDMA devices in a centralized manner.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Access Gateway**.

4. Click the **RDMA device policy management** tab.

5. Click **Create an RDMA device policy** and set the parameters. The following table describes the parameters.

   | Parameter | Description |
   | --- | --- |
   | Policy name | Enter a custom name for the policy. |
   | Description | Enter the description of the policy. This parameter is optional. |
   | Equipment manufacturer | Select a device vendor from the drop-down list. The system automatically displays the device vendors on the <strong>RDMA Device Management</strong> tab. |
   | Device role | Select the role of the device to which the policy applies from the drop-down list.Valid values:<br>• <strong>RASW</strong>: the access vSwitch of the data exchange module in RDMA networking scenarios.<br>• <strong>RDSW</strong>: the core vSwitch of the data exchange module in RDMA networking scenarios. The core vSwitch is used to connect different access vSwitches.<br>• <strong>EHSW</strong>: the vSwitch that is used to connect to the custodian network in RDMA networking scenarios. |
   | Equipment model | Select the model of the device to which the policy applies from the drop-down list. The system automatically displays the device models on the <strong>RDMA</strong> <strong>Device Management</strong> tab. |
   | Device List | Select the device to which the policy applies from the drop-down list. The system automatically displays the devices of a specific device model on the <strong>RDMA Device Management</strong> tab. |
   | Headroom | The size of the RDMA over Converged Ethernet (RoCE) queue buffer, and the maximum number of available cell resources in the headroom. Enter the size of the global buffer. |

6. Click **OK**.

**What to do next**

On the **RDMA device policy management** tab, you can perform the following operations:

| Operation | Procedure |
| --- | --- |
| Query the policy for an RDMA device | 1. Select <strong>Device Name</strong>, <strong>Equipment manufacturer</strong>, <strong>Equipment model</strong>, <strong>Device role</strong>, <strong>Device Management IP</strong>, <strong>Serial Number</strong>, or <strong>Device status</strong> from the drop-down list.<br>2. Enter the device name, device vendor, device model, device role, device management IP address, serial number, or device status in the search box<br>and click<img src="en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/ea3c8fc7b760bf7848f674f4a9c95f81.webp" width="16" alt="">. |
| View the details of the policy of an RDMA device | 1. Click <strong>Details</strong> in the <strong>Actions</strong> column.<br>2. Click <strong>OK</strong> or <strong>Cancel</strong>. |
| Retry the policy of an RDMA device | 1. Click <strong>Retry</strong> in the <strong>Actions</strong> column.<br>2. In the message that appears, click <strong>OK</strong>. |

<a id="section-2-2-4-3"></a>

#### 2.2.4.3. Manage policies for the RDMA device interface

This topic describes how to manage interface policies, such as policy configuration, query, and retry.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Access Gateway**.

4. Click the **RDMA device interface policy management** tab.

5. Click **Create an RDMA device interface policy** and configure the following parameters.

   | Parameter | Description |
   | --- | --- |
   | Policy Name | Enter a custom name for the policy. |
   | Description | Enter the description of the policy. This parameter is optional. |
   | Device Vendor | Select a device vendor from the drop-down list. The system automatically displays the device vendors on the <strong>RDMA Device Management</strong> tab. |
   | Device Role | Select the role of the device to which the policy applies from the drop-down list.Valid values:<br>• <strong>RASW</strong>: the access vSwitch of the data exchange module in Remote Direct Memory Access (RDMA) networking scenarios.<br>• <strong>RDSW</strong>: the core vSwitch of the data exchange module in RDMA networking scenarios. The core vSwitch is used to connect different access vSwitches.<br>• <strong>EHSW</strong>: the vSwitch that is used to connect to the custodian network in RDMA networking scenarios. |
   | Device Model | Select the model of the device to which the policy applies from the drop-down list. The system automatically displays the device models on the <strong>RDMA</strong> <strong>Device Management</strong> tab. |
   | Device List | Select the device to which the policy applies from the drop-down list. The system automatically displays the devices of a specific device model on the <strong>RDMA Device Management</strong> tab. |
   | RoCE queue PFCs configuration (RDMA over Converged Ethernet) | • <strong>Headroom cache threshold</strong>: the size of the RDMA over Converged Ethernet (RoCE) queue buffer, and the maximum number of available cell resources in the headroom.<br>• <strong>Back pressure frame trigger threshold</strong>: the analysis model of network traffic. The model ensures that the sum of the back pressure frame triggering thresholds for all ingresses is less than or equal to the tail-drops threshold for the egress.<br>• Offset between back pressure frame stop threshold and trigger <strong>threshold</strong>: When the number of cell resources used by packets with a 802.1p priority decreases by the value of this parameter after PFC is triggered, PFC stops sending PFC pause frames.<br>• <strong>PFCs reserved threshold</strong>: the number of cell resources reserved for packets with a 802.1p priority in the guaranteed storage capacity.<br>• <strong>PFCs</strong>: If you use PFC and congestion occurs in a specific type of traffic, the routing of other types of traffic is not affected. This ensures that different types of packets on the same link do not affect each other.<br>• <strong>Deadlock monitoring function</strong>: If a link or device failure occurs, temporary loops may occur during the route reconvergence period. In this case, PFC frames are repeatedly sent and received between devices, packets cannot be forwarded, cell resources in the interface buffer are occupied and cannot be released, and the device enters the PFC deadlock state. |
   | RoCE queue WRED configuration | • <strong>ECN function</strong>: Explicit Congestion Notification (ECN) uses the DiffServ field in the IP header to mark the congestion status along the packet transmission path. An ECN-capable terminal can determine whether congestion occurs on the transmission path based on the packet content. If congestion occurs, the terminal adjusts the method to send packets to prevent congestion from being aggravated.<br>• <strong>Lower limit of average queue length</strong>: the lower limit of the length of the queue that the packets of the forwarding device enter in the egress. The lower limit is also called ECN threshold.<br>• <strong>Upper limit of average queue length</strong>: When the device assigns packets to a queue in the outbound direction, the queue size reaches the upper threshold (ECN threshold).<br>• <strong>Discarding probability</strong>: the marking probability if ECN is used. A larger value indicates that more packets are marked between the upper and lower limits.<br>Note<br>• If the length of the queue that the packets of the forwarding device enter in the egress is smaller than the lower limit, the forwarding device directly forwards the packets from the egress without processing the packets.<br>• When the device assigns packets to a queue in the outbound direction, if the average queue size is between the lower threshold and the upper threshold, take note of the following items:<br>• If the value of the ECN field in the received packets is 00, the packets are sent out of an ECN-incapable terminal. In this case, the forwarding device determines whether to drop the packets based on the drop probability.<br>• If the value of the ECN field in the received packets is 01 or 10, the packets are sent out of an ECN-capable terminal. In this case, the forwarding devices change the value of the ECN field for some of these packets based on the drop probability and forward these packets. All incoming packets are not dropped.<br>• If the ECN field is 11 in a packet, the packet on the original device has experienced congestion along the transmission path. In this case, the device does not process the packet and directly forwards the packet out of the outgoing interface.<br>• When the device assigns packets to a queue in the outbound direction, if the average queue size exceeds the upper threshold, take note of the following items:<br>• If the ECN field is 00, the packets are sent out of an ECN-incapable terminal, the device drops the packets.<br>• If the value of the ECN field in the packet received by the device is 01 or 10, it indicates that the packet sender supports the ECN function. After the ECN field of the inbound packet is changed to 11, the packet continues to be forwarded, and all inbound packets are not discarded.<br>• If the ECN field is 11 in a packet, the packet on the original device has experienced congestion along the transmission path. In this case, the device does not process the packet and directly forwards the packet out of the outgoing interface. |

6. Click **OK**.

**What to do next**

On the **RDMA device interface policy management** tab, you can perform the following operations:

| Operation | Procedure |
| --- | --- |
| Query the policy for an RDMA device interface | 1. Configure the <strong>Policy Name</strong>, <strong>Device Vendor</strong>, <strong>Device Model</strong>, <strong>Device Role</strong>, or <strong>Device Management IP</strong> parameter.<br>2. Enter the policy name, device vendor, device model, device role, or device<br>management IP address in the search box and click the<img src="en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/ea3c8fc7b760bf7848f674f4a9c95f81.webp" width="16" alt="">icon. |
| View the details of a policy of an RDMA device interface | 1. Click <strong>Details</strong> in the <strong>Actions</strong> column.<br>2. Click <strong>OK</strong> or <strong>Cancel</strong>. |
| Retry the policy for an RDMA device interface | 1. Click <strong>Retry</strong> in the <strong>Actions</strong> column.<br>2. In the message that appears, click <strong>OK</strong>. |

<a id="section-2-2-5"></a>

### 2.2.5. RDMA NIC O&M

To perform O&M on Remote Direct Memory Access (RDMA) network interface cards (NICs), you must check the performance metrics of RDMA NICs. RDMA NIC O&M allows you to identify and troubleshoot issues and ensure network stability and reliability.

**Terms**

**RDMA**: RDMA is a high-speed network technology developed to reduce the delay of server-side data processing in network transmission. RDMA transfers data directly into the memory of a computer over the RDMA network and enables direct memory access between hosts without affecting the operating system. This increases the data transfer speed and reduces the CPU load.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > RDMA Card O&M**.

4. In the upper-right corner of the page, select **Data Source** and **Cluster**. You can set Data Source only to CPN.

5. On the **Cluster** tab, view the monitoring information about the cluster.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/9ac6506c97fcc78ee73e53b466c8b018.webp)

   | Section | Description |
   | --- | --- |
   | Average QP | The average number of queue pairs (QPs) in the RDMA network. If you select PAI for Data Source, this parameter is unavailable.<br>• If the number of QPs is insufficient, the queue is blocked, which affects the efficiency and stability of data transmission.<br>• If the number of QPs is excessively large, the system overheads, complexity, and failure rate increase.<br>Note<br>A QP is a key concept in RDMA networks and is used to describe the queue between a pair of endpoints. |
   | Abnormal Networks | The number of times that network device exceptions or traffic exceptions occur in the RDMA network. |
   | Average Throughput Sent by RDMA (Mbit/s) | The average amount of data sent by all nodes in the RDMA network per second. |
   | Average Throughput Received by RDMA (Mbit/s) | The average amount of data received by all nodes in the RDMA network per second. |
   | Monitoring Chart | i. Select the start time and the end time on the right side of the monitoring chart to view the monitoring data within the time range.<br>ii. In the <strong>Throughput Dashboard</strong> section, view the RDMA_TX_BYTES and RDMA_RX_BYTES metrics.<br>• RDMA_TX_BYTES is the number of bytes sent in the RDMA network.<br>• RDMA_RX_BYTES is the number of bytes received in the RDMA network.iii. In the <strong>Basic Data of RDMA Network</strong> section, view the following data in the specified time range:<br>• <strong>RDMA_IGNORE_CNP_AVG</strong>: the average number of ignored Congestion Notification Packets (CNPs) in the RDMA network.<br>Note |
   | RDMA Network Overview | CNPs are packets used for network congestion control. When View the metrics of the nodes in the RDMA network, including <strong>Nodes</strong>, network congestion occurs, CNPs are sent to notify the sender to <strong>Outbound Throughput</strong>, <strong>Inbound Throughput</strong>, <strong>Network QP</strong>, <strong>CNP</strong> reduce the sending rate to avoid network congestion and packet <strong>Processed by Network</strong>, <strong>Out-of-order Data Packets</strong>, and <strong>Network</strong> loss.<strong>Buffer Overflow</strong>. |

   - **RDMA_TX_PFC_PAUSE_AVG**: the average number of Priority-based

6. On the **Node** tab, view the monitoring information of each node.

   Flow Control (PFC) packets when data is sent in the RDMA network.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/d116c662944e16815449eaffabd60197.webp)

   - **RDMA_MARKED_ECN_AVG**: the average number of marked Explicit

   <table>
     <tr>
       <th>Con Parameter<br>• RD in t</th>
       <th>gestion Notification (ECN) packets in the RDMA network.Description MA_HANDLE_CNP_AVG: the average number of CNPs processed he RDMA network.</th>
     </tr>
     <tr>
       <td>• RD QP in RDMA Network that</td>
       <td rowspan="5">MA_TX_PFC_TRANS_AVG: the average number ofPFC packets are enabled in the RDMA network.<br>MA_QP_CNT_AVG:the average number of QPs in the RDMA work.<br>MA_TX_BYTES_AVG: the average number of bytes of data sent in RDMA network.<br>MA_RX_BYTES_AVGDisplays the monitoring data of a node. For more information,: the average number of bytes of data ived in the RDMA network.see the descriptions of the cluster metrics.</td>
     </tr>
     <tr>
       <td>• RD net Abnormal Networks<br>• RD</td>
     </tr>
     <tr>
       <td>the Throughput Sent by RDMA<br>• RD Network (Mbit/s) rece</td>
     </tr>
     <tr>
       <td>Throughput Received by RDMA Network (Mbit/s)</td>
     </tr>
     <tr>
       <td>Monitoring Chart</td>
     </tr>
   </table>

<a id="section-2-2-6"></a>

### 2.2.6. CPN management

<a id="section-2-2-6-1"></a>

#### 2.2.6.1. CPN topology

This topic describes how to query the topology information about clusters and nodes.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Network Management > CPN Topology**.

4. In the upper-left corner of the page, select **Cluster** and **Nodes**.

5. Click **Query** to query the topology information.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/d654df48ed68fdf38463afcf0dd303cf.webp)

**What to do next**

After the topology is displayed, you can perform the following operations:

| Operation | Procedure |
| --- | --- |
| Zoom in or zoom out the topology | Click<img src="en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/1f886e4c075fdfa373e3410e46d43523.webp" width="14" alt="">or<img src="en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/4aaeb1100fb91aee3122092a3ba10394.webp" width="16" alt="">in the upper-right corner of the topology to zoom in or zoom<br>out the topology. |
| Reset the topology canvas | Click<img src="en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/9745c84a8f9fc50ea004b7b9538eeb03.webp" width="18" alt="">in the upper-right corner of the topology to reset the canvas. |
| Display the topology in full screen | 1. Click<img src="en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/14130f5b5048abf2e2a43e37d2c28117.webp" width="17" alt="">in the upper right corner of the topology to display the topology<br>in full screen.<br>2. Click<img src="en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/9084a7d9d31be14e4ffc53021aa47a69.webp" width="27" alt="">in the upper-right corner to exit the full screen. |

<a id="section-2-2-6-2"></a>

#### 2.2.6.2. CPN network element

This topic describes how to view network devices and monitoring and O&M information in the cloud platform.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Network Management > CPN Network Element**.

4. Select a data center from the drop-down list and enter a network element name in the **Network element name** search box.

5. Click the name of a network element or click **Details** in the **Actions** column to go to the details page of the network element.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/81f724eea0e00f967c107ffcc66928a4.webp)

   | Tab | Description |
   | --- | --- |
   | Port | Displays the port information of the network element device. Click the port name or click <strong>View</strong> in the <strong>Actions</strong> column to view the usage data of the port. |
   | CPU Utilization | Displays the CPU usage of the network element device. |
   | Memory Utilization | Displays the memory utilization of the network element device. |
   | Aggregation Port Management | Displays the aggregated port information of the network element device.Click <strong>View</strong> in the <strong>Actions</strong> column to view the traffic of the port. |
   | Alert | Displays the alert information of the network element device. |

**What to do next**

On the **CPN network element** page, you can also perform the following operations:

| Operation | Procedure |
| --- | --- |
| Delete a CPN network element | 1. Click <strong>Delete</strong> in the <strong>Actions</strong> column.<br>2. In the message that appears, click <strong>OK</strong>. |

<a id="section-2-2-7"></a>

### 2.2.7. CPN network monitoring

<a id="section-2-2-7-1"></a>

#### 2.2.7.1. CPN host monitoring dashboard

You can use this feature to monitor the key metrics of remote direct memory access (RDMA) networks on the server side of the intelligent computing network. The metrics include bandwidth, packet loss rate, and traffic control.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Network Monitoring > CPN Host Monitoring**.

4. In the upper-right corner of the CPN host monitoring dashboard page, click **Variable Filtering**. In the Variable Filtering dialog box, configure the **Custer** and **Host** parameters, and click **OK**.

5. On the **CPN host monitoring dashboard** page, view information about the following metrics: **Network Overview**, **End-side congestion packet loss**, **Network card RDMA packet loss**, **Network card RDMA communication QP quantity & network card status**, **Network congestion metrics**, **Network physical throughput**, and **Nic queue**

   **throughput**. You can also click the <img src="en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/58d1e38d6cfbc20d2771d69225f41db3.webp" width="13" alt=""> icon to the left of each metric to view details.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/fbc918d40be961d84a1ba57e8d5c7bb6.webp)

<a id="section-2-2-7-2"></a>

#### 2.2.7.2. CPN switch dashboard

You can use this feature to monitor the running status metrics of vSwitches. The metrics include bandwidth, packet loss, and traffic control.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Network Monitoring > CPN Switcher**.

4. In the upper-right corner of the CPN switch dashboard page, click **Variable Filtering**. In the Variable Filtering dialog box, configure the **idc** and **host** parameters, and click **OK**.

5. On the CPN switch dashboard page, view information about the following metrics: **Network Overview**, **Ruijie exception indicator top 50**, **Top 50 abnormal indicators**, **Queue**

   **metrics**, **Port metrics**, **Alarm status**, and **Logs**. You can also click the <img src="en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/58d1e38d6cfbc20d2771d69225f41db3.webp" width="13" alt=""> icon to the left

   of each metric to view details.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/002e586d0af6091734eb430a666e8483.webp)

<a id="section-2-2-7-3"></a>

#### 2.2.7.3. NAK packet analysis tool

You can use this tool to collect NAK packets in real time. After the packets are aggregated and analyzed, a matrix diagram is generated to help you quickly identify abnormal nodes.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Network Monitoring > NAK Message Analysis Tool**.

4. In the upper-right corner of the NAK message Analysis Tool page, click **Variable Filtering**. In the Variable Filtering dialog box, configure the **Network cluster**, **SOURCE device Group**, and **Destination device Group** parameters, and click **OK**.

5. On the **NAK message Analysis Tool** page, view information about the following metrics: **Network cluster-level NAK dashboard** and **Device Group-level NAK dashboard.** You

   can also click the

   icon to the left of each metric to view details.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/196904b17216f73a5205df48c8b98bd8.webp)

<a id="section-2-2-7-4"></a>

#### 2.2.7.4. High-precision monitoring dashboard

The high-precision monitoring dashboard of Computing Platform Network (CPN) allows you to monitor traffic of network interface cards (NICs) and bond devices with a latency of seconds.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Network Dashboard > High Precision Monitoring Dashboard**.

4. In the upper part of the page, select a cluster from the **High Precision Monitoring Clusters** drop-down list and one or more nodes from the **Node** drop-down list, and then click Start High-precision Task.

5. In the dialog box that appears, configure the **Duration (s)** parameter. Valid values: 1 to

   600. Default value: 300. Then, click **OK**.

6. In the upper-right corner of the page, specify the time range of the monitoring. Select a start time and an end time, and then click **OK**.

7. In the upper-right corner of the page, click the Refresh icon or set the automatic refresh interval to view the latest monitoring data.

> **Note**
>
> If one of the selected nodes is in the Running state, you cannot start the task again until the duration of the task elapses.

![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/ca39719c5b27e44119b94bd19b85bc42.webp)

<a id="section-2-2-7-5"></a>

#### 2.2.7.5. High-precision vSwitch monitoring dashboard

The high-precision vSwitch monitoring dashboard of Computing Platform Network (CPN) allows you to monitor traffic of vSwitches with a latency of seconds.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Network Dashboard > Switch High Precision Monitoring Dashboard**.

4. In the upper part of the High-precision vSwitch Monitoring page, configure the required parameters and click **Start High-precision Task**.

   The following table describes the parameters.

   | Parameter | Description |
   | --- | --- |
   | idc | The data center on which the high-precision monitoring task is performed. |
   | vSwitch | The vSwitch on which the high-precision monitoring task is performed. |
   | Port | The port that you want to monitor. |
   | Queue | The number of queues configured for the specified port. Valid values: 0 to 7. |

5. In the dialog box that appears, configure the **Duration (s)** and **Task type** parameters. Valid values of the Duration (s) parameter: 1 to 600. Default value of the Duration (s) parameter: 300. Then, click **OK**.

   > **Note**
   >
   > The value of the Task type indicates the monitoring object of the task. The related data of the unselected monitoring object is not displayed on the High-precision vSwitch Monitoring page.

6. In the upper-right corner of the page, click the time range drop-down list. Then, select the monitoring start time and end time from the drop-down list and click **OK**.

7. In the upper-right corner of the page, click the Refresh icon or set the automatic refresh time to view the latest monitoring data.

> **Note**
>
> If one of the selected nodes is in the Running state, you cannot start the task again until the duration of the task elapses.

<a id="section-2-2-7-6"></a>

#### 2.2.7.6. Job monitoring

Computing Platform Network (CPN) provides the job monitoring feature, including the monitoring of top N metrics for hosts, end-to-end packet loss caused by congestion, and Remote Direct Memory Access (RDMA) packet loss of network interface cards (NICs).

**Prerequisites**

The related tasks are created in the task modeling module of AI Studio.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Network Dashboard > Job Monitoring**.

4. In the upper part of the **Job Monitoring** page, click **Expand more** and configure the **idc**, **Cluster**, **JobType**, **TrainJobId**, **Tips**, **hostIps**, and **swNames** parameters.

5. After you configure these parameters, the corresponding monitoring data appears in the

   lower part of the page. You can view the monitoring metrics in each panel. Click the

   icon to the left of each panel name to fold or unfold the panel.

![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/2e0a05771ffc1684b68e9ccadc4b0c5d.webp)

<a id="section-2-2-7-7"></a>

#### 2.2.7.7. CPN stream monitoring

Computing Platform Network (CPN) supports the global traffic observability feature, including the visualization of communication relationships, communication paths, communication quality, and impacts of congestion.

**Prerequisites**

By default, the stream-based visualization feature of CPN is disabled. Before you use this feature, make sure that the cpn-lsgo database is enabled. Run the following code statement to enable the database:

```sql
update config_detail_info set config_value='on' where config_key in 
('tracing_open','cpn_gtp','cpn_gto','cpn_gts','asnet-cpn-lsgo-agent');
```

After the database is enabled, you must restart the service.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > CPN Management > CPN Network Dashboard > CPN Flow Monitor**.

4. On the **Host** tab, view the traffic monitoring data by cluster.

   - Advanced Filter: In this section, configure the **Cluster Name**, **Management Port IP Address of Source NC Filter based on the source IP addresses of the stream.**, **Source NIC**, **Management Port IP Address of Destination NC Filter based on the destination IP address of the stream.**, **Destination NIC**, and **Time** parameters to filter and view data.

   - View stream details: You can click **Details** in the **Actions** column to go to the stream details page and view information in the **Stream Change Events**, **Path Change Events**, and **RTT Trend** sections.

5. On the **vSwitch** tab, view the traffic monitoring data by vSwitch.

   - Advanced Filter: In this section, configure the **Local Device**, **Type**, **Local Device Port**, **Peer Device**, and **Time** parameters to filter and view data.

   - View stream details

     <ol type="a">

     <li>

     Click **Details** in the **Actions** column to view the streams loaded on a port.

     </li>

     <li>

     In the **Stream List** panel, click **Details** in the **Actions** column to go to the stream details page and view information in the **Stream Change Events**, **Path Change Events**, and **RTT Trend** sections.

     </li>

     </ol>

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/9609323e43d8d75e627f496817077a31.webp)

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/1154e3ad92d421865adde21ee3784ddc.webp)

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/f850b3188de22556351ad8e5120e815e.webp)

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/46689c8a8df340a197702bb4ff3f9a82.webp)

<a id="section-2-3"></a>

## 2.3. CGW

You can connect bare metal instances to a virtual private cloud (VPC) by using Central Gateway (CGW) to manage the bare metal instances in a centralized manner. CGW instances are dedicated hybrid switches (HSWs). The system supports operations such as instance management, operation log viewing, network management of bare metal instances, and O&M configurations to help you complete the daily O&M operations of CGW.

> **Note**
>
> By default, the CGW feature is not displayed. To use the feature, click **User Authorities** in the top navigation bar of the Apsara Uni-manager Operations Console. In the left-side navigation pane of the page that appears, click **Menu Management**. On the Menu management page, find Cloud Gateways and click Modify in the Actions column. In the Edit menu items panel, turn on **Show or not**.

**Instance management**

On the Instance Management page, you can manage the added CGW instances in a centralized manner and view the summary information about the CGW instances in the system.

**Display devices**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **Instance Management** tab. On the **Display Devices** tab, view the instance details.

   | Parameter | Description |
   | --- | --- |
   | Cloud Gateway Name | The name of the CGW instance. |
   | IBGP Role | The role of the CGW instance in the environment.<br>• <strong>Client</strong>: specifies that the CGW instance acts as a client of an Internal Border Gateway Protocol (iBGP) neighbor and provides server access.<br>• <strong>Deploy Client and RR on a Device</strong>: specifies that the CGW instance acts as a route reflector (RR) of an iBGP neighbor and provides server access.<br>• <strong>Deploy RR on a Device</strong>: specifies that the CGW instance acts as an RR of an iBGP neighbor and does not provide server access. |
   | Manage IP Address | The IP address of the CGW instance. |
   | Management status | The initialization state of the CGW instance. Valid values:<br>• Uninitialized<br>• Initializing<br>• Initialized |
   | Authorization Status | The authorization state of the CGW instance. Valid values:<br>• Unauthorized<br>• Authorized<br>Note<br>To use CGW instances, you must plan the number of CGW licenses in Deployment Planner. If the number of CGW licenses in Deployment Planner is less than that of used CGW instances, the CGW instances without license authorization are in the Unauthorized state. In this case, you need to increase the number of CGW licenses. |
   | Created At | The time when the CGW instance was created. |

**Scan new devices**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **Instance Management** tab. Then, click the **Scan for New Devices** tab.

5. On the Scan for New Devices tab, find the device that you want to manage and click **Manage** in the **Actions** column.

   Alternatively, select multiple devices that you want to manage and click **Batch Manage**.

6. In the Manage dialog box, find the device and configure the **IBGP Role** parameter.

   The IBGP Role parameter specifies the role of a CGW instance in the environment. Valid values of the IBGP Role parameter:

   - **Client**: specifies that the CGW instance acts as a client of an iBGP neighbor and provides server access.

   - **Deploy Client and RR on a Device**: specifies that the CGW instance acts as an RR of an iBGP neighbor and provides server access.

   - **Deploy RR on a Device**: specifies that the CGW instance acts as an RR of an iBGP neighbor and does not provide server access.

   > **Important**
   >
   > The iBGP role configurations must meet the following networking requirements:
   >
   > - Single-data center deployment: At least one group of CGW instances whose iBGP role is an RR and other devices whose iBGP role is a client are deployed in a single data center.
   >
   > - Multi-data center deployment: One group of CGW instances whose iBGP role is an RR and other devices whose iBGP role is a client are deployed in at least two data centers.
   >
   > - RR role recommendations:
   >
   >   - We recommend that you set the role to Deploy Client and RR on a Device.
   >
   >   - If you have higher network stability requirements, we recommend that you set the role to Deploy RR on a Device.

7. Click **OK**.

**Operation logs**

You can view records and results of CGW API operations that are called by the bare metal controller or Apsara Uni-manager Operations Console based on your O&M requirements.

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **Operation Logs** tab.

5. Optional. Select **Start/End Time** and configure the start time and end time.

6. View the operation logs.

   | Parameter | Description |
   | --- | --- |
   | ID | The ID of the API operation log. |
   | Bare Metal Name | The name of the bare metal instance that was applied for or released in the VPC. |
   | Created At | The time when the API operation was performed. |
   | API Operation | The category of the API operation. Valid values:<br>• <strong>add</strong>: specifies that a bare metal instance is applied for in the VPC.<br>• <strong>del</strong>: specifies that a bare metal instance is released in the VPC.<br>• <strong>del_pc</strong>: specifies that an Express Connect circuit is deleted.<br>• <strong>del_vbr</strong>: specifies that a virtual border router (VBR) is deleted.<br>• <strong>del_router_intf</strong>: specifies that a router interface is deleted.<br>• <strong>del_route_entry</strong>: specifies that a route entry is deleted. |
   | Vswitch ID | The ID of the dedicated vSwitch when the bare metal instance is applied for or released in the VPC. |
   | Cloud Gateway Name | The name of the CGW instance involved with the API operation. |
   | Port | The port to which the bare metal instance is connected. |
   | Status | The status of the API operation.<br>• <strong>success</strong>: The API operation was successful.<br>• If the API operation is in progress, the value indicates the real-time status of the API operation.<br>• If the API operation is complete but the value is not <strong>success</strong>, you can view the failure information in this column. Example: create vpc connection fail. |

7. Find the operation log that you want to view and click **Details** in the **Actions** column to view the details, including the region ID, initiator, and HTTP status code.

**Network management of bare metal instances**

**Create a bare metal instance and connect it to a VPC**

Create a bare metal instance and connect it to a VPC based on your O&M requirements. After the bare metal instance is connected to the VPC, the bare metal instance can communicate with other resources in the VPC over a private network.

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **Bare Metal Network Management** tab.

5. On the Bare Metal Network Management tab, click **Create Bare Metal Instance**. In the Create Bare Metal Instance dialog box, configure the **Bare Metal Name**, **SN**, and **Description** parameters and click **OK**.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/cc895df759b3d52011f81267eb5f8670.webp)

6. Find the bare metal instance that you created and click **Connect to VPC** in the **Actions** column. In the Connect to VPC dialog box, configure the parameters that are described in the following table and click **OK**.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/08fde7aa619b6e84ab2297726ae7612a.webp)

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Bare Metal Name</td>
       <td>The name of the bare metal instance. You do not need to configure this parameter.</td>
     </tr>
     <tr>
       <td>Bare Metal SN</td>
       <td>The serial number of the bare metal instance. You do not need to configure this parameter.</td>
     </tr>
     <tr>
       <td>AK</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs. For more information, see <strong>Manage the AccessKey pairs of</strong> <strong>an organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>SK</td>
     </tr>
     <tr>
       <td>Vswitch ID</td>
       <td>The ID of the dedicated vSwitch to which the bare metal instance is connected.</td>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The ID of the region in which the environment resides.</td>
     </tr>
     <tr>
       <td>Cloud Gateway Name</td>
       <td>The name of the CGW instance to which the bare metal instance is connected.</td>
     </tr>
     <tr>
       <td>Port</td>
       <td>The port of the CGW instance to which the bare metal instance is connected.</td>
     </tr>
     <tr>
       <td>Bare Metal Description</td>
       <td>The description of the bare metal instance.</td>
     </tr>
   </table>

**View the network information about a bare metal instance in a VPC**

1. On the **Bare Metal Network Management** tab, click **Advanced Filter** and filter bare metal instances by specifying the following conditions: **Start and End Time**, **Bare Metal Name**, **VPC ID**, **Vswitch ID**, **VBR ID**, **BD ID**, and **Cloud Gateway Name**.

2. View the network information about the bare metal instance that meets the filter conditions.

   | Parameter | Description |
   | --- | --- |
   | Bare Metal Name | The name of the bare metal instance. |
   | SN | The serial number of the bare metal instance. |
   | VPC ID | The ID of the VPC to which the bare metal instance belongs. |
   | Vswitch ID | The ID of the dedicated vSwitch to which the bare metal instance is connected. |
   | Cloud Gateway Name | The name of the CGW instance to which the bare metal instance is connected. |
   | Port | The port of the CGW instance to which the bare metal instance is connected. |
   | VBR ID | The VBR ID of the Express Connect circuit created on the HSW by the VPC to which the bare metal instance belongs. |
   | BD ID | The value of the hardware bridge-domain (BD) to which the bare metal instance is added. |
   | Created At | The time when the bare metal network was created. |
   | Bare Metal IP Address | The IP address of the bare metal instance. Click <strong>Manage</strong> in the Bare Metal IP Address column to assign an IP address to the bare metal instance. This helps you configure the network of bare metal instances. For more information, see the Manage the IP address of a bare metal instance section of this topic. |

3. Find the bare metal instance and click **Details** in the **Actions** column to view the details of the bare metal instance, such as the ID of the Express Connect circuit, VPC router interface, and VBR interface.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/810500f9584b27e876d1cb7f57acfab4.webp)

**Disconnect a bare metal instance from a VPC**

After a bare metal instance is disconnected from a VPC, access isolation of resources can be implemented.

**Procedure**

Find the bare metal instance and click **Close the Connection to VPC** or **Delete Instance** in the Actions column.

- Click **Close the Connection to VPC** in the **Actions** column to disconnect the bare metal instance from the VPC.

  > **Note**
  >
  > The Close the Connection to VPC option appears only after the bare metal instance is connected to a VPC.

- Click **Delete Instance** in the Actions column to disconnect the bare metal instance from the VPC and delete the bare metal instance.

  > **Note**
  >
  > The Delete Instance option appears only for bare metal instances created on the Bare Metal Network Management page.

**Manage the IP address of a bare metal instance**

In the Bare Metal IP Address Management panel, you can assign an IP address to a bare metal instance. This helps you configure the network of bare metal instances.

**Background information**

CGW works with Bare-metal Management Service (BMS). BMS is used to install bare metal instances, assign IP addresses, and complete network configurations. CGW is used to connect bare metal instances to VPCs.

In some scenarios, you may not install bare metal instances or complete network configurations by using BMS, but you must use CGW to connect bare metal instances to VPCs. In such scenarios, the system cannot assign IP addresses to bare metal instances, and you must manually maintain IP address assignment results. This may cause IP address conflicts and poor usability. Therefore, network management of bare metal instances is supported on the Cloud Gateway page. You can manage IP addresses of bare metal instances in the Bare Metal IP Address Management panel.

**Prerequisites**

A bare metal instance is connected to a VPC.

**Procedure**

1. Find the bare metal instance and click **Manage** in the **Bare Metal IP Address** column.

2. In the **Bare Metal IP Address Management** panel, click **Apply for Bare Metal IP Address**.

3. In the **Apply for Bare Metal IP Address** dialog box, configure the **Bare Metal NIC**, **IP**, and **IP Address Description** parameters and click **OK**.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/1e0d2dd7ef27e2f3b70d6e47fc221fda.webp)

   > **Note**
   >
   > If you do not specify the IP parameter, an IP address is automatically generated.

4. After you apply for an IP address for a bare metal instance, view the IP address in the **Bare Metal IP Address Management** panel.

   - Find the IP address of the bare metal instance and click **Edit** to change the IP address.

   - Find the IP address of the bare metal instance and click **Release** to release the IP address.

**O&M configurations**

**Apply for a bare metal instance in a VPC**

In O&M emergency scenarios, you can use this feature to add the physical port of the CGW instance associated with a bare metal instance to the VPC.

> **Warning**
>
> - This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.
>
> - This feature can only be used to connect the bare metal instance to the CGW instance port but cannot be used to perform operations on the bare metal instance. To configure the network port, IP address, and routing information of the bare metal instance, contact the corresponding product team for guidance.
>
> - Typically, you cannot use this feature to apply for a bare metal instance in the VPC. You can use the bare metal controller to call an API operation to enable the bare metal network.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **Apply for Bare Metal in VPC** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/e0ea914638ac323f342fe41dd4f57823.webp)

6. Configure the parameters that are described in the following table.

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The ID of the region in which the environment resides.</td>
     </tr>
     <tr>
       <td>Cloud Gateway Name</td>
       <td>The name of the CGW instance to which the bare metal instance is connected.</td>
     </tr>
     <tr>
       <td>Vswitch ID</td>
       <td>The ID of the vSwitch to which the bare metal instance is to be added. You can obtain the vSwitch ID from the VPC console of the Apsara Uni-manager Management Console.</td>
     </tr>
     <tr>
       <td>Port</td>
       <td>The port of the CGW instance to which the bare metal instance is connected.</td>
     </tr>
     <tr>
       <td>AK</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs.<br>For more information, see <strong>Manage the AccessKey pairs of an</strong> <strong>organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>SK</td>
     </tr>
     <tr>
       <td>Bare Metal Name</td>
       <td>The name of the bare metal instance that you want to apply for. The name must be unique.</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

7. Click **Next**.

8. Check the information. If the information is correct, click **Confirm**.

   After the configurations are delivered, the **Result: Successful** message appears, and you can search for the bare metal instance by bare metal instance name on the **Bare Metal Network Management** tab. If the bare metal instance is displayed, it is connected to the VPC.

**Release a bare metal instance in a VPC**

In O&M emergency scenarios, you can use this feature to disconnect the physical port of the CGW instance associated with a bare metal instance from the VPC.

> **Warning**
>
> - This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.
>
> - This feature can only be used to connect the bare metal instance to the CGW instance port but cannot be used to perform operations on the bare metal instance. To configure the network port, IP address, and routing information of the bare metal instance, contact the corresponding product team for guidance.
>
> - Typically, you cannot use this feature to release a bare metal instance in the VPC. You can use the bare metal controller to call an API operation to delete the bare metal network.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **Release Bare Metal in VPC** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/c185018347d7df090bea5aab74e217d3.webp)

6. Configure the parameters that are described in the following table.

   | Parameter | Description |
   | --- | --- |
   | Region ID | The ID of the region in which the environment resides. |
   | Bare Metal Name | The name of the bare metal instance that you want to release.<br>You can obtain the name of the bare metal instance on the <strong>Bare</strong> <strong>Metal Network Management</strong> tab. |

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

7. Click **Next**.

8. Check the information. If the information is correct, click **Confirm**.

   After the configurations are delivered, the **Result: Successful** message appears, and you can search for the bare metal instance by bare metal instance name on the **Bare Metal Network Management** tab. If the bare metal instance is not displayed, it is released in the VPC.

**Delete a route entry**

In O&M emergency scenarios, you can use this feature to delete route entries that point to the bare metal subnet in the VPC and the default route entries of a VBR.

> **Warning**
>
> - This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.
>
> - Typically, you cannot use this feature to delete a VPC route entry. This operation is only for emergency scenarios.
>
> - You can perform this operation to delete only one route entry at a time. To delete multiple route entries, you must perform this operation multiple times.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **Delete Route Table Entry** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/86af836b7ce1c7a75c26a59ba24eb35d.webp)

6. Configure the parameters that are described in the following table.

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description about deleting a VPC route entry</th>
       <th>Description about deleting a VBR route entry</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The ID of the region in which the environment resides.</td>
       <td>The ID of the region in which the environment resides.</td>
     </tr>
     <tr>
       <td>Route Table ID</td>
       <td>The ID of the VPC route table, which can be obtained from the VPC console. For more information about how to obtain the ID of a VPC route table, see <strong>VPC</strong> <strong>User Guide</strong>.</td>
       <td>The ID of the VBR route table.<br>If the bare metal instance involved with the VBR is connected to a VPC, you can search for the bare metal instance by bare metal instance name on the <strong>Bare</strong> <strong>Metal Network Management</strong> tab, and then click Details in the Actions column. The value of the VBR Route Table ID parameter in the details is the value of this parameter.<br>If the bare metal instance involved with the VBR fails to be connected to a VPC, specify the name and creation time of the bare metal instance to search for the operation logs and find an operation log whose <strong>API Operation</strong> is <strong>add</strong> on the <strong>Operation Logs</strong> tab. Click <strong>Details</strong> in the Actions column. The value of the VBR Route Table ID parameter in the details is the value of this parameter.</td>
     </tr>
     <tr>
       <td>Router Interface ID</td>
       <td>The ID of the VPC router interface, which can be obtained from the VPC console. For more information about how to obtain the ID of a VPC router interface, see <strong>VPC User Guide</strong>.</td>
       <td>The ID of the VBR interface.<br>If the bare metal instance involved with the VBR is connected to a VPC, you can search for the bare metal instance by bare metal instance name on the <strong>Bare</strong> <strong>Metal Network Management</strong> tab, and then click Details in the Actions column. The value of the VBR Router Interface parameter in the details is the value of this parameter.<br>If the bare metal instance involved with the VBR fails to be connected to a VPC, specify the name and creation time of the bare metal instance to search for the operation logs and find an operation log whose <strong>API Operation</strong> is <strong>add</strong> on the <strong>Operation Logs</strong> tab. Click Details in the Actions column. The value of the VBR Router Interface parameter in the details is the value of this parameter.</td>
     </tr>
     <tr>
       <td>Routing Destinatio n CIDR</td>
       <td>The destination CIDR block to which the VPC points, which can be obtained from the VPC console. For more information about how to obtain a destination CIDR block, see <strong>VPC User Guide</strong>.</td>
       <td>Set the value to 0.0.0.0/0.</td>
     </tr>
     <tr>
       <td>AK</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs.For more information, see <strong>Manage the</strong> AccessKey pairs of an organization in Apsara Uni-manager Management Console User Guide.</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VBR belongs. For more information, see <strong>Manage the</strong> AccessKey pairs of an organization in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>SK</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

7. Click **Next**.

8. Check the information. If the information is correct, click **Confirm**.

   The system begins to deliver the configurations. After the configurations are delivered, the **Result: Successful** message appears.

9. Optional. In actual fault scenarios, if multiple route entries exist in the route table, repeat Step 5 to Step 8 to delete other route entries.

**Delete a router interface**

In O&M emergency scenarios, you can use this feature to delete a VPC router interface and a VBR interface.

> **Warning**
>
> This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **Delete Router Interface** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/2214d35143b45e5a78210ad9c078fc1b.webp)

6. Configure the parameters that are described in the following table.

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description about deleting a VPC router interface</th>
       <th>Description about deleting a VBR interface</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The ID of the region in which the environment resides.</td>
       <td>The ID of the region in which the environment resides.</td>
     </tr>
     <tr>
       <td>Router Interface ID</td>
       <td>The ID of the VPC router interface. On the <strong>Operation Logs</strong> tab, specify the name and creation time of the bare metal instance to search for the operation logs and find an operation log whose <strong>API Operation</strong> is <strong>add</strong>.Click Details in the Actions column.The value of the <strong>VPC Router</strong> <strong>Interface</strong> parameter in the details is the value of this parameter.</td>
       <td>The ID of the VBR interface.<br>If the bare metal instance involved with the VBR is connected to a VPC, you can search for the bare metal instance by bare metal instance name on the <strong>Bare</strong> <strong>Metal Network Management</strong> tab, and then click Details in the Actions column.The value of the VBR Router Interface parameter in the details is the value of this parameter.<br>If the bare metal instance involved with the VBR fails to be connected to a VPC, specify the name and creation time of the bare metal instance to search for the operation logs and find an operation log whose <strong>API Operation</strong> is <strong>add</strong> on the <strong>Operation Logs</strong> tab. Click Details in the Actions column. The value of the VBR Router Interface parameter in the details is the value of this parameter.</td>
     </tr>
     <tr>
       <td>AK</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs. For more information, see Manage the AccessKey pairs of <strong>an organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VBR belongs. For more information, see <strong>Manage the</strong> AccessKey pairs of an organization in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>SK</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

7. Click **Next**.

8. Check the information. If the information is correct, click **Confirm**.

   The system begins to deliver the configurations. After the configurations are delivered, the **Result: Successful** message appears.

   After the configurations are delivered, you can choose **Product Operation** > **Networking** > **Network Intelligence** in the navigation bar of the Apsara Uni-manager Operations Console. On the homepage of Apsara Network Intelligence, enter the ID of the router interface to search for the router interface. If no search result appears, the router interface is deleted.

**Delete a VBR**

In O&M emergency scenarios, you can use this feature to delete a VBR.

> **Warning**
>
> This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **Delete VBR** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/e97718b5d1ac3b0cd09185f0f9efffcc.webp)

6. Configure the parameters that are described in the following table.

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The ID of the region in which the environment resides.</td>
     </tr>
     <tr>
       <td>VBR ID</td>
       <td>The ID of the VBR that you want to delete. On the <strong>Operation Logs</strong> tab, specify the name and creation time of the bare metal instance to search for the operation logs and find an operation log whose <strong>API Operation</strong> is <strong>add</strong>. Click Details in the Actions column. The value of the VBR ID parameter in the details is the value of this parameter.</td>
     </tr>
     <tr>
       <td>AK</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VBR belongs. For more information, see <strong>Manage the AccessKey pairs of</strong> <strong>an organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>SK</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

7. Click **Next**.

8. Check the information. If the information is correct, click **Confirm**.

   The system begins to deliver the configurations. After the configurations are delivered, the **Result: Successful** message appears.

   After the configurations are delivered, you can choose **Product Operation** > **Networking** > **Network Intelligence** in the navigation bar of the Apsara Uni-manager Operations Console. On the homepage of Apsara Network Intelligence, enter the ID of the VBR to search for the VBR. If no search result appears, the VBR is deleted.

**Delete an Express Connect circuit**

In O&M emergency scenarios, you can use this feature to delete an Express Connect circuit.

> **Warning**
>
> This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **Delete Express Connect Circuit** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/0f8ad5b6ce339afc0706c9a56b3d1342.webp)

6. Configure the parameters that are described in the following table.

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The ID of the region in which the environment resides.</td>
     </tr>
     <tr>
       <td>Express Connect Circuit ID</td>
       <td>The ID of the Express Connect circuit that you want to delete. On the <strong>Operation Logs</strong> tab, specify the name and creation time of the bare metal instance to search for the operation logs and find an operation log whose <strong>API Operation</strong> is <strong>add</strong>. Click <strong>Details</strong> in the Actions column. The value of the Express Connect Circuit ID parameter in the details is the value of this parameter.</td>
     </tr>
     <tr>
       <td>AK</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VBR belongs. For more information, see <strong>Manage the AccessKey pairs of</strong> <strong>an organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>SK</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

7. Click **Next**.

8. Check the information. If the information is correct, click **Confirm**.

   The system begins to deliver the configurations. After the configurations are delivered, the **Result: Successful** message appears.

   After the configurations are delivered, you can choose **Product Operation** > **Networking** > **Network Intelligence** in the navigation bar of the Apsara Uni-manager Operations Console. On the homepage of Apsara Network Intelligence, enter the ID of the Express Connect circuit to search for the Express Connect circuit. If no search result appears, the Express Connect circuit is deleted.

**Delete all resources**

In O&M emergency scenarios, you can use this feature to delete all resources, including VPC route entries, VBR route entries, VPC router interfaces, VBR interfaces, VBRs, and Express Connect circuits.

> **Warning**
>
> This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **Delete ALL Resources** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/a10f99cd9b716a47d2b741a73ecc0752.webp)

6. Configure the parameters that are described in the following table.

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The ID of the region in which the environment resides.</td>
     </tr>
     <tr>
       <td>Cloud Gateway Name</td>
       <td>The name of the CGW instance to which the bare metal instance is connected.</td>
     </tr>
     <tr>
       <td>AK</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VBR belongs. For more information, see <strong>Manage the AccessKey pairs of</strong> <strong>an organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>SK</td>
     </tr>
     <tr>
       <td>VPC Router Interface ID</td>
       <td>The ID of the VPC router interface, which can be obtained from the VPC console. For more information about how to obtain the ID of a VPC router interface, see <strong>VPC User Guide</strong>.</td>
     </tr>
     <tr>
       <td>VPC Route Table ID</td>
       <td>The ID of the VPC route table, which can be obtained from the VPC console. For more information about how to obtain the ID of a VPC route table, see <strong>VPC User Guide</strong>.</td>
     </tr>
     <tr>
       <td>VBR Route Table ID</td>
       <td>The ID of the VBR route table.<br>If the bare metal instance involved with the VBR is connected to a VPC, you can search for the bare metal instance by bare metal instance name on the <strong>Bare Metal Network Management</strong> tab, and then click Details in the Actions column. The value of the <strong>VBR Route</strong> <strong>Table ID</strong> parameter in the details is the value of this parameter.<br>If the bare metal instance involved with the VBR fails to be connected to a VPC, specify the name and creation time of the bare metal instance to search for the operation logs and find an operation log whose <strong>API Operation</strong> is <strong>add</strong> on the <strong>Operation Logs</strong> tab. Click <strong>Details</strong> in the Actions column. The value of the VBR Route Table ID parameter in the details is the value of this parameter.</td>
     </tr>
     <tr>
       <td>VPC CIDR1</td>
       <td>The destination CIDR block 1 to which the VPC points, which can be obtained from the VPC console. For more information about how to obtain a destination CIDR block, see <strong>VPC User Guide</strong>.</td>
     </tr>
     <tr>
       <td>VPC CIDR2</td>
       <td>The destination CIDR block 2 to which the VPC points, which can be obtained from the VPC console. For more information about how to obtain a destination CIDR block, see <strong>VPC User Guide</strong>.</td>
     </tr>
     <tr>
       <td>VBR Router Interface ID</td>
       <td>The ID of the VBR interface.<br>If the bare metal instance involved with the VBR is connected to a VPC, you can search for the bare metal instance by bare metal instance name on the <strong>Bare Metal Network Management</strong> tab, and then click Details in the Actions column. The value of the <strong>VBR Router</strong> <strong>Interface</strong> parameter in the details is the value of this parameter.<br>If the bare metal instance involved with the VBR fails to be connected to a VPC, specify the name and creation time of the bare metal instance to search for the operation logs and find an operation log whose <strong>API Operation</strong> is <strong>add</strong> on the <strong>Operation Logs</strong> tab. Click Details in the Actions column. The value of the <strong>VBR Router Interface</strong> in the details is the value of this parameter.</td>
     </tr>
     <tr>
       <td>VBR ID</td>
       <td>The ID of the VBR that you want to delete. On the <strong>Operation Logs</strong> tab, specify the name and creation time of the bare metal instance to search for the operation logs and find an operation log whose <strong>API</strong> <strong>Operation</strong> is <strong>add</strong>. Click Details in the Actions column. The value of the <strong>VBR ID</strong> parameter in the details is the value of this parameter.</td>
     </tr>
     <tr>
       <td>Express Connect Circuit ID</td>
       <td>The ID of the Express Connect circuit that you want to delete. On the <strong>Operation Logs</strong> tab, specify the name and creation time of the bare metal instance to search for the operation logs and find an operation log whose <strong>API Operation</strong> is <strong>add</strong>. Click Details in the Actions column.The value of the <strong>Express Connect Circuit ID</strong> parameter in the details is the value of this parameter.</td>
     </tr>
     <tr>
       <td>Trunk ID</td>
       <td>You do not need to specify this parameter.</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

7. Click **Next**.

8. Check the information. If the information is correct, click **Confirm**.

   The system begins to deliver the configurations. After the configurations are delivered, the **Result: Successful** message appears.

**View the bandwidth of an Express Connect circuit**

You can view the bandwidth of the Express Connect circuit to which a router interface corresponds based on your O&M requirements when a CGW instance is connected to a VPC in the system.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **View Express Connect Circuit Bandwidth** from the drop-down list in the upper-left corner of the tab.

6. Configure the parameters that are described in the following table and click **Query**. The system displays the bandwidth of the Express Connect circuit that meets the filter conditions.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/2a74e9945571628662b774462632512c.webp)

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The ID of the region in which the environment resides.</td>
     </tr>
     <tr>
       <td>Router Interface ID</td>
       <td>The ID of the VBR interface. On the <strong>Bare Metal Network Management</strong> tab, specify a VPC ID and CGW instance name. Click <strong>Details</strong> in the Actions column. The value of the VBR Router Interface parameter in the details is the value of this parameter.</td>
     </tr>
     <tr>
       <td>AK</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VBR belongs.For more information, see <strong>Manage the AccessKey pairs of an</strong> <strong>organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>SK</td>
     </tr>
   </table>

7. View the table on the left and obtain the bandwidth in units of bit/s based on the specifications. The bandwidth information describes the specifications of the Express Connect circuit bandwidth on the HSW of the current VPC.

   | Specifications | Bandwidth (unit: bit/s) |
   | --- | --- |
   | Large.1 | 1G |
   | Large.2 | 2G |
   | Large.4 | 4G |
   | Large.5 | 5G |
   | Xlarge.1 | 10G |
   | Xlarge.2 | 20G |
   | Xlarge.4 | 40G |
   | Xlarge.5 | 50G |
   | Xlarge.8 | 80G |
   | Xlarge.10 | 100G |
   | Xlarge.16 | 160G |
   | Xlarge.20 | 200G |
   | Xlarge.50 | 500G |
   | Xlarge.320 | 3200G |

**Change the bandwidth of an Express Connect circuit**

In O&M emergency scenarios, you can use this feature to change the bandwidth of an Express Connect circuit.

> **Warning**
>
> This operation may affect your business. Unauthorized operations are prohibited. Configuration changes must be performed under the guidance of technical support.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **Change Express Connect Circuit Bandwidth** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/4869f81ab39ec9003f4a4ff9166d655f.webp)

6. Configure the parameters that are described in the following table and click **Next**.

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The ID of the region in which the environment resides.</td>
     </tr>
     <tr>
       <td>Router Interface ID</td>
       <td>The ID of the VBR interface. On the <strong>Bare Metal Network Management</strong> tab, specify a VPC ID and CGW instance name. Click <strong>Details</strong> in the Actions column. The value of the VBR Router Interface parameter in the details is the value of this parameter.</td>
     </tr>
     <tr>
       <td>Router Interface Specifications</td>
       <td>The specifications of the Express Connect circuit bandwidth.</td>
     </tr>
     <tr>
       <td>AK</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VBR belongs.For more information, see <strong>Manage the AccessKey pairs of an</strong> <strong>organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>SK</td>
     </tr>
   </table>

7. Check whether the parameter configurations are valid.

   - If yes, click **Confirm**. After the configurations are delivered, check whether the bandwidth of the Express Connect circuit is changed by referring to the View the bandwidth of an Express Connect circuit section of this topic.

   - If not, click **Back to Modify** to configure the parameters again.

**View trunk usage**

You can view trunk usage to obtain up-to-date information about the usage of hardware ports in a timely manner.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **View Trunk Usage** from the drop-down list in the upper-left corner of the tab.

6. Specify a trunk ID and CGW instance name, select a trunk state, and then click **Search** to view trunk usage. Valid values of the **Status** parameter are **Idle**, **Used**, **Creating**, and **Deleting**.

   > **Note**
   >
   > Specify the last integer of the value of the **Port** parameter that is obtained from the **Bare Metal Network Management** tab as a trunk ID. For example, if the value of the Port parameter is 10GE1/0/40, specify 40 as a trunk ID.

**View VPN usage of a bare metal instance**

You can view the VPN usage of a bare metal instance, and the VPN is assigned to a CGW instance.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **View BM VPN Usage** from the drop-down list in the upper-left corner of the tab.

6. Specify the name of a CGW instance, a Virtual Extensible Local Area Network (VXLAN) ID, and the VPN name of a bare metal instance, select a state, and then click **Search** to view the bare metal instance VPNs assigned to all the HSWs. Valid values of the **Status** parameter are **Succeeded** and **Creating**.

**View BD usage**

You can view BD usage to learn about the BD configuration distribution in a timely manner.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **View BD Usage** from the drop-down list in the upper-left corner of the tab.

6. Specify a CGW instance name, BD ID, and vSwitch ID, select a state, and then click **Search** to view BD usage. Valid values of the **Status** parameter are **Succeeded**, **Creating**, and **Deleting**.

**Check initialization configurations**

In O&M emergency scenarios, you can use this feature to check whether the initialization configurations of the HSW are successful.

> **Note**
>
> This feature only checks the initialization status of the platform access gateway vSwitch and whether the initialization configurations are successful. No operation is performed on the bare metal instance.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **Check the Initialization Configuration** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/91bcfb15860ead1d6f91d8a9adb23db9.webp)

6. Configure the parameters that are described in the following table.

   | Parameter | Description |
   | --- | --- |
   | Region ID | The ID of the region in which the environment resides. |
   | HSW Name | The name of the vSwitch to be checked in instance management. |

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

7. After you specify the parameters, click **Next** and click **Check** to check the initialization configurations of the vSwitch.

**Check route configurations**

In O&M emergency scenarios, you can use this feature to locate abnormal operations and check whether the route configurations of a bare metal instance are valid.

**Background information**

You can use this operation to locate the exception and scan the HSW after a bare metal instance fails to be added. This feature only checks whether the route configurations of the bare metal instance are valid. No operation is performed on the bare metal instance.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **Check the Route Configuration** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/6193d165783ba21adf3485a402c56511.webp)

6. Configure the parameters that are described in the following table.

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The ID of the region in which the environment resides.</td>
     </tr>
     <tr>
       <td>Bare Metal Name</td>
       <td>The name of the bare metal instance that was applied for or released in a VPC. It uniquely identifies the bare metal instance within a region.</td>
     </tr>
     <tr>
       <td>AK</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VBR belongs.For more information, see <strong>Manage the AccessKey pairs of an</strong> <strong>organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>SK</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

7. After you specify the parameters, click **Next** and click **Check** to check the route configurations.

**Display the information about a bare metal network gateway**

In O&M emergency scenarios, you can use this feature to check the gateway of a vSwitch.

**Background information**

This operation is only for emergency scenarios in which the bare metal network is inaccessible. This operation is used to check the vSwitch gateway information and has no impact on the bare metal instance.

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network** > **Cloud Gateways**.

4. On the Cloud Gateway page, click the **O&M Settings** tab.

5. Select **Display the Information of Bare Metal Network Gateways** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/a3c661b23b558d3c710bb27ba2d164a2.webp)

6. Configure the parameters that are described in the following table.

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The ID of the region in which the environment resides.</td>
     </tr>
     <tr>
       <td>Vswitch ID</td>
       <td>The ID of the vSwitch. You can obtain the vSwitch ID from the VPC console.</td>
     </tr>
     <tr>
       <td>AK</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs.For more information, see <strong>Manage the AccessKey pairs of an</strong> <strong>organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>SK</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

7. After you configure the parameters, click **Next** and click **Check** to check the information about the bare metal network gateway.

<a id="section-2-4"></a>

## 2.4. Computing access gateways

You can use computing access gateways such as dedicated computing host switches (CHSWs) to connect intelligent computing servers to virtual private clouds (VPCs). This helps implement the centralized management of intelligent computing servers. The system supports operations such as instance management, operation log management, VPC management and Express Connect circuit management of bare metal instances, and O&M configurations to complete routine O&M operations on computing access gateways.

> **Note**
>
> By default, the Computing Access Gateway module is not displayed in the left-side navigation pane. To use this module, click **User Authorities** in the top navigation bar of the Apsara Uni-manager Operations Console. In the left-side navigation pane of the page that appears, click **Menu Management**. On the Menus page, find Computing Access Gateway and click Modify in the Actions column. In the Modify Menu panel, turn on **Show**.

**Manage access gateways**

On the Instance Management tab, you can view information about computing access gateways, such as the computing access gateway name, internal Border Gateway Protocol (IBGP) role, and creation time.

**Display devices**

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation > Networking > Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > Computing Access Gateway**.

4. On the **Computing Access Gateway** page, click the **Instance Management** tab.

5. On the **Display Devices** tab, view the information about computing access gateways.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/0990839ad2e25b0bbc9f4b344d893ed8.webp)

   | Parameter | Description |
   | --- | --- |
   | Computing Access Gateway Name | The name of the computing access gateway. |
   | IBGP Role | The role of the computing access gateway in the environment. |
   | Manage IP Address | The IP address of the computing access gateway. |
   | Manufacturer | The manufacturer of the computing access gateway. |
   | Model | The model of the computing access gateway. |
   | Management Status | The initialization status of the computing access gateway.<br>• Uninitialized<br>• Initializing<br>• Initialized |
   | Authorization Status | The authorization status of the computing access gateway.<br>• Unauthorized<br>• Authorized<br>Note<br>To use computing access gateways, you must plan the number of computing access gateway licenses in Deployment Planner. If the number of computing access gateway licenses in Deployment Planner is less than the number of computing access gateways in use, the computing access gateways without license authorization are in the Unauthorized state. In this case, you need to increase the number of computing access gateway licenses. |
   | Created At | The time when the computing access gateway was created. |

**Scan for new devices**

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation > Networking > Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > Computing Access Gateway**.

4. On the **Computing Access Gateway** page, click the **Instance Management** tab.

5. Click the **Scan for New Devices** tab.

   - **Stacked Networking Devices**

     <ol type="a">

     <li>

     View devices

     On the **Stacked Networking Devices** tab, you can view the following information about devices: **Computing Access Gateway Name**, **Manage IP Address**, **IBGP Role**, **Vendor**, and **Model**.

     </li>

     <li>

     Configure the IBGP role for a device

     <ol type="a">

     <li>

     In the device list, find the device that you want to manage and click **Manage** in the **Actions** column.

     Alternatively, select multiple devices that you want to manage and click **Batch Manage**.

     </li>

     <li>

     Select an IBGP role from the **IBGP Role** drop-down list. Then, click **OK**.

     The IBGP role specifies the role of the computing access gateway in the environment. Valid values: Client, Deploy Client and RR on a Device, and Deploy RR on a Device.

     - **Client**: The computing access gateway serves as the client of the IBGP peer and is used only for server access.

     - **Deploy Client and RR on a Device**: The computing access gateway serves as the RR reflective route of the IBGP peer and is used for server access.

     - **Deploy RR on a Device**: The computing access gateway serves only as the RR reflective route of the IBGP peer and cannot be used for server access.

     > **Important**
     >
     > The following list describes the networking requirements for the IBGP role:
     >
     > - Single-data center deployment: At least one set of computing access gateways is deployed, and the IBGP roles of the computing access gateways are RR roles. The IBGP roles of other devices are Client.
     >
     > - Multi-data center deployment: A set of computing access gateways is deployed in at least two data centers, and the IBGP roles of the computing access gateways are RR roles. The IBGP roles of other devices are Client.
     >
     > - RR role recommendations:
     >
     >   - We recommend that you set the role to Deploy Client and RR on A Device.
     >
     >   - If you have higher network stability requirements, we recommend that you set the role to Deploy RR on a Device.

     </li>

     </ol>

     </li>

     </ol>

   - **Unstacked Networking Devices**

     - Perform the following operations to manage devices.

       Click the **Unstacked Networking Devices** tab. You can view the following information about devices: **Name of Computing Platform Access Gateway 1**, **Management IP Address 1**, **Name of Computing Platform Access Gateway 2**, **Management IP Address 2**, **IBGP Role**, **Vendor**, and **Model**.

     - Configure the IBGP role for a device

       <ol type="a">

       <li>

       In the device list, find the device that you want to manage and click **Manage** in the **Actions** column.

       Alternatively, select multiple devices that you want to manage and click **Batch Manage**.

       </li>

       <li>

       Select an IBGP role from the **IBGP Role** drop-down list. Then, click **OK**.

       The IBGP role specifies the role of the computing access gateway in the environment. Valid values: Client, Deploy Client and RR on a Device, and Deploy RR on a Device.

       - **Client**: The computing access gateway serves as the client of the IBGP peer and is used only for server access.

       - **Deploy Client and RR on a Device**: The computing access gateway serves as the RR reflective route of the IBGP peer and is used for server access.

       - **Deploy RR on a Device**: The computing access gateway serves only as the RR reflective route of the IBGP peer and cannot be used for server access.

       > **Important**
       >
       > The following list describes the networking requirements for the IBGP role:
       >
       > - Single-data center deployment: At least one set of computing access gateways is deployed, and the IBGP roles of the computing access gateways are RR roles. The IBGP roles of other devices are Client.
       >
       > - Multi-data center deployment: A set of computing access gateways is deployed in at least two data centers, and the IBGP roles of the computing access gateways are RR roles. The IBGP roles of other devices are Client.
       >
       > - RR role recommendations:
       >
       >   - We recommend that you set the role to Deploy Client and RR on A Device.
       >
       >   - If you have higher network stability requirements, we recommend that you set the role to Deploy RR on a Device.

       </li>

       </ol>

**Manage operation logs**

To meet O&M requirements, you can view the records and results of API operations that are managed by bare metal instances and called by the Apsara Uni-manager Operations Console. The API records and results are provided by the computing access gateways.

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation > Networking > Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > Computing Access Gateway**.

4. On the **Computing Access Gateway** page, click the **Operation History** tab to view the operation logs.

   Click **Advanced Filter** and filter operation logs by **Start/End Time**, **Bare Metal Name**, **VPC ID**, **vSwitch ID**, **VBR ID**, **BD ID**, **Computing Access Gateway Name**, or any combination of them.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/cd61d17e9eac77e3b190d4ce2b1b2f76.webp)

   | Parameter | Description |
   | --- | --- |
   | ID | The ID of the API operation log entry. |
   | Bare Metal Name | The name of the bare metal instance that was applied for or released in the VPC. |
   | Created At | The time when the API operation was performed. |
   | API Operation | The API operation, such as operations to apply for or release bare metal instances in a VPC. Valid values:<br>• <strong>add</strong>: applies for a bare metal instance in the VPC.<br>• <strong>del</strong>: releases a bare metal instance in the VPC.<br>• <strong>del_pc</strong>: deletes an Express Connect circuit.<br>• <strong>del_vbr</strong>: deletes a virtual border router (VBR).<br>• <strong>del_router_intf</strong>: deletes a router interface.<br>• <strong>del_route_entry</strong>: deletes a route entry. |
   | vSwitch ID | The ID of the dedicated vSwitch when the bare metal instance is applied for or released in the VPC. |
   | Computing Access Gateway Name | The name of the computing access gateway that is involved in the current API operation. |
   | Port | The port to which the bare metal instance is connected. |
   | Status | The status of the API operation.<br>• <strong>success</strong>: The API operation was successful.<br>• If the API operation is in progress, the value indicates the real-time status of the API operation.<br>• If the API operation is complete but the state is not <strong>success</strong>, you can view the failure information in this column. Example: create vpc connection fail. |

5. In the operation history list, find the operation log that you want to view and click **Details** in the **Actions** column. In the panel that appears, view the details of the operation log.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/321ba556dc926e69ed9c4bf31e51a369.webp)

**VPC Management**

Create a bare metal instance and connect it to a VPC based on your O&M requirements. After the bare metal instance is connected to the VPC, the bare metal instance can communicate with other resources in the VPC over a private network.

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation > Networking > Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > Computing Access Gateway**.

4. On the **Computing Access Gateway** page, click the **VPC Management** tab.

5. Click **Create Bare Metal Instance**.

6. In the **Create Bare Metal Instance** dialog box, configure the **Bare Metal Name**, **SN**, and **Description** parameters, and then click **OK**.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/cc895df759b3d52011f81267eb5f8670.webp)

7. On the **Computing Access Gateway** page, view the bare metal instances.

   Click **Advanced Filter** and filter bare metal instances by **Bare Metal Name**, **VPC ID**, **vSwitch ID**, **Computing Access Gateway Name**, or any combination of them.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/6130ca87b79141000370b95f924ed7eb.webp)

   | Parameter | Description |
   | --- | --- |
   | Bare Metal Name | The name of the bare metal instance. |
   | SN | The serial number of the bare metal instance. |
   | Status | The status of the bare metal instance. |
   | VPC ID | The ID of the VPC to which the bare metal instance belongs. |
   | vSwitch ID | The ID of the vSwitch to which the bare metal instance belongs. |
   | Computing Access Gateway Name | The name of the computing access gateway to which the bare metal instance is connected.<br>You can distinguish between stacked networking devices and unstacked networking devices based on Computing Access Gateway Name to perform operations on the devices. |
   | Port | The port of the computing access gateway to which the bare metal instance is connected. |
   | Created At | The time when the network of the bare metal instance was created. |
   | Bare Metal IP Address | The IP address of the bare metal instance. Click <strong>Manage</strong> in the Bare Metal IP Address column to assign an IP address to the bare metal instance. This helps you configure the network of the bare metal instance. For more information, see the Manage the IP address of a bare metal instance section of this topic. |

   - **View the network information about a bare metal instance in a VPC**

     <ol type="a">

     <li>

     In the bare metal instance list, find the bare metal instance that you want to view and click **Details** in the **Actions** column. In the panel that appears, view the details of the bare metal instance.

     ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/df01ba3e311415a2c07587b06fa8acf1.webp)

     </li>

     </ol>

   - **Connect the bare metal instance to a VPC**

     <ol type="a">

     <li>

     In the bare metal instance list, find the bare metal instance that you want to manage and click **Connect to VPC** in the **Actions** column.

     </li>

     <li>

     In the **Connect to VPC** dialog box, configure the following parameters and click **OK**.

     ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/fadf84783f843c2e66d95db5461c20f2.webp)

     <table>
       <tr>
         <th>Parameter</th>
         <th>Description</th>
       </tr>
       <tr>
         <td>Bare Metal Name</td>
         <td>The name of the bare metal instance. You do not need to specify this parameter.</td>
       </tr>
       <tr>
         <td>Bare Metal SN</td>
         <td>The serial number of the bare metal instance. You do not need to specify this parameter.</td>
       </tr>
       <tr>
         <td>AccessKey ID</td>
         <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs. For more information, see <strong>Manage the</strong> <strong>AccessKey pairs of an organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
       </tr>
       <tr>
         <td>AccessKey Secret</td>
       </tr>
       <tr>
         <td>vSwitch ID</td>
         <td>The ID of the dedicated vSwitch to which the bare metal instance is connected.</td>
       </tr>
       <tr>
         <td>Region ID</td>
         <td>The ID of the region in which the current environment resides.</td>
       </tr>
       <tr>
         <td>Computing Access Gateway Name</td>
         <td>The name of the computing access gateway to which the bare metal instance is connected.<br>You can distinguish between stacked networking devices and unstacked networking devices based on Computing Access Gateway Name to perform operations on the devices.</td>
       </tr>
       <tr>
         <td>Port</td>
         <td>The port of the computing access gateway to which the bare metal instance is connected.</td>
       </tr>
       <tr>
         <td>Bare Metal Description</td>
         <td>The description of the bare metal instance.</td>
       </tr>
     </table>

     </li>

     </ol>

   - **Close the Connection to VPC**

     > **Note**
     >
     > - After a bare metal instance is connected to a VPC, you can click **Close the Connection to VPC** to disconnect the bare metal instance from the VPC.
     >
     > - After you disconnect the bare metal instance from the VPC, the connection cannot be recovered. Proceed with caution.

     <ol type="a">

     <li>

     In the bare metal instance list, find the bare metal instance that you want to manage and click **Close the Connection to VPC** in the **Actions** column.

     </li>

     <li>

     In the message that appears, click **Exit**.

     </li>

     </ol>

   - **Delete a bare metal instance**

     > **Note**
     >
     > - You can delete a bare metal instance only if the instance is created on the **VPC Management** page.
     >
     > - After a bare metal instance is connected to a VPC, you can click **Delete Instance** to disconnect the bare metal instance from the VPC and delete the instance.
     >
     > - After you delete a bare metal instance, it cannot be recovered. Proceed with caution.

     <ol type="a">

     <li>

     In the bare metal instance list, find the bare metal instance that you want to delete and click **Delete Instance** in the **Actions** column.

     </li>

     <li>

     In the message that appears, click **Delete**.

     </li>

     </ol>

   - **Manage the IP address of a bare metal instance**

     Computing access gateways work with Bare Metal Management Service (BMS). BMS is used to install bare metal instances, assign IP addresses, and complete network configurations. Computing access gateways are used to connect bare metal instances to VPCs. In some scenarios, you may not install bare metal instances or complete network configurations by using BMS, but you must use computing access gateways to connect bare metal instances to VPCs. In such scenarios, the system cannot assign IP addresses to bare metal instances, and you must manually maintain IP address assignment results. This may cause IP address conflicts and poor usability. Therefore, network management of bare metal instances is supported on the Computing Access Gateway page. You can manage IP addresses of bare metal instances in the Bare Metal IP Address Management panel.

     <ol type="a">

     <li>

     In the bare metal instance list, find the bare metal instance that you want to manage and click **Manage** in the **Bare Metal IP Address** column.

     </li>

     <li>

     In the **Bare Metal IP Address Management** panel, click **Apply for Bare Metal IP Address**.

     </li>

     </ol>

     <ol type="i" start="100">

     <li>

     In the **Apply for Bare Metal IP Address** dialog box, configure the **Bare Metal NIC**, **IP**, and **IP Address Description** parameters and click **OK**.

     ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/1e0d2dd7ef27e2f3b70d6e47fc221fda.webp)

     > **Note**
     >
     > If you leave the **IP** parameter empty, the system automatically generates an IP address.

     </li>

     <li value="500">

     After you apply for an IP address for a bare metal instance, view the IP address in the **Bare Metal IP Address Management** panel. The IP address information includes **ID**, **IP Address**, **Bare Metal Name/SN**, **Bare Metal NIC**, **Created At**, **Modified At**, **Description**, **VPC ID**, and **vswitch id**.

     ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/e278c67fa8ae68959d0f9ad6a1ebfd96.webp)

     - Find the bare metal IP address that you want to manage and click **Edit** in the **Actions** column to modify the **IP** and **IP Address Description** parameters.

     - Find the bare metal IP address that you want to manage and click **Release** in the **Actions** column to release the bare metal IP address.

     </li>

     </ol>

**Private Line Management**

On the Private Line Management tab, you can view the bare metal networks associated with Express Connect Routers (ECRs).

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation > Networking > Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > Computing Access Gateway**.

4. On the **Computing Access Gateway** page, click the **Private Line Management** tab to view the Express Connect circuit information about bare metal instances.

   Click **Advanced Filter** and filter bare metal instances by **vSwitch ID**, **VPC ID**, **Private Line Gateway Name**, or any combination of them.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/e817b0664c991b3c14f5c678fca245d6.webp)

   | Parameter | Description |
   | --- | --- |
   | VPC ID | The ID of the VPC to which the bare metal instance belongs. |
   | vSwitch ID | The ID of the vSwitch to which the bare metal instance belongs. |
   | Status | The status of the bare metal instance. |
   | Name of Private Line Gateway 1 | The name of ECR 1 to which the bare metal instance is connected. |
   | Source IP Address that Probes Gateway 1 | The source IP address of ECR 1. |
   | Name of Private Line Gateway 2 | The name of ECR 2 to which the bare metal instance is connected. |
   | Source IP Address that Probes Gateway 2 | The source IP address of ECR 2. |
   | Created At | The time when the network of the bare metal instance was created. |

   - **View Express Connect circuit details of a bare metal instance**

     In the bare metal instance list, find the bare metal instance that you want to view and click **Details** in the **Actions** column. In the panel that appears, view the Express Connect circuit details of the bare metal instance.

     ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/0d34fc3ff994ec6816bee1d0bacd727f.webp)

   - **Delete an Express Connect circuit for a bare metal instance**

     In the bare metal instance list, find the bare metal instance that you want to manage and click **Delete** in the **Actions** column to delete the Express Connect circuit for the bare metal instance.

**O&M Settings**

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation > Networking > Network Operations Console**.

3. In the left-side navigation pane, choose **Basic Network > Computing Access Gateway**.

4. On the **Computing Access Gateway** page, click the **O&M Settings** tab to perform routine O&M operations.

   **Apply for a bare metal instance in a VPC**

   In O&M emergency scenarios, you can use this feature to add the physical port of the computing access gateway associated with a bare metal instance to the VPC.

   > **Warning**
   >
   > - This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.
   >
   > - This feature can be used only to connect a bare metal instance to the port of a computing access gateway but cannot be used to perform operations on the bare metal instance. To configure the network port, IP address, and routing information of the bare metal instance, contact the corresponding product team for guidance.
   >
   > - In most cases, you cannot use this feature to apply for a bare metal instance in a VPC. You can use the bare metal controller to call an API operation to enable the bare metal network.

   <ol type="i">

   <li>

   Select **Apply for Bare Metal in VPC** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/a81cfd4f1fac9d63f0c08c2563425478.webp)

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The name of the region in which the current environment resides.</td>
     </tr>
     <tr>
       <td>Computing Access Gateway Name</td>
       <td>The name of the computing access gateway to which the bare metal instance is connected.<br>You can distinguish between stacked networking devices and unstacked networking devices based on Computing Access Gateway Name to perform operations on the devices.</td>
     </tr>
     <tr>
       <td>vSwitch ID</td>
       <td>The ID of the vSwitch to which you want to add the bare metal instance. You can obtain the vSwitch ID from the VPC console of the Apsara Uni-manager Management Console.</td>
     </tr>
     <tr>
       <td>Port</td>
       <td>The port of the bare metal instance that is connected to the computing access gateway.</td>
     </tr>
     <tr>
       <td>AccessKey ID</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs.<br>For more information, see <strong>Manage the AccessKey pairs of an</strong> <strong>organization</strong> in <strong>Apsara Uni-manager Management Console User</strong> <strong>Guide</strong>.</td>
     </tr>
     <tr>
       <td>AccessKey Secret</td>
     </tr>
     <tr>
       <td>Bare Metal Name</td>
       <td>The name of the bare metal instance that you want to apply for. The name must be unique.</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

   <ol type="i" start="3">

   <li>

   Check whether the parameter configurations are valid.

   </li>

   </ol>

   - If yes, click **Confirm**. The system starts to apply the configurations.

     After the configurations are applied, the **Result: Successful** message appears.

   - If not, click **Back to Modify** to configure the parameters again.

   <ol type="i" start="4">

   <li>

   Optional. After the configurations are applied, you can search for the bare metal instance by bare metal instance name on the **VPC Management** tab. If the bare metal instance is displayed, it is connected to the VPC.

   </li>

   </ol>

   **Release a bare metal instance from a VPC**

   In O&M emergency scenarios, you can use this feature to disconnect the physical port of the computing access gateway associated with a bare metal instance from a VPC.

   > **Warning**
   >
   > - This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.
   >
   > - This feature can be used only to disconnect a bare metal instance from the port of a computing access gateway but cannot be used to perform operations on the bare metal instance. To configure the network port, IP address, and routing information of the bare metal instance, contact the corresponding product team for guidance.
   >
   > - In most cases, you cannot use the feature to release a bare metal instance in a VPC. You can use the bare metal controller to call an API operation to delete the network of the bare metal instance.

   <ol type="i">

   <li>

   Select **Release Bare Metal in VPC** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/ad55696ed80b70f6e965305bf80244c6.webp)

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   | Parameter | Description |
   | --- | --- |
   | Region ID | The name of the region in which the current environment resides. |
   | Computing Access Gateway Name | The name of the computing access gateway to which the bare metal instance is connected.<br>You can distinguish between stacked networking devices and unstacked networking devices based on Computing Access Gateway Name to perform operations on the devices. |
   | Bare Metal Name | The name of the bare metal instance that you want to release.<br>You can obtain the name of the bare metal instance on the <strong>VPC</strong> <strong>Management</strong> tab. |

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

   <ol type="i" start="3">

   <li>

   Check whether the parameter configurations are valid.

   </li>

   </ol>

   - If yes, click **Confirm**. The system starts to apply the configurations.

     After the configurations are applied, the **Result: Successful** message appears.

   - If not, click **Back to Modify** to configure the parameters again.

   <ol type="i" start="4">

   <li>

   Optional. After the configurations are applied, you can search for the bare metal instance by bare metal instance name on the **VPC Management** tab. If the bare metal instance is not displayed, it is released from the VPC.

   </li>

   </ol>

   **Delete a route entry**

   In O&M emergency scenarios, you can use this feature to delete route entries that point to the subnet of a bare metal instance in a VPC and the default route entries of a VBR.

   > **Warning**
   >
   > - This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.
   >
   > - In most cases, you cannot use this feature to delete a VPC route entry. This operation is only used for emergency scenarios.
   >
   > - You can perform this operation to delete only one route entry at a time. To delete multiple route entries, you must perform this operation multiple times.

   <ol type="i">

   <li>

   Select **Delete Route Table Entry** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/7c5ffe1e88e45055726ec35c1d062d61.webp)

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description about deleting a VPC route entry</th>
       <th>Description about deleting a VBR route entry</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The name of the region in which the current environment resides.</td>
       <td>The name of the region in which the current environment resides.</td>
     </tr>
     <tr>
       <td>Route Table ID</td>
       <td>The ID of the VPC route table, which can be obtained from the VPC console.For more information about how to obtain the ID of a VPC route table, see <strong>VPC User Guide</strong>.</td>
       <td>The ID of the VBR route table.<br>If the bare metal instance associated with the VBR is connected to a VPC, you can search for the bare metal instance by bare metal instance name on the <strong>VPC Management</strong> tab, click Details in the Actions column, and then view the value of the VBR Route Table ID parameter.<br>If the bare metal instance associated with the VBR is not added to the VPC, specify the bare metal instance name and creation time to search for the operation log entry whose <strong>API</strong> <strong>Operation</strong> is <strong>add</strong> on the <strong>Operation</strong> <strong>History</strong> tab. Click Details and view the value of the <strong>VBR Route Table ID</strong> parameter.</td>
     </tr>
     <tr>
       <td>Router Interface ID</td>
       <td>The ID of the VPC router interface, which can be obtained from the VPC console. For more information about how to obtain the ID of a VPC router interface, see <strong>VPC User Guide</strong>.</td>
       <td>The ID of the VBR interface.<br>If the bare metal instance associated with the VBR is added to VPC, you can search for the bare metal instance on the <strong>VPC Management</strong> tab based on the bare metal instance name, and then click Detail to view the value of the VBR Router Interface parameter.<br>If the bare metal instance associated with the VBR is not added to the VPC, specify the bare metal instance name and creation time to search for the operation log entry whose <strong>API</strong> <strong>Operation</strong> is <strong>add</strong> on the <strong>Operation</strong> <strong>History</strong> tab. Click Details and view the value of the VBR Router Interface parameter.</td>
     </tr>
     <tr>
       <td>Routing Destinatio n CIDR</td>
       <td>The destination CIDR block to which the VPC points, which can be obtained from the VPC console. For more information about how to obtain a destination CIDR block, see <strong>VPC User</strong> <strong>Guide</strong>.</td>
       <td>Set the value to 0.0.0.0/0.</td>
     </tr>
     <tr>
       <td>AccessKey ID</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs.For more information, see <strong>Manage</strong> the AccessKey pairs of an <strong>organization</strong> in <strong>Apsara Uni-</strong>manager Management Console <strong>User Guide</strong>.</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VBR belongs.For more information, see <strong>Manage</strong> the AccessKey pairs of an <strong>organization</strong> in <strong>Apsara Uni-</strong>manager Management Console <strong>User Guide</strong>.</td>
     </tr>
     <tr>
       <td>AccessKey Secret</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

   <ol type="i" start="3">

   <li>

   Check whether the parameter configurations are valid.

   </li>

   </ol>

   - If yes, click **Confirm**. The system starts to apply the configurations.

     After the configurations are applied, the **Result: Successful** message appears.

   - If not, click **Back to Modify** to configure the parameters again.

   <ol type="i" start="4">

   <li>

   Optional. In actual fault scenarios, if multiple route entries exist in the route table, repeat Step 5 to Step 8 to delete other route entries.

   </li>

   </ol>

   **Delete a router interface**

   In O&M emergency scenarios, you can use this feature to delete a VPC router interface and a VBR interface.

   > **Warning**
   >
   > This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.

   <ol type="i">

   <li>

   Select **Delete Router Interface** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/344170669724867a9fe9e3993d962421.webp)

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description about deleting a VPC router interface</th>
       <th>Description about deleting a VBR interface</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The name of the region in which the current environment resides.</td>
       <td>The name of the region in which the current environment resides.</td>
     </tr>
     <tr>
       <td>Router Interface ID</td>
       <td>The ID of the VPC router interface.On the <strong>Operation History</strong> tab, specify the name and creation time of the bare metal instance to search for the operation log entry whose <strong>API Operation</strong> is <strong>add</strong>. Click Details in the Actions column and view the value of the <strong>VPC Router Interface</strong> parameter.</td>
       <td>The ID of the VBR interface.<br>If the bare metal instance associated with the VBR is added to VPC, you can search for the bare metal instance on the <strong>VPC Management</strong> tab based on the bare metal instance name, and then click Detail to view the value of the VBR Router Interface parameter.<br>If the bare metal instance associated with the VBR is not added to the VPC, specify the bare metal instance name and creation time to search for the operation log entry whose <strong>API</strong> <strong>Operation</strong> is <strong>add</strong> on the <strong>Operation</strong> <strong>History</strong> tab. Click Details and view the value of the VBR Router Interface parameter.</td>
     </tr>
     <tr>
       <td>AccessKey ID</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs. For more information, see <strong>Manage the</strong> AccessKey pairs of an <strong>organization</strong> in <strong>Apsara Uni-</strong>manager Management Console <strong>User Guide</strong>.</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VBR belongs. For more information, see <strong>Manage the</strong> AccessKey pairs of an organization in <strong>Apsara Uni-manager</strong> <strong>Management Console User Guide</strong>.</td>
     </tr>
     <tr>
       <td>AccessKey Secret</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

   <ol type="i" start="3">

   <li>

   Check whether the parameter configurations are valid.

   </li>

   </ol>

   - If yes, click **Confirm**. The system starts to apply the configurations.

     After the configurations are applied, the **Result: Successful** message appears.

   - If not, click **Back to Modify** to configure the parameters again.

   <ol type="i" start="4">

   <li>

   Optional. After the configurations are applied, you can choose **Product Operation** > **Networking** > **Network Intelligence** in the top navigation bar of the Apsara Uni-manager Operations Console. On the homepage of Apsara Network Intelligence, enter the ID of the router interface to search for the router interface. If no search result appears, the router interface is deleted.

   </li>

   </ol>

   **Delete a VBR**

   In O&M emergency scenarios, you can use this feature to delete a VBR.

   > **Warning**
   >
   > This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.

   <ol type="i">

   <li>

   Select **Delete VBR** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/68965b459949c32c1da6959f9e1939a2.webp)

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The name of the region in which the current environment resides.</td>
     </tr>
     <tr>
       <td>VBR ID</td>
       <td>The ID of the VBR that you want to delete. On the <strong>Operation History</strong> tab, specify the name and creation time of the bare metal instance to search for the operation log entry whose <strong>API Operation</strong> is <strong>add</strong>. Click Details in the Actions column to view the value of the VBR ID parameter.</td>
     </tr>
     <tr>
       <td>AccessKey ID</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VBR belongs. For more information, see <strong>Manage the AccessKey pairs of</strong> <strong>an organization</strong> in <strong>Apsara Uni-manager Management Console</strong> <strong>User Guide</strong>.</td>
     </tr>
     <tr>
       <td>AccessKey Secret</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

   <ol type="i" start="3">

   <li>

   Check whether the parameter configurations are valid.

   </li>

   </ol>

   - If yes, click **Confirm**. The system starts to apply the configurations.

     After the configurations are applied, the **Result: Successful** message appears.

   - If not, click **Back to Modify** to configure the parameters again.

   <ol type="i" start="4">

   <li>

   Optional. After the configurations are applied, you can choose **Product Operation** > **Networking** > **Network Intelligence** in the top navigation bar of the Apsara Uni-manager Operations Console. On the homepage of Apsara Network Intelligence, enter the ID of the VBR to search for the VBR. If no search result appears, the VBR is deleted.

   </li>

   </ol>

   **Delete an Express Connect circuit**

   In O&M emergency scenarios, you can use this feature to delete an Express Connect circuit.

   > **Warning**
   >
   > This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.

   <ol type="i">

   <li>

   Select **Delete Express Connect Circuit** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/86cb5b42234419683dce174010eaf626.webp)

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The name of the region in which the current environment resides.</td>
     </tr>
     <tr>
       <td>Express Connect Circuit ID</td>
       <td>The ID of the Express Connect circuit that you want to delete. On the <strong>Operation History</strong> tab, specify the bare metal instance name and creation time to search for the operation log entry whose <strong>API</strong> <strong>Operation</strong> is <strong>add</strong>. Click <strong>Details</strong> to view the value of the Express Connect Circuit ID parameter.</td>
     </tr>
     <tr>
       <td>AccessKey ID</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs. For more information, see <strong>Manage the AccessKey pairs of</strong> <strong>an organization</strong> in <strong>Apsara Uni-manager Management Console</strong> <strong>User Guide</strong>.</td>
     </tr>
     <tr>
       <td>AccessKey Secret</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

   <ol type="i" start="3">

   <li>

   Check whether the parameter configurations are valid.

   </li>

   </ol>

   - If yes, click **Confirm**. The system starts to apply the configurations.

     After the configurations are applied, the **Result: Successful** message appears.

   - If not, click **Back to Modify** to configure the parameters again.

   <ol type="i" start="4">

   <li>

   Optional. After the configurations are applied, you can choose **Product Operation** > **Networking** > **Network Intelligence** in the top navigation bar of the Apsara Uni-manager Operations Console. On the homepage of Apsara Network Intelligence, enter the ID of the Express Connect circuit to search for the Express Connect circuit. If no search result appears, the Express Connect circuit is deleted.

   </li>

   </ol>

   **Delete all resources**

   In O&M emergency scenarios, you can use this feature to delete all resources, including VPC route entries, VBR route entries, VPC router interfaces, VBR interfaces, VBRs, and Express Connect circuits.

   > **Warning**
   >
   > This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.

   <ol type="i">

   <li>

   Select **Delete ALL Resources** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/002ad0e50077ff63b6c2179f47375b35.webp)

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The ID of the region in which the environment resides.</td>
     </tr>
     <tr>
       <td>Computing Access Gateway Name</td>
       <td>The name of the computing access gateway to which the bare metal instance is connected.</td>
     </tr>
     <tr>
       <td>AccessKey ID</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs. For more information, see <strong>Manage the</strong> <strong>AccessKey pairs of an organization</strong> in <strong>Apsara Uni-manager</strong> <strong>Management Console User Guide</strong>.</td>
     </tr>
     <tr>
       <td>AccessKey Secret</td>
     </tr>
     <tr>
       <td>VPC Router Interface ID</td>
       <td>The ID of the VPC router interface, which can be obtained from the VPC console. For more information about how to obtain the ID of a VPC router interface, see <strong>VPC User Guide</strong>.</td>
     </tr>
     <tr>
       <td>VPC Route Table ID</td>
       <td>The ID of the VPC route table, which can be obtained from the VPC console. For more information about how to obtain the ID of a VPC route table, see <strong>VPC User Guide</strong>.</td>
     </tr>
     <tr>
       <td>VBR Route Table ID</td>
       <td>The ID of the VBR route table.<br>If the bare metal instance associated with the VBR is connected to a VPC, you can search for the bare metal instance by bare metal instance name on the <strong>VPC Management</strong> tab, click Details in the Actions column, and then view the value of the <strong>VBR Route Table ID</strong> parameter.<br>If the bare metal instance associated with the VBR is not added to the VPC, specify the bare metal instance name and creation time to search for the operation log entry whose <strong>API Operation</strong> is <strong>add</strong> on the <strong>Operation History</strong> tab. Click Details and view the value of the <strong>VBR Route Table ID</strong> parameter.</td>
     </tr>
     <tr>
       <td>VPC CIDR1</td>
       <td>The Destination CIDR Block 1 to which the VPC points, which can be obtained from the VPC console. For more information about how to obtain a destination CIDR block, see <strong>VPC User Guide</strong>.</td>
     </tr>
     <tr>
       <td>VPC CIDR2</td>
       <td>The Destination CIDR Block 2 to which the VPC points, which can be obtained from the VPC console. For more information about how to obtain a destination CIDR block, see <strong>VPC User Guide</strong>.</td>
     </tr>
     <tr>
       <td>VBR Router Interface ID</td>
       <td>The ID of the VBR interface.<br>If the bare metal instance associated with the VBR is connected to a VPC, you can search for the bare metal instance by bare metal instance name on the <strong>VPC Management</strong> tab, click Details in the Actions column, and then view the value of the <strong>VBR Router</strong> <strong>Interface</strong> parameter.<br>If the bare metal instance associated with the VBR is not added to the VPC, specify the bare metal instance name and creation time to search for the operation log entry whose <strong>API Operation</strong> is <strong>add</strong> on the <strong>Operation History</strong> tab. Click Details and view the value of the <strong>VBR Router Interface</strong> parameter.</td>
     </tr>
     <tr>
       <td>VBR ID</td>
       <td>The ID of the VBR that you want to delete. On the <strong>Operation</strong> <strong>History</strong> tab, specify the name and creation time of the bare metal instance to search for the operation log entry whose <strong>API Operation</strong> is <strong>add</strong>. Click Details in the Actions column to view the value of the <strong>VBR ID</strong> parameter.</td>
     </tr>
     <tr>
       <td>Express Connect Circuit ID</td>
       <td>The ID of the Express Connect circuit that you want to delete. On the <strong>Operation History</strong> tab, specify the bare metal instance name and creation time to search for the operation log entry whose <strong>API</strong> <strong>Operation</strong> is <strong>add</strong>. Click <strong>Details</strong> to view the value of the Express Connect Circuit ID parameter.</td>
     </tr>
     <tr>
       <td>Trunk ID</td>
       <td>You do not need to specify this parameter.</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

   <ol type="i" start="3">

   <li>

   Check whether the parameter configurations are valid.

   </li>

   </ol>

   - If yes, click **Confirm**. The system starts to apply the configurations.

     After the configurations are applied, the **Result: Successful** message appears.

   - If not, click **Back to Modify** to configure the parameters again.

   **View the bandwidth of an Express Connect circuit**

   You can view the bandwidth of the Express Connect circuit for a router interface when the computing access gateway is connected to a VPC based on your O&M requirements.

   <ol type="i">

   <li>

   Select **View Express Connect Circuit Bandwidth** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/cf2e5c37d18cac6718d95e5ebe60ff86.webp)

   </li>

   <li>

   Configure the following parameters and click **Query**. The system displays the bandwidth

   </li>

   </ol>

   of the Express Connect circuit that meets the filter conditions.

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The name of the region in which the current environment resides.</td>
     </tr>
     <tr>
       <td>Router Interface ID</td>
       <td>The ID of the VBR interface. On the <strong>VPC Management</strong> tab, specify a VPC ID and computing access gateway name and click Search. Click <strong>Details</strong> in the Actions column to view the value of the VBR Router Interface parameter.</td>
     </tr>
     <tr>
       <td>AccessKey ID</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs. For more information, see <strong>Manage the AccessKey pairs of</strong> <strong>an organization</strong> in <strong>Apsara Uni-manager Management Console</strong> <strong>User Guide</strong>.</td>
     </tr>
     <tr>
       <td>AccessKey Secret</td>
     </tr>
   </table>

   <ol type="i" start="3">

   <li>

   View the table on the left and obtain the bandwidth in units of bit/s based on the

   </li>

   </ol>

   specifications. The bandwidth information describes the specifications of the Express Connect circuit bandwidth on the HSW of the current VPC.

   | Specification | Bandwidth (bit/s) |
   | --- | --- |
   | Large.1 | 1G |
   | Large.2 | 2G |
   | Large.4 | 4G |
   | Large.5 | 5G |
   | Xlarge.1 | 10G |
   | Xlarge.2 | 20G |
   | Xlarge.4 | 40G |
   | Xlarge.5 | 50G |
   | Xlarge.8 | 80G |
   | Xlarge.10 | 100G |
   | Xlarge.16 | 160G |
   | Xlarge.20 | 200G |
   | Xlarge.50 | 500G |
   | Xlarge.320 | 3200G |

   **Change the bandwidth of an Express Connect circuit**

   In O&M emergency scenarios, you can use this feature to change the bandwidth of an Express Connect circuit.

   > **Warning**
   >
   > This operation may affect your business. Unauthorized operations are prohibited. Configuration changes must be performed under the guidance of technical support.

   <ol type="i">

   <li>

   Select **Change Express Connect Circuit Bandwidth** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/241787a5341ed5b87b05c28655498420.webp)

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The name of the region in which the current environment resides.</td>
     </tr>
     <tr>
       <td>Router Interface ID</td>
       <td>The ID of the VBR interface. On the <strong>VPC Management</strong> tab, specify a VPC ID and computing access gateway name and click Search. Click <strong>Details</strong> in the Actions column to view the value of the VBR Router Interface parameter.</td>
     </tr>
     <tr>
       <td>Router Interface Specifications</td>
       <td>The new bandwidth of the Express Connect circuit.</td>
     </tr>
     <tr>
       <td>AccessKey ID</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs. For more information, see <strong>Manage the AccessKey pairs of an</strong> <strong>organization</strong> in <strong>Apsara Uni-manager Management Console User</strong> <strong>Guide</strong>.</td>
     </tr>
     <tr>
       <td>AccessKey Secret</td>
     </tr>
   </table>

   <ol type="i" start="3">

   <li>

   Check whether the parameter configurations are valid.

   </li>

   </ol>

   - If yes, click **Confirm**. The system starts to apply the configurations.

     After the configurations are applied, the **Result: Successful** message appears.

   - If not, click **Back to Modify** to configure the parameters again.

   <ol type="i" start="4">

   <li>

   Optional. After the configurations are applied, check whether the bandwidth of the Express Connect circuit is changed. For more information, see the View the bandwidth of an Express Connect circuit section of this topic.

   </li>

   </ol>

   **View trunk usage**

   You can view trunk usage to obtain up-to-date information about the usage of hardware ports.

   <ol type="i">

   <li>

   Select **View Trunk Usage** from the drop-down list in the upper-left corner of the tab.

   </li>

   <li>

   View the trunk usage in the list. By default, all data in the **idle** state is displayed.

   </li>

   </ol>

   Specify a trunk ID and computing access gateway name, select a trunk state, and then click **Search** to view trunk usage. Valid values of the **Status** parameter are **Idle**, **Used**, **Creating**, and **Deleting**.

   > **Note**
   >
   > Specify the last integer of the value of the **Port** parameter that is obtained from the **VPC Management** tab as the **trunk ID**. For example, if the value of the Port parameter is 10GE1/0/40, specify 40 as the **trunk ID**.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/98f1798da8d5179a470cec18022fa0e0.webp)

   **View VPN usage of a bare metal instance**

   You can view the VPN usage of a bare metal instance and the VPN assigned to a computing access gateway.

   <ol type="i">

   <li>

   Select **View BM VPN Usage** from the drop-down list in the upper-left corner of the tab.

   </li>

   <li>

   In the list, view the bare metal instance VPNs assigned to all the HSWs. By default, all

   </li>

   </ol>

   data in the **Succeeded** state is displayed.

   Specify the **name of a computing access gateway**, a **Virtual Extensible Local Area Network (VXLAN) ID**, and the **VPN name of a bare metal instance**, select a state, and then click **Search** to view the bare metal instance VPNs assigned to all the HSWs. Valid values of the **Status** parameter are **Succeeded** and **Creating**.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/c46114abc042d351a48a682c6f951dd6.webp)

   **View BD usage**

   You can view BD usage to learn about the BD configuration distribution in a timely manner.

   <ol type="i">

   <li>

   Select **View BD Usage** from the drop-down list in the upper-left corner of the tab.

   </li>

   <li>

   View the BD usage in the list. By default, all data in the **Succeeded** state is displayed.

   </li>

   </ol>

   Specify a **computing access gateway name**, a **BD ID**, and a **vSwitch ID**, select a state, and then click **Search** to view BD usage. Valid values of the **Status** parameter are **Succeeded**, **Creating**, and **Deleting**.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/585f0b248b766d88691cd2385f145072.webp)

   **Check initialization configurations**

   In O&M emergency scenarios, you can use this feature to check whether the initialization configurations of the HSW are successful.

   > **Note**
   >
   > This feature only checks the initialization status of vSwitches for computing access gateways and whether the initialization configurations are successful. No operation is performed on the bare metal instance.

   <ol type="i">

   <li>

   Select **Check the Initialization Configuration** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/1d5918078152514ffa9c43dfe7ba88b7.webp)

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   | Parameter | Description |
   | --- | --- |
   | Region ID | The name of the region in which the current environment resides. |
   | HSW Name | The name of the vSwitch to be checked in instance management. |

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

   <ol type="i" start="3">

   <li>

   Click **Check** to check the initial configuration of the vSwitch.

   </li>

   </ol>

   **Check route configurations**

   In O&M emergency scenarios, you can use this feature to locate abnormal operations and check whether the route configurations of a bare metal instance are valid.

   > **Note**
   >
   > - You can use this operation to locate the exception and scan the HSW after a bare metal instance fails to be added.
   >
   > - This feature checks only whether the route configurations of a bare metal instance are valid. No operation is performed on the bare metal instance.

   <ol type="i">

   <li>

   Select **Check the Route Configuration** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/3e1b5a7f2f7fd2eae9c8e1a2a140aa06.webp)

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The name of the region in which the current environment resides.</td>
     </tr>
     <tr>
       <td>Bare Metal Name</td>
       <td>The name of the bare metal instance that was applied for or released in a VPC. It uniquely identifies the bare metal instance within a region.</td>
     </tr>
     <tr>
       <td>AccessKey ID</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs. For more information, see <strong>Manage the AccessKey pairs of</strong> <strong>an organization</strong> in <strong>Apsara Uni-manager Management Console</strong> <strong>User Guide</strong>.</td>
     </tr>
     <tr>
       <td>AccessKey Secret</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

   <ol type="i" start="3">

   <li>

   Click **Check** to check the route configurations.

   </li>

   </ol>

   **Display the information about a bare metal network gateway**

   In O&M emergency scenarios, you can use this feature to check the gateway of a vSwitch.

   > **Note**
   >
   > - This operation is only for emergency scenarios in which bare metal networks are unavailable.
   >
   > - The feature only checks the gateway information of vSwitches. It does not perform operations on bare metal instances.

   <ol type="i">

   <li>

   Select **Display the Information of Bare Metal Network Gateways** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/a80ae19c550d714e67f06a141da6056d.webp)

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The name of the region in which the current environment resides.</td>
     </tr>
     <tr>
       <td>vSwitch ID</td>
       <td>The ID of the vSwitch. You can obtain the vSwitch ID from the VPC console.</td>
     </tr>
     <tr>
       <td>AccessKey ID</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs. For more information, see <strong>Manage the AccessKey pairs of</strong> <strong>an organization</strong> in <strong>Apsara Uni-manager Management Console</strong> <strong>User Guide</strong>.</td>
     </tr>
     <tr>
       <td>AccessKey Secret</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

   <ol type="i" start="3">

   <li>

   Click **Check** to check the information about the bare metal network gateway.

   </li>

   </ol>

   **Upgrade single-RR deployment to double-RR deployment**

   In O&M emergency scenarios, you can use this feature to upgrade single-RR deployment to double-RR deployment.

   > **Warning**
   >
   > This operation may affect your business. Unauthorized operations are prohibited. Configuration changes must be performed under the guidance of technical support.

   <ol type="i">

   <li>

   Select **Change Single-RR Deployment to Double-RR Deployment** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/613956338f65f4687879314a055b918a.webp)

   </li>

   <li>

   Configure the following parameters and click **Submit**.

   </li>

   </ol>

   | Parameter | Description |
   | --- | --- |
   | Region ID | The name of the region in which the current environment resides. |
   | Existing RR Device Name | The name of RR device that you want to upgrade. |
   | New RR Device Name | The name of the new RR device that you want to use. |

   **History of changing single-RR deployment to double-RR deployment**

   You can view the history of changing single-RR deployment to double-RR deployment to obtain the up-to-date status of your RR device.

   <ol type="i">

   <li>

   Select **History of Changing Single-RR Deployment to Double-RR Deployment** from the drop-down list in the upper-left corner of the tab.

   </li>

   <li>

   You can view the history of changing single-RR deployment to double-RR deployment.

   </li>

   </ol>

   Specify **Existing RR Device Name**, **New RR Device Name**, and **Request ID** to view the records of RR device upgrades that meet the filter conditions.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/a9c4b4fc77acc07d891472ef958d7d67.webp)

   <ol type="i" start="3">

   <li>

   Find the record that you want to view and click **Details** in the **Actions** column to view

   </li>

   </ol>

   the details of the record, such as the additional information and HTTP status code.

   **Associate a vSwitch with an ECR**

   > **Warning**
   >
   > This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.

   <ol type="i">

   <li>

   Select **vSwitch Bound to Private Line Gateway** from the drop-down list in the upper-left corner of the tab.

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The name of the region in which the current environment resides.</td>
     </tr>
     <tr>
       <td>vSwitch ID</td>
       <td>The ID of the vSwitch. You can obtain the vSwitch ID from the VPC console.</td>
     </tr>
     <tr>
       <td>AccessKey ID</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs. For more information, see <strong>Manage the AccessKey</strong> <strong>pairs of an organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>AccessKey Secret</td>
     </tr>
     <tr>
       <td>Name of Border Gateway 1</td>
       <td>The name of ECR 1 to which the bare metal instance is connected.<br>On the <strong>Private Line Management</strong> tab, specify a VPC ID and computing access gateway name and click Search. Then, view the value in the <strong>Name of Private Line Gateway 1</strong> column.</td>
     </tr>
     <tr>
       <td>Source IP Address that Probes Gateway 1</td>
       <td>The source IP address of ECR 1.<br>On the <strong>Private Line Management</strong> tab, specify a VPC ID and computing access gateway name and click Search. Then, view the value in the <strong>Source IP Address that Probes Gateway 1</strong> column.</td>
     </tr>
     <tr>
       <td>Name of Border Gateway 2</td>
       <td>The name of ECR 2 to which the bare metal instance is connected.<br>On the <strong>Private Line Management</strong> tab, specify a VPC ID and computing access gateway name and click Search. Then, view the value in the <strong>Source IP Address that Probes Gateway 2</strong> column.</td>
     </tr>
     <tr>
       <td>Source IP Address that Probes Gateway 2</td>
       <td>The source IP address of ECR 2.<br>On the <strong>Private Line Management</strong> tab, specify a VPC ID and computing access gateway name and click Search. Then, view the value in the <strong>Source IP Address that Probes Gateway 2</strong> column.</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

   <ol type="i" start="3">

   <li>

   Check whether the parameter configurations are valid.

   </li>

   </ol>

   - If yes, click **Confirm**. The system starts to apply the configurations.

     After the configurations are applied, the **Result: Successful** message appears.

   - If not, click **Back to Modify** to configure the parameters again.

   **Disassociate a vSwitch from an ECR**

   > **Warning**
   >
   > This operation is only for emergency scenarios and must be performed under the guidance of R&D engineers. Otherwise, normal business operations may be affected.

   <ol type="i">

   <li>

   Select **vSwitch Unbound from Private Line Gateway** from the drop-down list in the upper-left corner of the tab.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/49f6788b3d27959cb50b0722c5734eba.webp)

   </li>

   <li>

   Configure the following parameters and click **Next**.

   </li>

   </ol>

   <table>
     <tr>
       <th>Parameter</th>
       <th>Description</th>
     </tr>
     <tr>
       <td>Region ID</td>
       <td>The name of the region in which the current environment resides.</td>
     </tr>
     <tr>
       <td>vSwitch ID</td>
       <td>The ID of the vSwitch. You can obtain the vSwitch ID from the VPC console.</td>
     </tr>
     <tr>
       <td>AccessKey ID</td>
       <td rowspan="2">The AccessKey ID and AccessKey secret of the organization, which can be obtained from the <strong>Organizations</strong> page of the Apsara Uni-manager Management Console based on the organization to which the VPC belongs. For more information, see <strong>Manage the AccessKey</strong> <strong>pairs of an organization</strong> in Apsara Uni-manager Management Console User Guide.</td>
     </tr>
     <tr>
       <td>AccessKey Secret</td>
     </tr>
   </table>

   > **Note**
   >
   > If the specified values are invalid, click **Re-enter** in the lower part of the tab and configure the parameters again.

   <ol type="i" start="3">

   <li>

   Check whether the parameter configurations are valid.

   </li>

   </ol>

   - If yes, click **Confirm**. The system starts to apply the configurations.

     After the configurations are applied, the **Result: Successful** message appears.

   - If not, click **Back to Modify** to configure the parameters again.

<a id="section-3"></a>

# 3.Networking products

<a id="section-3-1"></a>

## 3.1. CGW O&M

> **Note**
>
> By default, the **CGW O&M** module is hidden in the navigation pane. If you need to perform O&M operations on CGW clusters, you can modify the corresponding menu settings by referring to **User permissions** > **Menu Management** in Apsara Uni-manager Operations Console User Guide.

<a id="section-3-1-1"></a>

### 3.1.1. CGW cluster management

**Procedure**

1. Log on to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Network Services** > **CGW O&M** > **CGW Cluster Management**.

4. On the CGW Cluster Management page, select a region from the **Region** drop-down list. The zones and cluster topology in the selected region are displayed in the **Zone List** and **Cluster Topology** sections.

   > **Note**
   >
   > Only x86-based physical machines can be managed.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/0e59cbefc0dc3fe1f93375f86924829c.webp)

5. Find the zone that you want to manage and click **Set Secondary Zone** in the **Actions** column.

   > **Note**
   >
   > You can perform this operation on zones for which the secondary zone is not configured.

6. In the Set Secondary Zone dialog box, select a secondary zone from the **Secondary Zone** drop-down list and click **OK**.

   > **Note**
   >
   > - The cluster that you select as the secondary zone must have the same architecture and reside in the same region as the current cluster.
   >
   > - The secondary zone that you select cannot be the secondary zone of another zone.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/7e23507452ab999dd3ad1ae9b77e8eef.webp)

**What to do next**

**Remove a secondary zone**

> **Note**
>
> You can perform this operation on zones for which the secondary zone is configured.

1. Find the zone that you want to manage and click **Remove Secondary Zone** in the **Actions** column.

2. In the message that appears, click **OK**.

**View the change history of a zone**

1. Find the zone that you want to manage and click **View Change History** in the **Actions** column.

2. In the View Change History dialog box, view the change history of the zone.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/a9bead704aea369117e3770a3250b3d7.webp)

3. Find the change record that you want to manage and click **View details** in the **Operation** column. On the **Execution Details** page, view detailed information. For more information, see Execution history.

<a id="section-3-1-2"></a>

### 3.1.2. CGW management

<a id="section-4"></a>

# 4.Traffic visualization

The Traffic Visualization module can monitor physical and virtual networks in the cloud platform, and analyze real-time and historical traffic in the networks. This module also analyzes traffic by virtual network, public network, and border physical network and generates visualized charts. You can also troubleshoot issues based on the traffic data or monitored traffic metrics.

> **Note**
>
> By default, the Traffic Visualization module is not displayed. To use this module, perform the following operations: Log on to the Apsara Uni-manager Operations Console. In the top navigation bar, choose More > **User Authorities**. In the left-side navigation pane, click **Menu Management**. On the Menu management page, modify the menu settings to display the Traffic Visualization module.

<a id="section-4-1"></a>

## 4.1. Visual settings

Before you use traffic visualization, you must configure items such as analyzers, collection rules, and scenarios to collect, process, and analyze traffic based on your business requirements.

**Workflow**

The following flowchart shows how to initialize traffic visualization.

1. Create an analyzer and an analysis port. For more information, see Manage analysis devices.

2. Create a collection rule. For more information, see Manage collection rules.

3. Create an analysis scenario. For more information, see Manage scenarios.

**Manage analysis devices**

Analysis devices include analyzers and analysis ports. The collection and analysis of traffic depend on the analysis devices. Before you collect and analyze traffic, you must create the required analysis devices.

**Usage notes**

- An **analyzer**, also known as a network performance monitor (NPM), refers to a device that performs traffic analysis. The following types of analyzers are supported: NPM physical machines and NPM central control machines.

- An **analysis port** refers to the traffic collection port of an NPM device. Traffic is received on the port for collection and analysis.

**Procedure**

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Traffic Visualization** > **Visual Settings**.

4. On the **System Management** page, click the **Analyze Device Management** tab. On this tab, you can perform operations that are described in the following table.

   | Section | Operation | Description |
   | --- | --- | --- |
   |  | Create an analyzer | i. In the <strong>Analyzer management</strong> section, click <strong>Add analyzer</strong> above the analyzer list. |

   <ol type="i" start="2">

   <li>

   In the **Add analyzer** panel, configure the parameters and click

   </li>

   </ol>

   **OK**.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/1839873af70352ed18e873ad1fed1d0d.webp)

   Analyzer management

   - **Zone**: the zone in which you want to create an analyzer.

   - **Analyzer name**: the name of the analyzer.

     The name can be up to 32 characters in length and can contain letters, digits, and underscores. It cannot start with a digit.

   - **Analyzer role**: the role that the NPM device plays. Valid values:

     - **NPM physical machine**: collects and processes traffic.

     - **NPM central control machine**: displays traffic analysis results.

     - **Galaxy Security Gateway**: preferentially forwards traffic to the **traffic gateway** when you configure virtual private cloud (VPC) traffic mirroring rules.

   - **Manage IP addresses:** the IP address of the NPM device<strong>.</strong>

   - **Username**: the username that is used to log in to the NPM device.

   - **Password**: the password that is used to log in to the NPM device.

   - **Serial Number**: the serial number of the NPM device.

   - **Portal**: the web page URL of the NPM central control machine, which is used for daily O&M and management of the NPM device. After an analyzer is created, a portal for the analyzer is automatically generated by the system and can be viewed in the analyzer list.

   - **Analyzer description**: the description of the analyzer.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/567da393ca11bdd58e7784005f78f31f.webp)

   <ol type="i">

   <li>

   In the analyzer list of the **Analyzer management** section, you can view information about an analyzer, including **Device ID**,

   </li>

   </ol>

   View an

   **Analyzer name**, **Zone**, **Manage IP addresses**,

   analyzer

   **Authorization Status**, **Running status**, **Role**, **Description**, **Serial Number**, **Portal**, **Creation date**, and **Modified At**.

   <ol type="i" start="2">

   <li>

   Find the analyzer that you want to view and click **Details** in the

   </li>

   </ol>

   **Actions** column. In the **Details** panel, view the details of the analyzer.

   <ol type="i">

   <li>

   In the analyzer list of the **Analyzer management** section, find the analyzer that you want to modify and click **Edit** in the **Actions** column.

   </li>

   <li>

   In the **Edit analyzer** panel, modify the parameters and click

   </li>

   </ol>

   **OK**.

   Modify an

   For more information about the parameters, see Create an

   analyzer

   analyzer.

   > **Note**
   >
   > The **Analyzer role** parameter cannot be modified.

   > **Important**
   >
   > - If an analyzer is associated with an analysis port, you cannot delete the analyzer.
   >
   > - If an analyzer is associated with a collection rule, you cannot delete the analyzer.

   Delete an analyzer

   <ol type="i">

   <li>

   In the analyzer list of the **Analyzer management** section, find the analyzer that you want to delete and click **Delete** in the **Actions** column.

   </li>

   <li>

   In the message that appears, click **OK**.

   </li>

   </ol>

   > **Note**
   >
   > Before you create an analysis port, make sure that an analyzer is created.

   <ol type="i">

   <li>

   In the **Analysis Port Management** section, click **Add an analysis Port** above the analysis port list.

   </li>

   </ol>

   <table>
     <tr>
       <td>Analysis Port Management</td>
       <td>Create an analysis port</td>
       <td>ii. In the <strong>Add an analysis Port</strong> panel, configure the parameters and click <strong>OK</strong>.<br><img src="en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/5278ccefb919e676dff1f14b10a17f15.webp" alt=""><br>• <strong>Analysis port name:</strong> the name of the analysis port.<br>The name can be up to 32 characters in length and can contain letters, digits, and underscores. It cannot start with a digit.<br>• <strong>Analyzer name:</strong> the name of the analyzer that you want to use.<br>• <strong>Analyzer physical interface name:</strong> the physical interface of the analyzer.<br>• <strong>Analysis Port Type</strong>: the type of the analysis port. Valid values:<br>• VPC<br>• Physical<br>• ACK<br>• ALL<br>• <strong>Analysis port IP</strong>: the IP address of the analysis port.Standard IPv4 address is supported.<br>• <strong>Description</strong>: the description of the analysis port.</td>
     </tr>
   </table>

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/a935179940234ec0787003c1412e0d44.webp)

   <ol type="i">

   <li>

   In the analysis port list of the **Analysis Port Management** section, you can view information about an analysis port,

   </li>

   </ol>

   View an

   including **No.**, **Analysis port name**, **Analyzer name**,

   analysis port

   **Analyzer physical network port name**, **Analysis Port Type**, **Analysis port IP**, **Description**, and **Creation date**.

   <ol type="i" start="2">

   <li>

   Find the analysis port that you want to view and click **Details** in

   </li>

   </ol>

   the **Actions** column. In the **Details** panel, view the details of the analysis port.

   <ol type="i">

   <li>

   In the analysis port list of the **Analysis Port Management** section, find the analysis port that you want to modify and click **Edit** in the **Actions** column.

   </li>

   <li>

   In the **Edit analysis Port** panel, modify the parameters and

   </li>

   </ol>

   click **OK**.

   For more information about the parameters, see Create an analysis port.

   > **Note**

   Modify an

   > The **Analyzer name** and **Analyzer physical interface**

   analysis port

   > **name** parameters cannot be modified.

   > **Important**
   >
   > If an analysis port is associated with a collection rule, you cannot delete the analysis port.

   Delete an analysis port

   <ol type="i">

   <li>

   In the analysis port list of the **Analysis Port Management** section, find the analysis port that you want to delete and click **Delete** in the **Actions** column.

   </li>

   <li>

   In the message that appears, click **OK**.

   </li>

   </ol>

**Manage collection rules**

A collection rule defines the data source and analysis mode of traffic. The analysis devices specified in a collection rule collect and analyze traffic based on the collection rule.

**Prerequisites**

Before you create a collection rule, make sure that an analyzer and an analysis port are created. For more information, see Manage analysis devices.

**Procedure**

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Traffic Visualization** > **Visual Settings**.

4. On the **System Management** page, click the **Collection Rule Management** tab. On this tab, you can perform operations that are described in the following table.

   | Operation | Description |
   | --- | --- |
   | Create a collection rule | i. Click <strong>Add collection rules</strong> above the collection rule list.ii. In the <strong>Add collection rules</strong> panel, configure the parameters and click <strong>OK</strong>.<br>For more information about the parameters, see Collection rule parameters. |
   | View a collection rule | In the collection rule list, you can view information about a collection rule, including <strong>Rule ID</strong>, <strong>Collection rule name</strong>, <strong>Zone</strong>, <strong>Data source type</strong>, <strong>Data</strong> <strong>source host device</strong>, <strong>Data source port</strong>, <strong>VPC ID</strong>, <strong>Data Source Port ID</strong>, <strong>SLB</strong> <strong>ID</strong>, <strong>ACK Cluster ID</strong>, <strong>Flow direction</strong>, <strong>Traffic analysis mode</strong>, <strong>Analyzer name</strong>, <strong>Analysis port name</strong>, <strong>Analysis Port VLAN ID</strong>, <strong>Status</strong>, <strong>Description</strong>, <strong>Creation</strong> <strong>date</strong>, and <strong>Modified At</strong>. |

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/a1bc776ff2c11577ba90e6c4c3acac3c.webp)

   <table>
     <tr>
       <td>Retry a collection rule</td>
       <td>Note<br>If the <strong>Status</strong> of a collection rule is other than Failed, you can retry the collection rule.<br>i. In the collection rule list, find the collection rule that you want to retry and click <strong>Retry</strong> in the <strong>Actions</strong> column.<br>ii. In the panel that appears, configure the parameters and click <strong>OK</strong>.</td>
     </tr>
     <tr>
       <td>Modify a collection rule</td>
       <td>Note<br>If the <strong>Status</strong> of a collection rule is <strong>Effective</strong>, or if the <strong>Status</strong> is <strong>Failed</strong> and the failure is caused by insufficient resources, you can edit the collection rule.<br>i. In the collection rule list, find the collection rule that you want to modify and click <strong>Edit</strong> in the <strong>Actions</strong> column.<br>ii. In the <strong>Edit collection rules</strong> panel, modify the parameters and click <strong>OK</strong>.<br>For more information about the parameters, see Collection rule parameters.<br>Note<br>• If the <strong>Data source type</strong> parameter is set to <strong>Elastic network</strong> <strong>card</strong>, you can modify the <strong>Zone</strong>, <strong>Rule name</strong>, <strong>Display VPC Image</strong> <strong>Filtering Rules</strong>, <strong>SLB Instance</strong>, and <strong>Description</strong> parameters.<br>• If the <strong>Data source type</strong> parameter is set to <strong>Physical switch</strong>, you can modify the <strong>Zone</strong>, <strong>Rule name</strong>, and <strong>Description</strong> parameters.<br>• If the <strong>Data source type</strong> parameter is set to <strong>ACK container</strong>, you can modify the <strong>Rule name</strong> and <strong>ACK Cluster ID</strong> parameters.</td>
     </tr>
     <tr>
       <td>Delete a collection rule</td>
       <td>Important<br>If a collection rule is associated with an analysis scenario, you cannot delete the collection rule.<br>i. In the collection rule list, find the collection rule that you want to delete and click <strong>Delete</strong> in the <strong>Actions</strong> column.<br>ii. In the message that appears, click <strong>OK</strong>.</td>
     </tr>
   </table>

**Collection rule parameters**

| Parameter | Description |
| --- | --- |
| Zone | Select a zone for the collection rule. |
| Rule name | Enter a name for the collection rule. |
| Data source type | Select the type of the data source. By default, <strong>Physical switch</strong> is selected.Valid values:<br>• <strong>Elastic network card</strong>: collects traffic from elastic network interfaces (ENIs).<br>• <strong>Physical switch</strong>: collects traffic from physical switches.<br>• <strong>ACK container</strong>: collects traffic from Container Service for Kubernetes (ACK) containers. |
| Traffic analysis mode | Select a mode for traffic analysis. Only Traffic Image is supported.<br><strong>Traffic Image</strong>: specifies that all traffic is copied to the analysis port.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> or <strong>Physical switch</strong>. |
| Create Resource Type | Select the type of the resource to be created. Only <strong>SLB Instance</strong> is supported.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>ACK container</strong>. |
| <strong>SLB Type</strong> (ACK container selected) | Select the purpose of the SLB instance to be created. Valid values:<br>• <strong>Data Channel</strong>: creates an SLB instance to connect the ACK cluster to the ACK traffic analysis port of the NPM device. This serves as a data channel to carry the ACK traffic.<br>• <strong>Signaling Channel</strong>: creates an SLB instance to connect the ACK cluster to the management port of the NPM device. This serves as a signal channel.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>ACK container</strong>. |

<table>
  <tr>
    <td><strong>AliUid</strong>/<strong>Level-1</strong> Organization AliUid</td>
    <td>Enter the Alibaba Cloud account ID of the level-1 organization for Cloud Gateway (CGW) for authorization. You can obtain the ID in the Apsara Uni-manager Operations Console.<br>Note<br>• This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> or <strong>ACK container</strong>.<br>• After authorization is complete, the system creates a VPC image, creates a Server Load Balancer (SLB) instance, and then attaches an NPM server or traffic gateway to the backend servers of the SLB instance for tenants in the level-1 organization.</td>
  </tr>
  <tr>
    <td>ACK Cluster ID</td>
    <td>Enter the ID of an ACK cluster.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>ACK container</strong>.</td>
  </tr>
  <tr>
    <td>Select VPC</td>
    <td>Select the VPC to which your ENI or ACK cluster belongs.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> or <strong>ACK container</strong>.</td>
  </tr>
  <tr>
    <td>Select a VSwitch</td>
    <td>Select the vSwitch to which the ACK cluster belongs.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>ACK container</strong>.</td>
  </tr>
  <tr>
    <td>Select ENI</td>
    <td>Select the ENI that you want to use.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong>.</td>
  </tr>
</table>

| Display VPC Image Filtering Rules | Select <strong>Show</strong> or <strong>Hide</strong>.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong>. |
| --- | --- |
| Collection Policy for Inbound Rules | Select the collection action of the inbound rule. Valid values:<br>• Collect Network Traffic<br>• Network Traffic Is Not Collected<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>Display VPC Image Filtering</strong> <strong>Rules</strong> parameter to <strong>Show</strong>. |
| Source CIDR Block of Inbound Traffic | Specify the source CIDR block of inbound traffic. You must enter a valid CIDR block.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>Display VPC Image Filtering</strong> <strong>Rules</strong> parameter to <strong>Show</strong>. |
| Source Port Range of Inbound Traffic | Enter the source port range of inbound traffic.<br>Note<br>• This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>Display VPC</strong> <strong>Image Filtering Rules</strong> parameter to <strong>Show</strong>.<br>• Valid values: 1 to 65535. Separate the first port and the last port with a forward slash (/). Examples: 1/200 and 80/80. If you set the protocol type to <strong>ALL</strong> or <strong>ICMP</strong>, all ports are available. In this case, you do not need to configure this parameter. |
| Protocol Type Used by Inbound Traffic to Be Mirrored | Select the protocol type that is used by inbound traffic to be mirrored.Valid values: <strong>ALL</strong>, <strong>ICMP</strong>, <strong>TCP</strong>, and <strong>UDP</strong>.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>Display VPC Image Filtering</strong> <strong>Rules</strong> parameter to <strong>Show</strong>. |
| Destination CIDR Block of Inbound Traffic | Specify the destination CIDR block of inbound traffic. You must enter a valid CIDR block.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>Display VPC Image Filtering</strong> <strong>Rules</strong> parameter to <strong>Show</strong>. |
| Destination Port Range of Inbound Traffic | Enter the destination port range of inbound traffic.<br>Note<br>• This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>Display VPC</strong> <strong>Image Filtering Rules</strong> parameter to <strong>Show</strong>.<br>• Valid values: 1 to 65535. Separate the first port and the last port with a forward slash (/). Examples: 1/200 and 80/80. If you set the protocol type to <strong>ALL</strong> or <strong>ICMP</strong>, all ports are available. In this case, you do not need to configure this parameter. |
| Collection Policy for Outbound Rules | Select the collection action of the outbound rule. Valid values:<br>• Collect Network Traffic<br>• Network Traffic Is Not Collected<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>Display VPC Image Filtering</strong> <strong>Rules</strong> parameter to <strong>Show</strong>. |
| Source CIDR Block of Outbound Traffic | Specify the source CIDR block of outbound traffic. You must enter a valid CIDR block.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>Display VPC Image Filtering</strong> <strong>Rules</strong> parameter to <strong>Show</strong>. |
| Source Port Range of Outbound Traffic | Enter the source port range of outbound traffic.<br>Note<br>• This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>Display VPC</strong> <strong>Image Filtering Rules</strong> parameter to <strong>Show</strong>.<br>• Valid values: 1 to 65535. Separate the first port and the last port with a forward slash (/). Examples: 1/200 and 80/80. If you set the protocol type to <strong>ALL</strong> or <strong>ICMP</strong>, all ports are available. In this case, you do not need to configure this parameter. |
| Protocol Type Used by Outbound Traffic to Be Mirrored | Select the protocol type that is used by outbound traffic to be mirrored.Valid values: <strong>ALL</strong>, <strong>ICMP</strong>, <strong>TCP</strong>, and <strong>UDP</strong>.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>Display VPC Image Filtering</strong> <strong>Rules</strong> parameter to <strong>Show</strong>. |
| Destination CIDR Block of Outbound Traffic | Specify the destination CIDR block of outbound traffic. You must enter a valid CIDR block.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>Display VPC Image Filtering</strong> <strong>Rules</strong> parameter to <strong>Show</strong>. |
| Destination Port Range of Outbound Traffic | Enter the destination port range of outbound traffic.<br>Note<br>• This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>Display VPC</strong> <strong>Image Filtering Rules</strong> parameter to <strong>Show</strong>.<br>• Valid values: 1 to 65535. Separate the first port and the last port with a forward slash (/). Examples: 1/200 and 80/80. If you set the protocol type to <strong>ALL</strong> or <strong>ICMP</strong>, all ports are available. In this case, you do not need to configure this parameter. |
| <strong>SLB Type</strong> (Elastic network card selected) | You can select <strong>Use Existing SLB Instance</strong> or <strong>Create SLB Instance</strong> for this parameter.<br>Note<br>• This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong>.<br>• If you select <strong>Create SLB Instance</strong>, the system automatically creates an SLB instance. |
| SLB Instance | Select an existing SLB instance.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>SLB Type</strong> parameter to <strong>Use</strong> <strong>Existing SLB Instance</strong>. |
| SLB Backend Device Name | Specify an analyzer for SLB backend collection. This parameter is available only if you set the Data source type parameter to <strong>Elastic network card</strong> or <strong>ACK container</strong>.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>SLB Type</strong> parameter to <strong>Create</strong> <strong>SLB Instance</strong>, or if you set the <strong>Data source type</strong> parameter to <strong>ACK</strong> <strong>container</strong>. |
| Analysis Port Name of SLB Backend Device | Specify an analysis port for SLB backend collection.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> and the <strong>SLB Type</strong> parameter to <strong>Create</strong> <strong>SLB Instance</strong>, or if you set the <strong>Data source type</strong> parameter to <strong>ACK</strong> <strong>container</strong>. |
| Data source host device | Select the host device of the physical switch.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Physical switch</strong>. |
| Port name of the data source host device | Select a port for the physical switch host device based on the data source host device that you select.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Physical switch</strong>. |
| Data Source Port ID | The value is automatically matched and displayed based on the data source host device and the port name of the data source host device that you select.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Physical switch</strong>. |
| Analyzer Name | Select the analyzer that you want to use to collect traffic.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Physical switch</strong>. |
| Analysis Port Name | Select the analysis port that you want to use to collect traffic.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Physical switch</strong>. |
| Analysis Port VLAN ID | Enter the VLAN ID of the analysis port.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Physical switch</strong>. |
| Description | Enter a description for the collection rule.<br>Note<br>This parameter is required if you set the <strong>Data source type</strong> parameter to <strong>Elastic network card</strong> or <strong>Physical switch</strong>. |

**Manage scenarios**

You can associate different collection rules with different analysis scenarios based on your business requirements.

**Prerequisites**

Before you create an analysis scenario, make sure that collection rules are created. For more information, see Manage collection rules.

**Procedure**

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Traffic Visualization** > **Visual Settings**.

4. On the **System Management** page, click the **Scenario Management** tab. On this tab, you can perform operations that are described in the following table.

   | Operation | Description |
   | --- | --- |
   | Create an analysis scenario | i. Click <strong>Create an analysis scenario</strong> above the analysis scenario list.<br>ii. In the <strong>Add scenario</strong> panel, configure the parameters and click <strong>OK</strong>.<br>![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/508cc2546a75f82c5f9c07142c1645e9.webp)<br>• <strong>Zone</strong>: the zone in which you want to create an analysis scenario.<br>• <strong>Scene name</strong>: the name of the analysis scenario.<br>The name can be up to 32 characters in length and can contain letters and digits.<br>• <strong>Network Type</strong>: the network type of the analysis scenario. Valid values:<br>• <strong>VPC</strong>: the virtual network.<br>• <strong>BORDER</strong>: the border physical network.<br>• <strong>Collection rules</strong>: the one or more collection rules that you want to associate with the analysis scenario. You can select multiple collection rules.<br>• <strong>Description</strong>: the description of the analysis scenario. |
   |  |  |
   | View an analysis scenario | i. In the analysis scenario list, you can view information about an analysis scenario.<br>ii. Find the analysis scenario that you want to view and click <strong>Details</strong> in the <strong>Actions</strong> column. In the <strong>Details</strong> panel, view the details of the analysis scenario. |
   | Modify an analysis scenario | i. In the analysis scenario list, find the analysis scenario that you want to modify and click <strong>Edit</strong> in the <strong>Actions</strong> column.<br>ii. In the panel that appears, modify the analysis scenario parameters and click <strong>OK</strong>.<br>For more information about the parameters, see Create an analysis scenario.<br>Note<br>The <strong>Network Type</strong> parameter cannot be modified. |
   | Delete an analysis scenario | i. In the analysis scenario list, find the analysis scenario that you want to delete and click <strong>Delete</strong> in the <strong>Actions</strong> column.<br>ii. In the message that appears, click <strong>OK</strong>. |

**Network Resource List**

You can view all the SLB instances that are created in the traffic visualization module.

**Procedure**

1. Log in to the Apsara Uni-manager Operations Console.

2. In the top navigation bar, choose **Product Operation** > **Networking** > **Network Operations Console**.

3. In the left-side navigation pane, choose **Traffic Visualization** > **Visual Settings**.

4. On the **System Management** page, click the **Network Resource List** tab. On this tab, view the network resource information in the following columns: **Zone**, **Resource ID**, **Resource Value**, **Resource Type**, **VpcId**, **Resource Usage**, **Resource Owner**, and **Created At**.

   ![](en-cloud-gateway-operations-guide-v3.18.6-20260310.assets/485e761b2802e13f36cb759d419fd229.webp)
