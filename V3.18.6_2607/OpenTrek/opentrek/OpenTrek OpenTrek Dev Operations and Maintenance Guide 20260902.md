Alibaba Cloud  
Apsara Stack  
OpenTrek  
OpenTrek Dev Operations and  
Maintenance Guide  
Product Version: v3.18.6-2607  
Document Version: 20260902

**Table of Contents**

- [1.O&M overview](#section-1)
- [2.View the monitoring dashboard](#section-2)
- [3.View alert notifications](#section-3)
- [4.Troubleshooting](#section-4)
    - [4.1. Agent](#section-4-1)
        - [4.1.1. Troubleshoot agent issues](#section-4-1-1)
        - [4.1.2. Agent node execution failure](#section-4-1-2)
    - [4.2. Data center](#section-4-2)
        - [4.2.1. Dataset management](#section-4-2-1)
            - [4.2.1.1. Datasets](#section-4-2-1-1)
            - [4.2.1.2. Data files](#section-4-2-1-2)
            - [4.2.1.3. Data subsets](#section-4-2-1-3)
        - [4.2.2. Data processing](#section-4-2-2)
            - [4.2.2.1. Create a knowledge base parsing service](#section-4-2-2-1)
                - [4.2.2.1.1. Upload a custom image](#section-4-2-2-1-1)
                - [4.2.2.1.2. Create an AI gateway](#section-4-2-2-1-2)
                - [4.2.2.1.3. Create a Kafka instance and a topic](#section-4-2-2-1-3)
                - [4.2.2.1.4. Create a VLM inference service](#section-4-2-2-1-4)
            - [4.2.2.2. Troubleshoot knowledge base document parsing issues](#section-4-2-2-2)
            - [4.2.2.3. Perform a hot upgrade on the image of a knowledge base parsing service](#section-4-2-2-3)
            - [4.2.2.4. Troubleshooting processing tasks](#section-4-2-2-4)
            - [4.2.2.5. Perform a hot update on a control application](#section-4-2-2-5)
            - [4.2.2.6. Perform a hot update on an offline image](#section-4-2-2-6)
            - [4.2.2.7. Video data processing FAQ](#section-4-2-2-7)
    - [4.3. Model integration](#section-4-3)

<a id="section-1"></a>

# 1.O&M overview

Alibaba Cloud OpenTrek Agent Dev is built on cloud-native and Artificial Intelligence Generated Content (AIGC) technologies, and runs on Kubernetes. If you have basic Linux and Kubernetes O&M experience, you can quickly get started with basic O&M for the Agility Edition. This document describes the O&M objectives, requirements, precautions, and support channels for OpenTrek Agent Dev.

<a id="section-2"></a>

# 2.View the monitoring dashboard

**Apsara Uni-Manager**

Log on to ASO > Cloud Platform Monitoring Dashboard > OpenTrek Agent Dev Monitoring Dashboard.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/1b4aa5be72181f557ea7af9029169412.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/79cbd9a0f01d8cffaf070921b2ec38c2.webp)

**Kubernetes cluster node monitoring dashboard**

Click the cluster node monitoring dashboard to view metrics such as CPU, memory, disk, I/O, and network usage by node.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/bf27fd90ebf9f7506cd0223abd526885.webp)

**Kubernetes cluster pod monitoring dashboard**

Click the cluster pod monitoring dashboard to view metrics such as CPU, memory, and restart count by pod.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/0a1fa68cbe00608b2ef838c6e97679a5.webp)

**Java application monitoring dashboard**

Click the basic monitoring dashboard to view metrics such as HTTP, JVM, and Dubbo by application and pod.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/3357a19be80de02e9869e649bfd50c7a.webp)

**Python application monitoring dashboard**

Click the basic monitoring dashboard (Python) to view metrics such as HTTP by application and pod.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/9cc06639c23d308395699b662276fa1d.webp)

**Go application (Gin framework) monitoring dashboard**

Click the basic monitoring dashboard (Go-gin) to view metrics such as HTTP, Go heap, and Goroutine by application and pod.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/c55437fe9ad96ef4d196368d3f684ece.webp)

**Go application (Arrow framework) monitoring dashboard**

Click the basic monitoring dashboard (Go-arrow) to view metrics such as HTTP, Go heap, and Goroutine by application and pod.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/82b2bd51a428e804f4993cfefcc88f67.webp)

**Tenant**

Go to OpenTrek Agent Dev > Global Resource Management and find the ACK cluster name.

Go to Prometheus Monitoring 2.0 > Grafana Dashboard, click the sfm catalog, and find the dashboard for the target cluster.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/8d2abe664572781a319e3dcdbe288e6c.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/a67ddac23be7d220e9af4cd575a0cda8.webp)

**Kubernetes cluster node monitoring dashboard**

Click the sfm-tenant-cluster-node-dashboard dashboard to view metrics such as CPU, memory, disk, I/O, and network usage.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/79cb0c4e28c4ae9360bda9691faf34e0.webp)

**Kubernetes cluster pod monitoring dashboard**

Click the sfm-tenant-cluster-pod-dashboard dashboard to view metrics such as CPU, memory, and restart count by namespace and pod.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/79cb0c4e28c4ae9360bda9691faf34e0.webp)

**Java application monitoring dashboard**

Click the sfm-tenant-basic-java-dashboard dashboard to view metrics such as HTTP, JVM, and Dubbo by application and pod.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/a3d81db90f765e4f1603bc6e350c0baf.webp)

**Go application (Gin framework) monitoring dashboard**

Click the sfm-tenant-basic-go-gin-dashboard dashboard to view metrics such as HTTP, Go heap, and Goroutine by application and pod.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/b89b6290ffb201d09357328456071916.webp)

**Go application (Arrow framework) monitoring dashboard**

Click the sfm-tenant-basic-go-arrow-dashboard dashboard to view metrics such as HTTP, Go heap, and Goroutine by application and pod.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/8541939395f6210a5daa21273dec87d9.webp)

<a id="section-3"></a>

# 3.View alert notifications

**Apsara Uni-Manager**

**View alerts**

Log on to ASO, go to the Monitoring and Alerting > Alert List page, and select sfm from the Resource Ownership drop-down list to view the alerts of OpenTrek Agent Dev.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/0f298d0724df8965e17363916504b679.webp)

**Alert rules**

On the Monitoring and Alerting > Alert Rules page, select sfm from the Cloud Service drop-down list in the advanced filter to view the alert rule configuration.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/87a1931fedf24c8d0fc3223f5b83ee09.webp)

Click Custom Change to modify the alert configuration.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/18c63177cee5ca8d6d75db882efc92b1.webp)

**Alert notification configuration**

On the Monitoring and Alerting > Alert Settings > Policy Management page, add contacts to configure alert recipients and select sfm as the service.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/70056e4e935f7e630c4e7835fe8ca6e1.webp)

On the Monitoring and Alerting > Alert Settings > Alert Notification page, subscribe to alerts.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/6d63dc1559a56c2e16a8a29cc2e6a91f.webp)

**Tenant side**

Go to Prometheus Monitoring 2.0.

**Alert rules**

All alert rules of OpenTrek Agent Dev use the SfmAlertRule tag. You can filter alerts based on this tag.

You can filter rules that are currently triggering alerts based on the current status.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/922748ceefb8aca23ae33e0a15df68e4.webp)

**Alert notification configuration**

Filter all alert rules of OpenTrek Agent Dev based on the SfmAlertRule tag.

Set the page size to 100, select all rules, and click Configure Notification Method.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/e13547231916e527325ec447a08352ce.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/2007548541742d87754eda65e46ebec9.webp)

<a id="section-4"></a>

# 4.Troubleshooting

This chapter describes troubleshooting guidance for common runtime issues of the OpenTrek Agent Dev platform. For more information, see the troubleshooting checklists in each module center.

<a id="section-4-1"></a>

## 4.1. Agent

<a id="section-4-1-1"></a>

### 4.1.1. Troubleshoot agent issues

**Query agent progress**

**Prerequisites**

Database query: Query data in the business database ibp_system of an agent. Most projects use PolarDB databases.

Log query: Query the log of the agent application ibp-agent-platform, which is a tenant-specific application and uses the log directory /home/admin/logs/.

You can obtain the specific session ID, request ID, and request time.

In most cases, you can send a query to obtain such information, which is returned in the response body.

```sql
-- If only the session ID is returned: 
-- You can use the following statements to compare the timestamps of calls.
-- The request ID (index_name_5) and the gmt_create value (the request time that can beused in log queries) are returned.

select gmt_create,index_name_5
from ibp_task where  index_name_7 = 'Session_ID';


-- Query whether the session_code is created.
select * from ibp_agent_session where session_code like '111%'
-- Query the historical Q&A corresponding to the session_code.
select * from ibp_agent_cmd_message where session_id like '111%'
```

**Database schema SQL statements**

**Query task data**

```sql
-- Query the task execution process. 
-- index_name_1 indicates the execution result of the task. Pay attention to failed tasks.
-- index_name_2 indicates the task type, which is the node type on the left side of thecanvas.
-- index_name_2='LogTsak ' indicates the task generated in the first step.
-- index_name_2='UiTask ' indicates the task generated in the last step.
-- gmt_create indicates the estimated execution duration of each node.
-- UiTask and gmt_create of LogTsak can be used to evaluate the duration of a complete 
Q&A process. 
-- CAST(feature AS JSON)->> 'startTime' indicates the start time of the API operation.
-- CAST(feature AS JSON)->> 'endTime' indicates the end time of the API operation.
-- unique_code indicates the task ID.
select * from ibp_task where  index_name_7 = 'Session_ID' order by id desc;

-- If multiple requests are initiated from a session, add the following condition: index_name_5 = 'Request ID'.


-- index_name_2 = 'AgentInvocationTask' indicates the agent task.
-- You need to obtain the session ID of the agent task for further recursive troubleshooting.
select CAST(feature AS JSON) ->> 'CHILD_INFO'
from "ibp_task" where index_name_2 = 'AgentInvocationTask' 
and unique_code = 'Task ID from Step 1';
// If the task ID cannot be obtained in some scenarios, use keywords to query the log and find the matching task ID.
select content from "ibp_record" where title like 'Print the input parameters%'
and task_unique_code = 'Task ID from Step 1';
```

**Query execution progress data**

```sql
-- Display logs in ascending order by task and creation time.
-- You can observe the execution process and execution time difference of a task.
-- Pay attention to the content related to {"recordLoggingStatus":"error"}.
-- If multiple requests are initiated from a session, add the following condition: index_name_5 = 'Request ID'.
select * from ibp_record
where task_unique_code in 
(select unique_code as task_id 
 from ibp_task where index_name_7 ='Specific session ID')
order by task_unique_code,gmt_create asc;
```

**Log solutions**

**Analyze the duration of a request**

```bash
Replace requestId with the actual request ID.

-- Query the progress of a request in the log that is output in real time.
kubectl get pods -A -o jsonpath='{range .items[*]}
{.metadata.namespace}/{.metadata.name}{"\n"}{end}' | grep ibp-agent | while IFS=/ read 
-r ns pod; do
    echo "Processing $ns/$pod" >&2
    kubectl exec -n "$ns" "$pod" -- bash -c 'cat /home/admin/logs/ibp-agent.log 2>&1 | grep --line-buffered "Duration of the request" 2>/dev/null'
done > output1.log 2>&1

-- Query the progress of a request in historical logs.
kubectl get pods -A -o jsonpath='{range .items[*]}
{.metadata.namespace}/{.metadata.name}{"\n"}{end}' | grep ibp-agent | while IFS=/ read 
-r ns pod; do
    echo "Processing $ns/$pod" >&2
    kubectl exec -n "$ns" "$pod" -- bash -c 'zcat /home/admin/logs/ibp-agent.log.2025* 
2>&1 | grep --line-buffered "Duration of the request" 2>/dev/null'
done > output1.log 2>&1
```

**Analyze exceptions of a request**

Contact the caller to obtain the exception information carried in the response body.

```bash
Replace Exception description with the specific onsite exception information.

-- Query the progress of a request in the log that is output in real time.
kubectl get pods -A -o jsonpath='{range .items[*]}
{.metadata.namespace}/{.metadata.name}{"\n"}{end}' | grep ibp-agent | while IFS=/ read 
-r ns pod; do
    echo "Processing $ns/$pod" >&2
    kubectl exec -n "$ns" "$pod" -- bash -c 'cat /home/admin/logs/ibp-agent.log 2>&1 | grep --line-buffered -C 200 "Exception description" 2>/dev/null'
done > output1.log 2>&1

-- Query the progress of a request in historical logs.
-- You can modify the following value. The asterisk (*) indicates the specific point intime, such as ibp-agent.log.2025-05-08.*
-- /home/admin/logs/ibp-agent.log.*
kubectl get pods -A -o jsonpath='{range .items[*]}
{.metadata.namespace}/{.metadata.name}{"\n"}{end}' | grep ibp-agent | while IFS=/ read 
-r ns pod; do
    echo "Processing $ns/$pod" >&2
    kubectl exec -n "$ns" "$pod" -- bash -c 'zcat /home/admin/logs/ibp-agent.log.* 2>&1
| grep --line-buffered -C 200 "Exception description" 2>/dev/null'
done > output1.log 2>&1


llmConsumeStream, sessionId=7d84076b-42eb-47b8-abe4-89c33b2489fd,
cat agent.log | grep 'llmConsumeStream' | grep sessionId | grep node_id 
```

**Traffic metrics by agent (Scheduled collection on the on site requires a read-only database)**

-- By day.

YYYYMMDD

-- By hour.

YYYYMMDDHH24

-- By minute.

YYYYMMDDHH24MI

**Number of requests created on a session**

```sql
-- Total number of created sessions
select count(*) from ibp_agent_session;

-- Total number of active sessions (new or initiated requests) by day.
SELECT 
    TO_CHAR(gmt_modified, 'YYYYMMDD') AS days,
    COUNT(*) 
FROM 
    ibp_agent_session
WHERE 
    gmt_modified > '2025-01-15 08:00:00'
GROUP BY 
    TO_CHAR(gmt_modified, 'YYYYMMDD')
ORDER BY 
    days;
```

**Number of initiated requests**

```sql
-- The number of requests initiated by the agent. The data size of table is large.
select COUNT(*)  from "ibp_task" where index_name_2 = 'LogTask' ;

-- Statistics by day.
SELECT 
    TO_CHAR(gmt_create, 'YYYYMMDD') AS days,
    COUNT(*) 
FROM 
    ibp_task
WHERE 
    index_name_2 = 'LogTask' and gmt_create > '2025-01-15 08:00:00'
GROUP BY 
    TO_CHAR(gmt_create, 'YYYYMMDD')
ORDER BY 
    days;
```

**Traffic statistics by agent**

```text
-- Set a value range for gmt_create.
-- Configure the agent_code and agent_version fields to specify a specific agent version.

SELECT 
    TO_CHAR(gmt_create, 'YYYYMMDD') AS days,
    COUNT(*) 
FROM 
    (SELECT a.index_name_5,b."agent_code" ,b."agent_version",a.gmt_create 
     FROM "ibp_task" a LEFT JOIN "ibp_agent_session"  b on a.index_name_7 = 
b.session_code 
     where a.index_name_2 = 'LogTask' and b.agent_code = '' and b.agent_version =''
    ) m
WHERE 
    gmt_create > '' and  gmt_create < ''
GROUP BY 
    TO_CHAR(gmt_create, 'YYYYMMDD')
ORDER BY 
    days;


-- Example: Count the number of calls per agent per day after May 1, 2025.
select
  h."agent_name",
  n.*
from
  (
    SELECT
      agent_code,
      TO_CHAR(gmt_create, 'YYYYMMDD') AS days,
      COUNT(*) as number
    FROM
      (
        SELECT
          b.agent_code,
          b.agent_version,
          a.gmt_create
        FROM
          (
            select
              *
            from
              "ibp_task"
            where
              index_name_2 = 'LogTask'
              and gmt_create > '2025-05-01 00:00:00'
          ) a
          LEFT JOIN "ibp_agent_session" b on a.index_name_7 = b.session_code
      ) m
    GROUP BY
      TO_CHAR(gmt_create, 'YYYYMMDD'),
      agent_code
    ORDER BY
      days desc,
      number desc
  ) n
  LEFT JOIN "ibp_agent_ref" h on n."agent_code" = h."agent_code"
```

**Memory consumed by agent requests**

```text
-- Descriptions of returned fields: task type, session ID, request ID, and disk space occupied by task data.
-- Response condition: Task data that occupies more than 1 MB of disk space within the specified time range
SELECT 
  index_name_2,index_name_7,index_name_5,
  pg_column_size(feature) AS size_bytes,
  ROUND(pg_column_size(feature) / 1024.0 / 1024.0, 2)
FROM ibp_task
WHERE gmt_create > '2025-10-20 21:16:00' and pg_column_size(feature) > 1024 * 1024 
ORDER BY size_bytes DESC;
```

**Number of model node calls**

```sql
-- Platform wide.
SELECT 
    TO_CHAR(gmt_create, 'YYYYMMDD') AS days,
    COUNT(*) 
FROM 
    ibp_task
WHERE 
    gmt_create > '2025-01-15 08:00:00' and index_name_2 = 'LLMReasoningTask'
GROUP BY 
    TO_CHAR(gmt_create, 'YYYYMMDD')
ORDER BY 
    days;

-- Query statistics of a single agent.
SELECT 
    TO_CHAR(gmt_create, 'YYYYMMDD') AS days,
    COUNT(*) 
FROM 
    (SELECT a.index_name_5,b."agent_code" ,b."agent_version",a.gmt_create 
     FROM "ibp_task" a LEFT JOIN "ibp_agent_session"  b 
     on a.index_name_7 = b.session_code 
     and a.index_name_2 = 'LLMReasoningTask' 
     and b.agent_code = '' and b.agent_version =''
    ) m
WHERE 
    gmt_create > '' and  gmt_create < ''
GROUP BY 
    TO_CHAR(gmt_create, 'YYYYMMDD')
ORDER BY 
    days;


-- Query which models are configured.
select distinct(a.modelCode)
from (
SELECT CAST(node_config AS JSON) -> 'config' ->> 'modelCode'  as modelCode from ibp_config_node 
where  node_action = 'LLM' and node_config like '%modelCode%') a ;
    
```

**Number of calls to other external service nodes (API, RAG, or KC)**

```text
SELECT 
    TO_CHAR(gmt_create, 'YYYYMMDD') AS days,(CAST(feature AS JSON)->> 
'custom_tool_type') AS toolType,
    COUNT(*) 
FROM 
    ibp_task
WHERE 
    gmt_create > '2025-01-15 08:00:00' and index_name_2 = 'ToolInvocationTask'
GROUP BY 
    TO_CHAR(gmt_create, 'YYYYMMDD'),CAST(feature AS JSON)->> 'custom_tool_type'
ORDER BY 
    days;
```

**Java program stack**

**Virtual thread stack**

The following script dumps the virtual thread stack, merges duplicate stacks, and retains only the thread name. After the following content is copied to the environment, it runs in Python. The result is output to  `/home/admin/stack_analyzed.log`

```bash
1. Enter the Pod of the agent.
cd /home/admin
vi javastack.py

2. Run the script.
su admin
/usr/local/bin/python3  javastack.py

3. Copy the following file.
/home/admin/stack_analyzed.log
```

```python
from collections import OrderedDict
import subprocess
import os


def get_java_pid():
    # Run the 'ps -ef | grep java' command and query the result.
    try:
        result = subprocess.run(["ps", "-ef"], capture_output=True, text=True)
        processes = result.stdout.splitlines()

        # Find the first line of the Java process.
        for line in processes:
            if "java" in line and "grep" not in line:
                return line.split()[1], line.split()[7]

    except Exception as e:
        print(f"Error occurred while getting Java PID: {e}")

    return None, None


def dump_thread_stack(pid, jdk_bin, stack_file):
    try:
        command = [
            os.path.join(jdk_bin, "jcmd"),
            pid,
            "Thread.dump_to_file",
            "-format=text",
            "-overwrite",
            stack_file,
        ]

        # Run the jcmd command.
        subprocess.run(command)
        print(f"Thread stack dumped to {stack_file}")

    except Exception as e:
        print(f"Error occurred while dumping thread stack: {e}")


def main():
    stack_file = "/home/admin/stack.log"
    pid, java_exec = get_java_pid()

    if pid and java_exec:
        jdk_bin = os.path.dirname(java_exec)
        dump_thread_stack(pid, jdk_bin, stack_file)
    else:
        print("No Java process found.")
        return

    stacks = OrderedDict()
    with open(stack_file) as f:
        content = f.read()
        blocks = content.split("\n\n")
        for block in blocks:
            if not block.startswith("#"):
                continue
            split = block.split("\n", 1)
            thread = split[0]
            if len(split) <= 1:
                continue
            stack = split[1]
            if stack not in stacks:
                stacks[stack] = []
            stacks[stack].append(thread)

    stacks = OrderedDict(
        sorted(stacks.items(), key=lambda item: len(item[1]), reverse=True)
    )

    result = ""
    for stack in stacks:
        result += (
            str(len(stacks[stack])) + " in total, " + " , ".join(stacks[stack]) + "\n"
        )
        result += stack + "\n\n"
    result_file = "/home/admin/stack_analyzed.log"
    with open(result_file, "w") as f:
        f.write(result)
    print(f"Thread stack analysis completed. Please check {result_file} for details.")


if __name__ == "__main__":
    main()
```

**Thread dump by using jstack**

Obtain the process ID (PID), as shown in the following figure.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/711e4723227971a483a02d359652867b.webp)

```text
-- Replace pid with the actual PID and run the following command to download the agent.dump file.
/opt/graalvm/bin/jstack pid > agent.dump 
```

**O&M database status**

**View storage of large-sized fields**

```text
SELECT 
    id, 
    feature, index_name_2, name,
    pg_column_size(feature) AS column_size_bytes,
    (pg_column_size(feature) / 1024) AS column_size_kb
FROM 
    ibp_task
WHERE 
    gmt_create > '2025-09-08 00:00:00' and 
    pg_column_size(feature) > 500 * 1024
ORDER BY 
    column_size_kb DESC;
```

**View database connection usage**

```text
SELECT 
    datname AS database_name,         -- The database name.
    COUNT(*) AS connection_count      -- The number of connections.
FROM pg_stat_activity
GROUP BY datname
ORDER BY connection_count DESC;
```

**View the real-time status of the database**

```text
SELECT 
    datname AS database_name,         -- The database name.
    pid,                            -- The PID.
    usename AS user_name,           -- The username.
    application_name,               -- The application name.
    client_addr AS client_address,  -- The client IP address.
    state,                          -- The current status, such as active and idle.
    query                           -- The SQL statement that is being executed.
FROM pg_stat_activity WHERE state = 'active';
```

**Business data**

**View the number of tasks to be scheduled**

```sql
select count(*) from ibp_task where "index_name_11" = '0' 
and "index_name_2" in 
('CustomerSupportTask','ToolInvocationTask','AgentInvocationTask');
```

**View the execution status of a session**

```text
-- Query the task data of a session request.
-- Task type, task name, task result, task execution status, whether the task has been scheduled, (time-related parameters), and execution parameters.
select "index_name_2","name","index_name_1","index_name_9","index_name_11",
  "gmt_create" ,"gmt_modified" ,
  CAST(feature AS JSON)->> 'toolExecuteStartTime',CAST(feature AS JSON)->> 
'toolExecuteEndTime',
  CAST(feature AS JSON)->> 'startTime',CAST(feature AS JSON)->> 'endTime',
  feature
from "ibp_task" WHERE index_name_7 = 'Actual session ID' and index_name_5 = 'Actual request ID'
order by "gmt_create" desc;


select "index_name_2","name","index_name_1","index_name_9","index_name_11",
  "gmt_create" ,"gmt_modified"  
from "ibp_task" WHERE index_name_7 = 'Actual session ID' and index_name_5 = 'Actual request ID'
order by "gmt_create" desc;
-- Sort the records in descending order and compare the gmt_create values between the records, which can roughly evaluate the time consumed by the preceding node (except for streaming scenarios).
```

**Data backlog**

```sql
-- Query large-sized tables related to the agent.
select count(*) from ibp_task where gmt_create < '2025-12-16 10:33:39.559';
select count(*) from ibp_record  where gmt_create < '2025-12-16 10:33:39.559';
select count(*) from ibp_agent_cmd_message icm  where gmt_create < '2025-12-16 10:33:39.559';
select count(*) from ibp_agent_stream_thougths iast   where gmt_create < '2025-12-16 10:33:39.559';
select count(*) from ibp_agent_memory_fragment iamf    where gmt_create < '2025-12-16 10:33:39.559';


-- Query table capacity usage (in PostgreSQL database).
SELECT 
    schemaname AS table_schema,
    relname AS table_name,
    pg_total_relation_size(relid) / (1024.0 * 1024) AS total_size_mb
FROM 
    pg_stat_user_tables
WHERE 
    schemaname = 'public'
ORDER BY 
    total_size_mb DESC;


-- Query table capacity usage (in MySQL database).
SELECT 
    TABLE_NAME, 
    TABLE_SCHEMA, 
    ROUND((DATA_LENGTH + INDEX_LENGTH) / 1024 / 1024, 2) AS Total_Size_MB
FROM 
    information_schema.TABLES
WHERE 
    TABLE_SCHEMA = 'ibp_system'
ORDER BY 
    Total_Size_MB DESC;
```

**Table fields related to effect tracing**

**Q&A list**

**Table fields**

ibp_agent_cmd_message

Record the Q&A of each session

<table>
  <tr>
    <td>session_id</td>
    <td>Session ID</td>
  </tr>
  <tr>
    <td>request_id</td>
    <td>Request ID</td>
  </tr>
  <tr>
    <td>from_id</td>
    <td>The source. In agent answers, from_id is session_id.</td>
  </tr>
  <tr>
    <td>to_id</td>
    <td>The destination. In agent questions, to_id is session_id.</td>
  </tr>
  <tr>
    <td>message</td>
    <td>Content of the question or answer.</td>
  </tr>
</table>

**SQL statements**

```text
    select *
    from ibp_agent_cmd_message
    <where>
      <if test="requestId != null">
        request_id = #{requestId}
      </if>
      <if test="requestId == null">
        <if test="sessionId != null">
          session_id = #{sessionId}
        </if>
        <if test="sessionId == null">
          session_id in (
          SELECT session_code  FROM ibp_agent_session
          WHERE agent_code =  #{agentCode}
          <if test="agentVersion != null">
            and agent_version = #{agentVersion}
          </if>
          order by id desc
          limit 100
          )
        </if>
      </if>
       and (from_id != session_id or from_id is null)
       and gmt_create > #{endDate}
    </where>
    order by gmt_create desc
    limit #{pageIndex},#{pageSize}
```

**Task details**

**Table fields**

ibp_task

Record the information about tasks created on each node and the task execution and invocation information

```json
{
  "unique_code":""
 "index_name_1":"result",     // The execution result.
 "index_name_2":"taskType",   // The task type, which starts with LogTask and ends with
UiTask.
 "index_name_3":"batchNo",  
  "index_name_4":"debug",
  "index_name_5":"requestId",
 "index_name_6":"name",         
 "index_name_7":"sessionId",
  "index_name_8":"title",       // The task name.
 "index_name_9":"status",     // The task execution status.
 "index_name_10":"env",       // The environment label.
 "index_name_11":"isFire",    // Whether the task is scheduled.
 "index_name_12":"breakPoint" // The break-point label.
 "feature":"" // The extension fields, including request and response parameters.
} 
```

```text
LogTask: The logging task.
    LLMReasoningTask: The model task.
    ScriptInvocationTask: The script task.
    ToolInvocationTask: The tool task.
    AgentInvocationTask: The agent task.
    //CONSIDER_TASK("ConsiderTask","Planning task"),
    CustomerSupportTask: The general-purpose asynchronous task.
    //OBSERVATION_TASK("ObservationTask", "Result observation task"),
    // INVISIBLE_TASK("InvisibleTask", "Frontend invisible task"),
    UiTask: the result rendering task.
```

**System logs**

Table ibp_record

**Chain-of-thought**

Data ibp_agent_stream_thougths

<a id="section-4-1-2"></a>

### 4.1.2. Agent node execution failure

During the debugging phase, the execution of the agent node fails.

Example:

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/e88fdbe28e8d070f89f840f73b539e3e.webp)

Find the red dot on the canvas to locate the failed node, and obtain the specific error details in the response or error message on the right side of the page. Then, go back to the design page to fix the node.

If the operation is performed by calling the API, click Effect Tracking on the agent version page.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/8707728862cd73e7c014d829109f4814.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/1bc27b12fe49ad63c8f264b8ca6ea81c.webp)

Find the task based on the session ID and request ID, and go to the details page and system log to identify the cause of failure.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/245ae0cebd4b8a79e04b8e88cfa1d315.webp)

<a id="section-4-2"></a>

## 4.2. Data center

<a id="section-4-2-1"></a>

### 4.2.1. Dataset management

<a id="section-4-2-1-1"></a>

#### 4.2.1.1. Datasets

This topic describes the issues that may arise when you use datasets, the possible causes, and the solutions.

1. **The dataset list reports the following error message:**

**Contact the O&M administrator and go to the Resource Management> Global Service Management page to create a search and parse service and allocate namespace.**

Problem: The dataset list reports the following error message: Contact the O&M administrator and go to the Resource Management> Global Service Management page to create a search and parse service and allocate namespace.

Cause: The storage resources required by the dataset are not allocated to the current namespace.

Solution: Go to the Resource Management page as an O&M administrator and allocate resources to the namespace.

2. **After a file is uploaded and a new subset is created, the**

**number of rows or size displayed on the Datasets page is unchanged.**

Problem: After a file is uploaded and a new subset is created, the number of rows or size displayed on the Datasets page is unchanged.

Cause: The dataset statistics on the Datasets page are updated every 1 hour. The number of rows and size of the statistics are the size of the subsets, excluding the original file.

Workaround: Check the Datasets page 1 hour after the file is uploaded.

<a id="section-4-2-1-2"></a>

#### 4.2.1.2. Data files

This topic describes the issues that may arise when you use data files, and the possible causes of and solutions to the issues.

1. **A CROS error occurs when you upload a file**

Problem: When you attempt to upload a file to Object Storage Service (OSS) on the Dataset Management > Data File tab, the file cannot be uploaded. The console prompts a Cross-Origin Resource Sharing (CROS) error.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/715a55e25611fc0ff575aa35f5a67681.webp)

Cause: The CORS feature is not configured for the OSS bucket associated with the dataset.

Solution: Log in to the OSS console and configure the following CORS rule.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/7dfa7e6d9c9e41ea01a95140d8f46ad9.webp)

2. **`"This request has content must be served over HTTPS"`**  **is reported when you**

**upload a file**

Problem: When you attempt to upload a file on the Dataset Management > Data File tab, the file cannot be uploaded. The console prompts the following error message:  `This request has content must be served over HTTPS` .

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/548ba7b53ca97928c62bf42c06fe397e.webp)

Cause: HTTPS is not enabled for the OSS bucket.

Solution: Log in to the OSS console and check whether HTTP-only access is enabled in the bucket policy. If not, enable HTTPS access. Check whether the access protocol for OSS resources is HTTP. If yes, switch to HTTPS.

3. **"The OSS Access Key Id you provided does not exist in our**

**records" is reported when you use a temporary credential to upload files**

Problem: "The OSS Access Key Id you provided does not exist in our records" is reported when you call API operations to obtain the upload credential of a dataset to upload a file.

Cause: The temporary credential has expired. Temporary credentials automatically expire upon the expiration time.

Solution: Obtain the expiration time returned by the temporary credential API operation, and renew the credential again before it expires.

4. **"Access denied by authorizer's policy" is reported when you**

**perform operations on a file by using a temporary credential**

Problem: "Access denied by authorizer's policy" is reported when you perform operations on a data file after you call the Dataset API operation to obtain a temporary credential for uploading or downloading a dataset.

Cause: The upload credential supports only the upload operation in the corresponding dataset directory. The download credential provides only the download operation in the corresponding dataset directory. The preceding error message is reported when an unauthorized operation is performed, such as using an upload credential to download or delete an object or using an upload credential to upload an object to a path outside the dataset.

Solutions:

- To upload files, use the upload credential to upload files in the corresponding dataset directory.

- To download files, use the download credential to download files in the corresponding dataset directory.

- To delete files, call the dataset API operation to delete data files.

  5. **`"403 Forbidden"`**  **is reported when you delete a file**

Problem: On the Dataset > Data File tab, files can be uploaded and viewed, but the  `403 Forbidden`  error is reported when you click Delete.

Cause: Deletion permissions are not granted to the OSS role.

Solution: Check the OSS resources that you use and the role. Assign the  `DeleteObject` permission to the role in the OSS console.

<a id="section-4-2-1-3"></a>

#### 4.2.1.3. Data subsets

This topic describes the issues that may arise when you use the data subsets, the possible causes, and the solutions.

1. **"No found any file types match supported type" is reported**

**when you create or update a subset**

Issue: "No found any file types match supported type" is reported when your attempt to create a subset fails.

Causes:

- The file used to create the subset is not in the list of recognized file types.

- The wildcard character is invalid and cannot match the data file.

Solution:

- If the file that you want to use to create the subset is not in the list of recognized file types, you need to convert the file to a recognized file type.

- If you use a wildcard character to match files, you can click the Preview icon on the Data View tab after the configuration is completed. If the compilation is correct, the first 100 matching data files are displayed. Check whether the files meet your expectations.

**2."Found multi file modal in your paths" is reported when your attempt to create or update a subset fails**

Issue: "Found multi file modal in your paths" is reported when your attempt to create or update a subset fails.

Cause: When you configure a data file for a data subset, files of multiple modes are selected.

Solution: Retain only one model of files based on the error message.

3. **The system prompts that the paging data in the view is too**

**large to be previewed when you attempt to preview a subset**

Issue: The system prompts that the paging data in the view is too large to be previewed when you attempt to preview a subset.

Cause: When you load the data block where the subset page is located, the memory limit of 128 MB for a single query is exceeded. By default, each data block contains 1,000 rows of data.

Solution: Split the large field into multiple small fields or multiple rows of data.

4. **Subset creation or update fails**

Issue: After you open a dataset, the Create Subset and Update Subset buttons are dimmed. As a result, you cannot create or update subsets.

Cause: Only the dataset creator and namespace administrator have the permissions to modify subsets.

Solution: Acquire the namespace administrator role.

<a id="section-4-2-2"></a>

### 4.2.2. Data processing

<a id="section-4-2-2-1"></a>

#### 4.2.2.1. Create a knowledge base parsing service

1. **Create an online service**

The procedure to creating an online service is the same as to creating an online parsing service path.

**1.1. Basic information**

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/c579e790ea4a7e38a0dc325c837ce66f.webp)

Turn on Image Deployment. You do not need to select a model.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/46aa0b20b4617ce9e5f300a67b1114f5.webp)

**1.2. Select a resource group**

If you use document deep analysis, you need to select a resource pool with intelligent computing equipment. In this example, basic parsing is used.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/63d2c39c6a20280585d1e11bd155a352.webp)

**1.3. Select a service image**

For the production environment, you can select a public image. Select a CPU for basic parsing and a GPU for deep parsing.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/a73539cbc4296e5f5702f0c414322c13.webp)

**Images for the Enterprise edition:**

- nvidia-dke-online-parser:cuda12.6-ubuntu22.04-py3.10-v3.0

- cpu-dke-online-parser:ubuntu22.04-py3.10-v3.0

- apg-dke-online-parser:cuda12.6-ubuntu22.04-py3.10-v3.0

- ascend-dke-online-parser:cuda12.6-ubuntu22.04-py3.10-v3.0

- dcu-dke-online-parser:cuda12.6-ubuntu22.04-py3.10-v3.0

**For a test environment, you can select a custom image.**

For more information about how to upload a custom image, see Upload a custom image.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/20b93e7713ce7b48b1da34074cad6203.webp)

**1.4. Configure the service**

- Classic Network Access: must be enabled. However, it can be skipped when you turn on AI Gateway.

- AI Gateway: Optional. The AI gateway supports monitoring. You can enable asynchronous inference. For more information, see Create an AI gateway.

- Port: Configure Service Port and Container Port, as shown in the following figure.

- Startup Commands: Enter the startup command, as shown in the following figure.

- Environment Variables: Enter environment variables, as shown in the following figure. SERVER_WORKERS indicates the inference parallelism capability, which can be adjusted based on the resource configuration.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/b7626054148e77081903acd37aafc20b.webp)

The following table describes some other parameters:

| Environment variable | Description | Suggested configuration | Value |
| --- | --- | --- | --- |
| SERVER_WORKERS | The number of workers (maximum number of concurrent requests). | 8 | 8 |
| SERVER_PORT | Service port number | 8001 |  |
| RUNTIME_SHARE_PAT H | The path to store log files and artifacts. | /runtime_share | /runtime_share |
| START_TRITON_SERVE R | Specifies whether to start the Triton inference server. | 1 | 1 |

**1.5. Advanced settings (optional)**

Enable asynchronous inference, which allows you to manage Kafka request queues and persist parsing results.

For more information about how to create a Kafka instance and a topic for asynchronous inference, see Create a Kafka instance and a topic.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/a099c7cd20bd12f2e65322453a0ed0c8.webp)

**1.6. Create the service**

After you click OK, a record is added to the service list, as shown in the following figure.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/dec000ac32b975555cd6c49d024af72d.webp)

Wait until the deployment is completed.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/75f8ab1eb4044acf77f8736b52201283.webp)

**1.7. Associate with an API key**

Create an API key. We recommend that you do not use the admin account.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/63bbde3ad832055dbc1bf3e90fcb4c0d.webp)

Associate the service with the API key.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/5ecc67e6e0bca65ddb80521f598d1149.webp)

**1.8 Connect to a model**

After the online service is started, you need to go to the operation management page to connect it to a model before you can use the service.

Switch the user who created the API key to the resource administrator role, and go to the operation management page.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/59d2846f7f7426a299a32e0406e989d7.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/3bc66b537f436b1aea393b01cb4f387a.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/c43a67883510d01df0960c0143298642.webp)

Click + Access model, select Online Parsing Service as the model type, and select the API key that is associated with the service. You can select Global Space as the effective space.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/d81813ceef7131d894013657ce58493b.webp)

After the model is created, debug it until it is error-free, and then click Debugging passed. The button becomes green.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/93aad3d7914c0ee049dcccd22f1fa15e.webp)

Return to the model list, find the model, and then click Enable. Then, the model is available in the knowledge base.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/42f3be040cbbf86bf1e1380eb92a2eaf.webp)

<a id="section-4-2-2-1-1"></a>

##### 4.2.2.1.1. Upload a custom image

**Upload an image**

Apsara Stack Container Registry requires you to create a repository in your test resource set and change the password. In most cases, the AliOS%1688 is used.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/aee6baf0c3d014bcecbd0f19f9b623fe.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/29fc1094dac6a1b2c06d220da95eedfc.webp)

```text
# Upload a local image to the remote end.
podman push reg.docker.alibaba-inc.com/dke/data-mixer-operators:2.1.1-hotx.3-cpu-1031-release --creds=ascm-org-1756263186183:AliOS%1688 --tls-verify=false docker://cr-ee.registry.cn-wulan-env38g1-d02.inter.env223.shuguang.com/dke/data-mixer-operators:2.1.1-hotx.3-cpu-1031-release

# Use the skopeo command on Linux and Windows operating systems.
skopeo copy \
  --src-tls-verify=false \
  --src-creds chihou.wc:chihou@aliyun \
  docker://reg.docker.alibaba-inc.com/dke/data-mixer-operators:2.1.1-hotx.3-gpu-1110-release \
  docker://cr-ee.registry.cn-wulan-env17e-
d01.inter.env17e.shuguang.com/aipaas_test/data-mixer-operators:2.1.1-hotx.3-gpu-1110-release \
  --dest-creds ascm-org-1760067243940:AliOS%1688 \
  --dest-tls-verify=false
```

**Custom images**

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/1d990677bbc2d19cd2579e2f3529b43c.webp)

Note: You must manually add a version for uploaded images.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/60102ef37b28895bafefa0ee1cc1210e.webp)

<a id="section-4-2-2-1-2"></a>

##### 4.2.2.1.2. Create an AI gateway

**Create a cluster**

https://one.console.con.env17e.shuguang.com/cop/gateway

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/10f63ac537d311afc9670d81a7e735fc.webp)

Take note of the following two items:

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/327a38c27bb6a683170b118206a31c91.webp)

**Create an AI gateway**

An error was reported when I saved the configurations. However, the gateway is eventually created.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/92cc5325d82dfc8e55e826f7793e1923.webp)

**Configure the AI gateway**

Associate with the gateway that you created.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/57bb7843c99c5691c761787aafdd8167.webp)

<a id="section-4-2-2-1-3"></a>

##### 4.2.2.1.3. Create a Kafka instance and a topic

**Create a Kafka instance**

First, find the ID of the virtual private cloud (VPC) in which the cluster of the AI gateway is created and record the VPC ID.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/bea870ea7c0be796952f7980d204f06b.webp)

When you enable asynchronous inference, the vSwitch ID is prompted. Record the vSwitch ID.

Create a Kafka instance and use the preceding VPC and vSwitch.

**Create an SASL user and grant permissions**

Create a user. Username: aistudio. Password: Admin123@ascm.

Creates three access control lists (ACLs).

**Create a partition**

<a id="section-4-2-2-1-4"></a>

##### 4.2.2.1.4. Create a VLM inference service

**Create a service**

Step 0: Go to the MaaS marketplace to download the desired model. In this example, the Qwen 2.5 model is used. In this case, search for  `Qwen2.5-VL-7B-Instruct` .

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/c30d33bbba490cbbc564032b1191f624.webp)

Step 1: Create an online service, select 16 cores, 64 GB, 64 GB of shared memory, and 1 GPU (A10 or A100).

Step 2: Select an image, such as nvidia-vllm-lws.

Step 3: Select the model  `Qwen2.5-VL-7B-Instruct`  and the mount path  `/models/Qwen2.5-VL-7B-Instruct` .

Step 4: Enable the classic network. If you do not enable the classic network, you must enable the AI gateway. Otherwise you cannot call the AI gateway.

Step 5: Configure a port and a startup command. In this example, the container port 8000 and startup command ( `--tensor-parallel-size`  equals the number of GPUs) are used.

```text
python3 -m vllm.entrypoints.openai.api_server --max_num_batched_tokens 65536 --dtype bfloat16 --gpu-memory-utilization 0.9 --tensor-parallel-size 1 --trust-remote-code --served-model-name Qwen2.5-VL-7B-Instruct --model /models/Qwen2.5-VL-7B-Instruct --disable-custom-all-reduce --host 0.0.0.0 --port 8000
```

(Optional) Step 6: After the AI gateway is created, enable it and add a web page link.

**Test the model**

Check the call information. The office network is accessible over the classic network address. Note that you need to manually allow access to the address.

```bash
curl -X POST 'http://d4e36c8d.classic.inter.env17e.shuguang.com/v1/chat/completions' \
-H 'Authorization: Bearer sk-3daefc8d0d0b9040b7' \
-H 'Content-Type: application/json' \
-d '{
    "messages": [
        {
            "role": "user",
            "content": [
                {
                    "text": "Who is Columbus?",
                    "type": "text"
                }
            ]
        }
    ],
    "model": "Qwen2.5-VL-7B-Instruct",
    "temperature": 1.0,
    "top_p": 1.0,
    "presence_penalty": 0.0,
    "max_tokens": null,
    "stream": false
}'
```

```bash
curl -X POST 'http://d4e36c8d.classic.inter.env17e.shuguang.com/v1/chat/completions' \
-H 'Authorization: Bearer sk-3daefc8d0d0b9040b7' \
-H 'Content-Type: application/json' \
-d '{
    "messages": [
        {
            "role": "user",
            "content": [
                {
                    "image_url": {
                        "url": "http://dke.oss-cn-wulan-env17e-d01-
a.inter.env17e.shuguang.com/datasets%2Ftest%2Fimage_0001.jpg?
Expires=1762528157&OSSAccessKeyId=w0mbe5gdBHxX4y5r&Signature=GZFQYP%2BSwh4NHl3iA%2BWi7NCU
c%3D"
                    },
                    "type": "image_url"
                },
                {
                    "text": "You are an intelligent image description assistant, please 
use short statements to describe the content of the figure. ",
                    "type": "text"
                }
            ]
        }
    ],
    "model": "Qwen2.5-VL-7B-Instruct",
    "temperature": 1.0,
    "top_p": 1.0,
    "presence_penalty": 0.0,
    "max_tokens": null,
    "stream": false
}'
```

<a id="section-4-2-2-2"></a>

#### 4.2.2.2. Troubleshoot knowledge base document parsing issues

**Check service availability**

Log on to OpenTrek Agent Dev as a Resource Set Administrator or an O&M administrator:

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/c65d7ddb5bc8b8ab3cb3a5640ad07f75.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/56cdcbec5165f9562eb22a1e3e86932c.webp)

Go to the registered online parsing service, click Debug, and check the service connectivity. A returned result indicates that the service is available.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/a113e268aa56f3be3a8bc77d601b5147.webp)

**View service logs**

Go to the AI Studio product page, navigate to Online Service, find the manually deployed online parsing service, and click it to open the details page.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/db4becc95c039d7f489c23fff5acb2fb.webp)

Check the replica running status on the Resource Instance page to confirm normal operation, and click Log to check for errors.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/781881effcc48fdfe9b16c7e0c2435fb.webp)

To view complete logs, go to the Event & Log page.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/bab3f226ad2df675ec3a75e48caebdad.webp)

If the instance status is abnormal, go to the Event page to view Kubernetes events.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/377d8ea3d35a474f79b1d82d6f13de08.webp)

**Common issues**

1. **Online service restarts due to OOM kill**

Excessive concurrency or large individual files can cause the parsing process of an online instance to restart due to out-of-memory (OOM). You can change the service configuration based on actual needs and adjust the CPU, memory, and shared memory settings. Recommended configurations:

- NVIDIA GPUs: 8 vCPUs, 32 GB memory, and 16 GB shared memory per replica, with worker=8

- APG GPUs: 8 vCPUs, 80 GB memory, and 16 GB shared memory per replica, with worker=4

- Hygon GPUs: 8 vCPUs, 80 GB memory, and 16 GB shared memory per replica, with worker=4

- Huawei GPUs: 8 vCPUs, 80 GB memory, and 16 GB shared memory per replica, with worker=4

To change the configuration, stop the service first. On the Online Service list page, find the target service and click Service Configuration > Resource Change on the right side.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/b28ae704faacbec9fbdd0d5891a85936.webp)

Enter the new resource configuration in the dialog box, click OK, and then click Restart. Wait for the service to start successfully.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/cf9c9da9a5dbbf4e6eb206a6066c2902.webp)

<a id="section-4-2-2-3"></a>

#### 4.2.2.3. Perform a hot upgrade on the image of a knowledge base parsing service

Step 1: Push the image that requires a hot update to the tenant-side Container Registry instance, create a custom image, and add an image version. For more information, see Upload a custom image.

Step 2: Stop the online service and click Modify Configurations.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/40e22de6b3c3d58a34155fd9198f55a9.webp)

In the panel that appears, select the custom image that you uploaded and click OK. Return to the service list, find the service and click Restart to restart the service.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/18e2a8c8ec4f4a936d48d9333deda8b5.webp)

<a id="section-4-2-2-4"></a>

#### 4.2.2.4. Troubleshooting processing tasks

1. **View the execution log of a processing task**

**1.1. Go to the Log tab**

Go to the Task Execution Overview page, search for the task by its name or enter the name and click O&M in the Operation column, find the job that you want to view, and click Detail in the Operation column.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/d1bb42a493825140d226dd0fd600ecc9.webp)

Click the Log tab.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/79a6e332a01abc85f30622e9e0d01f63.webp)

**1.2. Check the task configuration**

Find  `cfg.process is:`  and find the corresponding parameter setting.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/ea0d3c523346dfa350133f2eb9591c54.webp)

Confirm which operators and parameters are used.

**1.3. Find the operator that triggers the error**

Run the `- OP [`  command to query which operators are executed and which triggers the error.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/bc0d7757aeb8608956c7e680cd8d2d44.webp)

A summary log entry is generated after every operator is executed. The log entry includes the execution time and number of output samples.

**1.4. Check the error details**

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/6baf637e84537c8410b15afc5c7085c9.webp)

As shown in the preceding figure, you can find the cause of error in the stack trace of the Python log.

2. **Troubleshoot the parsing failure caused by the PDF source**

**file conversion failure**

The log includes the soffice and logic of the conversion failure.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/9d8b824c225d937e09f59e4741033d2b.webp)

If the source file cannot be automatically converted to a PDF file for parsing, the file may be excessively large or corrupted.

3. **Thoroughly analyze the error. The error message includes**

**both expand_page_images_to_rows_mapper and image_caption_backfill_selector.**

[2026-01-08 16:14:58.286] 2026-01-08T16:14:58.281+08:00 | INFO | data_mixer_operators.core.data:240 - OP [expand_page_images_to_rows_mapper] Done in 1.213s. Left 192 samples.

[2026-01-08 16:14:58.292] 2026-01-08T16:14:58.289+08:00 | ERROR | data_mixer_operators.utils.error_handler:44 - An error [DATA-403] &lt;Unexpected error occurred in Op [image_caption_backfill_selector]: dict_keys(['imagePath', 'pageNumber','pageReadingOrder']) doesn't meet the req of ['pageNumber', 'pageReadingOrder','imagePath', 'imageCaption'].> occurred in operation image_caption_backfill_selector when processing sample: Dataset({

[2026-01-08 16:14:58.292] features: ['__idx', 'doc', '__dm__stats__', 'converted_doc','layout_analysis', '__tok...

[2026-01-08 16:14:58.292] 2026-01-08T16:14:58.290+08:00 | ERROR | data_mixer_operators.core.data:244 - GLOBAL ERROR LOG: An error occurred during Op [image_caption_backfill_selector], pipeline crashed.

The preceding log entries show that the **Enhanced image parsing of the PDF file layout -Image decompression** operator is executed. In this case, expand_page_images_to_rows_mapper is directly followed by the error of the operator **Enhanced image parsing of the PDF file layout - Image analysis and content merging**. The content input to image_caption_backfill_selector is incorrect.

This indicates that the user execution path configuration is incomplete. For in-depth parsing paths, you need to configure all the following operators:

**Enhanced image parsing of the PDF file layout - Image decompression**

**Enhanced image parsing of the PDF file layout - Image enhancement service call**

**Enhanced image parsing of the PDF file layout - Image analysis and content merging**

You can enable or delete the preceding operators at the same time.

Users may delete only the operator Enhanced image parsing of the PDF file layout - Image enhancement service call due to the lack of a VLM model in the environment.

This issue can be resolved by deleting the preceding three operators.

4. **An error is reported during deep parsing, and the log**

**contains "Failed to convert document"**

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/ce442bfa66b8ca96596013bddb46a530.webp)

In the PDF parsing path, an error is reported when the preset conversion file format is supported. You need to check whether the source file format is invalid. Perform the following steps to troubleshoot the issue:

1. First, use the corresponding PC application, such as Word, Excel, or LibreOffice, to open the file, and confirm that the file can be opened.

2. Save the file as a new file and compare the size difference between the source and new files, such as the following document. The result shows that the files are not the same. This indicates that the original file format is invalid and is automatically fixed by the application.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/d900402ad119d49faf244daf099a6170.webp)

3. Parse the new file, and it can work as expected.

4. Directly save the source file as a PDF file on the PC and analyze the PDF file.

   5. **Analyze the content of the knowledge chunks to find**

**whether duplicate chunks exist. The analysis result shows that chunkBboxs contains duplicate chunks.**

In the list of chunks, chunkBboxes contains duplicate chunks. For example, in the knowledge chunks of the following file, two chunks with different chunkContent have the same chunkBboxs.

Cause:

- The parsing result of the file is split into different paragraphs by page and saved as a result list.

- The length of the paragraphs varies. If the length of a paragraph exceeds the upper limit of a knowledge chunk, the paragraph is split into two chunks.

- Both chunks include the same chunkBboxes, which is used to trace the source of the chunk.

The first knowledge chunk ends at the text "... lifeless".

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/ba4305571cfa51edc26074ee00013ca3.webp)

Before the text "... lifeless", an overlap token is added to the second chunk, and the text is:

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/44175fef8b6dc75e655ea9bc95d8ecfc.webp)

6. **The PPU environment reports the following error message:**

**processor running error: [500] in ensemble'layout_analysis_ensemble', Stub process'layout_analysis_det_0_3' is not healthy.**

Conclusion: **The PyTorch Processing Unit (PPU) environment consumes more memory than NVIDIA GPUs. This error is reported when the Out Of Memory (OOM) model process is terminated. We recommend that you allocate at least 70 GB of memory to ppu-1.4.3, and at least 50 GB of memory to ppu-1.5.1.**

Symptom: The Triton service runs as expected for the first few times after it is started (in the 99 test environment), and the layout_analysis_det_0_3 model remains unhealthy after a certain run.

Run the dmesg -T command to query OOM events:

```text
[5. 14:29:16, May 30, 2025] triton_python_b invoked oom-killer: 
gfp_mask=0xcc0(GFP_KERNEL), order=0, oom_score_adj=0
[5. 14:29:16, May 30, 2025] oom_kill_process.cold + 0xb/0x28
[14:29:16, May 30, 2025] [ pid ] uid tgid total_vm rss pgtables_bytes swapents 
oom_score_adj name
[5. 14:29:16, May 30, 2025] oom-kill:constraint=CONSTRAINT_MEMCG,nodemask=
(null),cpuset=0d3888b689ecbb71ff8e119e700b4302822812bbb6fd16dd6cb68ddb7467d944,mems_allow
=0-
1,oom_memcg=/docker/0d3888b689ecbb71ff8e119e700b4302822812bbb6fd16dd6cb68ddb7467d944,task
emcg=/docker/0d3888b689ecbb71ff8e119e700b4302822812bbb6fd16dd6cb68ddb7467d944,task=triton
ython_b,pid=1355052,uid=0
[5. 14:29:19, May 30, 2025] oom_reaper: reaped process 1355052 (triton_python_b), now anon-rss:0kB, file-rss:0kB, shmem-rss:9896kB
```

In the Docker startup parameters, 8 GB of memory is allocated, and mem_swap is enabled.

Run the docker stats command to check whether the allocated memory takes effect.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/9c21fc77e93555c593538917120abafd.webp)

The following dependencies and triton-ppu base images are not aligned.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/727cff551edd721d731477d7ff326304.webp)

The misalignment does not affect the business.

7. **The PPU environment report the following error message:**

**layout_analysis.utils.element.DocException: process page error: pool index 85 process time too long, cancel with timeout!**

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/142b6158c57984f616aef4b152e604cf.webp)

The model timed out during processing and reduced the concurrency from np=4 to np=2.

8. **The H200 environment reports the following error message:**

**unable to enqueue for inference table_cell_detect_0_1**

The path execution log shows that the PDF file can be recognized by other models, but an error is reported when the table parsing submodel is executed. The chunk generated from table parsing in the dataset execution result is empty.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/70efb6dc5b90d9a18f13bd42a3eb782a.webp)

Troubleshooting algorithms executed on the site detect that the model files are compiled by using the H20 drive. On-site table parsing reports an error.

Solve the issue by directly compiling the model files on the site. If similar issues arise, check the GPU model and drive. Contact on-site algorithm engineers for model compiling if necessary, and generate compatible model files.

9. **File download from the parsing path fails**

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/bf9d9dedf8b63549baababc0ca50d243.webp)

In the current version, Referer configuration is enabled for all web services. For example, hotlink protection is enabled for Object Storage Service (OSS).

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/53edac88fdf8fbe177c21f152780b116.webp)

The address of the hotlink protection configuration must be the same as the Referer configuration used in the environment. The HTTPS protocol is not used in the inter.env\*.\*.com address in the preceding figure. The service can run as expected only if the address starts with https://.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/99292f13b5d6f394105f69a6144b4ad1.webp)

10. **Startup failures of common GPU model services. If a service**

**cannot run, check for image packing errors. If such errors exist, contact the image publisher and perform a hot update on the image.**

Screenshot of the error:

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/955e4919ee1fcad00175a0669c87ef05.webp)

**Note: In versions 211 and earlier, the following error is reported because the restart logic of the algorithm contains errors. You do not need to update the image. You only need to manually restart the container.**

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/c140451d9a17a8ef9ebde3fbf06daab1.webp)

When an error-free Triton model is started, all model services are in the ready state.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/ad235db99baca177fce6b39800ae83ab.webp)

The model can be started without errors, but the Triton service cannot be called:

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/4093354cf6911dd75d605c25e6c91973.webp)

Run the  `dmesg -T`  command to check for OOM killer events.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/a6630776283cf0816d0fea1cbdfe41e1.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/4638500e35ef4010d291cce9d48e71c5.webp)

Ask the algorithm for memory requirements:

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/5d0952a595444094b0061738df3f4fce.webp)

Adjust the memory, include the limits and requests, of the Deployment corresponding to the online service to 50 GB as needed.

12. **The DCU environment reports that the online parsing**

**service failed to be called.**

This issue is similar to the previous issue. Run the  `dmesg -T`  command to check for OOM killer events. The following figure shows the required memory:

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/21d8574285687f1a0dfaacf38d726353.webp)

Adjust the memory, include the limits and requests, of the Deployment corresponding to the online service to 80 GB as needed.

13. **How do I enter an online container to manually restart the**

**Triton inference server?**

Enter the cluster in which the online service is deployed. In most cases, the  `/root/.kube` directory contains kubeconfig.

```bash
cd /root/.kube
# Assume that the cluster is Beijing A10. Set the KUBECONFIG environment variable.
export KUBECONFIG=/root/.kube/config_A10_beijing
# Find the running online instance.
kubectl get pod -A | grep elastic | grep Running

# Enter the container.
kubectl exec -it -n xlm-cluster-alpqxj dke-elastic-pod-lpl4pm6l3uhn-54d8688777-k4qd8 -cserver -- bash
```

Run  `cat /home/admin/bin/start.sh`  to query the startup command of the Triton inference server.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/69539c861a89b8d8b423cbb216dbbd58.webp)

Copy the command marked by the red box and execute the command directly on the terminal. You can view the log  `tail -fn1000 /tmp/tritonserver.log`  for verification. If all table models are ready, the model can be started as expected.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/706556b38f4b3210b1364ee02f874d3b.webp)

14. **Common bounding box (bbox) logic in document deep**

**analysis task results**

In the output of document deep parsing tasks, the bbox position in the common parsing content is expressed in the format of an array, as shown in the following example:

**Example:**

[0.1250, 0.2500, 0.1667, 0.2500]

**Assume that:**

Page size: width = 800, height = 600

bbox: x0 = 100, y0 = 150, x1 = 300, y1 = 250

**Calculation:**

x0/width = 100/800 = 0.1250

y0/height = 150/600 = 0.2500

(y1-y0) ÷ height = (250-150) ÷ 600 = 100 ÷ 600 ≈ 0.1667

(x1-x0)/width = (300-100)/800 = 200/800 = 0.2500

**Meaning:**

The bbox starts at 12.5% on the left and 25% on the top of the image, with a height of 16.67% of the image and a width of 25%.

<a id="section-4-2-2-5"></a>

#### 4.2.2.5. Perform a hot update on a control application

The data processing control application must include data-engine-console and data-engine-workflow. Their update methods are the same.

1. **Obtain the image file**

In most cases, the image file is an OCI file, which is provided by the manufacturer or the R&D team.

2. **Distribute the image to the customer repository**

Run the following Skopeo commands to push the application image OCI file to the image repository:

```text
# sfm-kn-data-engine
skopeo copy oci-archive:sfm-kn-data-engine_2.1.0-hotx.1.oci 
docker://__your_repo_endpoint__/sfm/sfm-kn-data-engine:<YOUR_TAG>

# sfm-kn-workflow
skopeo copy oci-archive:sfm-kn-workflow_2.1.0-hotx.1.oci 
docker://__your_repo_endpoint__/sfm/sfm-kn-workflow:<YOUR_TAG>
```

3. **Update the image**

Note: Back up the original configurations. Sample command:  `kubectl get pod -n sfm data-`

```text
engine-workflow -o yaml > data-engien-workflow_deploy.yaml.bak 
```

Enter the OPS cluster and modify the deployment configuration of the corresponding control application.

```bash
# data-engine-workflow. Add the latest image tag to the image.
kubectl edit deploy -n sfm data-engine-workflow

# data-engine-console. Add the latest image tag to the image.
kubectl edit deploy -n sfm data-engine-console
```

After the modification, the image automatically restarts. The following status shows that the image is updated.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/f24b5eafd6970a211a244d0d1e0ef694.webp)

After the update, check whether the service features are affected.

<a id="section-4-2-2-6"></a>

#### 4.2.2.6. Perform a hot update on an offline image

1. **Obtain the image file**

In most cases, the image file is an OCI file, which is provided by the manufacturer or the R&D team.

2. **Distribute the image to the customer repository**

Run the following Skopeo commands to push the processing task image OCI file to the image repository:

Note:

1. To facilitate rollback, do not overwrite the existing image of the customer. Add  `-MMDD-release`  to the tag, which indicates the update time.

2. 2.1.1-hotx.2 is a recent version. Offline and online services use the same image. You only need to push the image once.

```text
# NVIDIA: offline and online.
skopeo copy oci-archive:data-mixer-operators.offline.gpu.oci 
docker://__your_repo_endpoint__/sfm/data-mixer-operators:2.1.1-full-tritionserver-inclmodel-MMDD-release

# PPU (T-Head APG): offline and online.
skopeo copy oci-archive:data-mixer-operators.offline.ppu.oci 
docker://__your_repo_endpoint__/sfm/data-mixer-operators:2.1.1-non-sci-tritionserver-ppu-inclmodel-MMDD-release

# DCU (Hygon K100 and BW1000): offline and online.
skopeo copy oci-archive:data-mixer-operators.offline.dcu.oci 
docker://__your_repo_endpoint__/sfm/data-mixer-operators:2.1.1-non-sci-tritionserver-dcu-inclmodel-MMDD-release

# Atlas (Huawei 910B): offline and online.
skopeo copy oci-archive:data-mixer-operators.offline.atlas.oci 
docker://__your_repo_endpoint__/sfm/data-mixer-operators:2.1.1-non-sci-tritionserver-atlas-inclmodel-MMDD-release
```

**Note: If the Skopeo commands cannot be installed or used, run the Skopeo commands of the sfm-deploy-tool image to push the image.**

```bash
# The configurations are for reference only. Adjust the configurations based on your business requirements.
docker run --rm -it --name skopeo -v /root/data-mixer/2.1.1-hotx.2/data-mixer-operators.gpu.oci:/app/data-mixer-operators.gpu.oci sfm-deploy-tool:1.0.0 skopeo --insecure-policy copy --dest-creds username:pwd --dest-tls-verify=false oci-archive:/app/data-mixer-operators.gpu.oci docker://acr-opentrek-prd-registry-vpc.cn-
shanghai.cr.aliyuncs.com/sfm/data-mixer-operators:2.1.1-hotx.2-gpu-MMDD-release
```

3. **Modify the database image tag**

**First, back up the kn_kv table configuration of the customer.**

**First, back up the kn_kv table configuration of the customer.**

**First, back up the kn_kv table configuration of the customer.**

**3.1. Standard update process**

Because the suffix  `-MMDD-release`  is added to the tag, you need to modify the default image tag for database update.

For more information about how to connect to a database, see the "Other questions" section of this topic.

Tag for an offline image with an NVIDIA GPU:

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/66cdf4559512ade20c4b328b5994753a.webp)

Tag for an offline image in the PPU environment:

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/bc800080a37d7def12dfba2d963041f8.webp)

```sql
# Update the corresponding tag based on the value.
# Note⚠️: You must store the tags of historical images. If the new image encounters issues, you can update the database and roll back to the previous image.
# For example, update the tag of an image with an offline NVIDIA:
update kn_kv set value='2.1.0-full-tritonserver-inclmodel-0810-release' where 
value='2.1.0-full-tritonserver-inclmodel-0804-release';
```

**3.2. Special scenario: If the process.imageTag.xxx field does not contain the customer GPU model.**

For example, no support is provided for less commonly used Huawei, Hygon, and NVIDIA A800, H200, and H100 models. Therefore, you need to manually add the mappings between the GPU model and image tag to the database.

In some projects, the GPU model is manually specified. Make sure that you check the model before you modify data in the database.

The following figure shows the H200 GPU model in the resource group.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/dcc1e3ca6ff0c809889d9c2c859b0be2.webp)

In this case, execute the following SQL statements. The value is the image tag of data-mixer-operators.

```sql
insert into public.kn_kv (key, value)
values ('process.imageTag.NVIDIA-H200', '2.1.1-non-sci-tritonserver-inclmodel');
```

4. **Use the updated image**

**4.1. New tasks**

New tasks directly read the image tag from the database and directly use the new image.

**4.2. Existing tasks**

The image tag of existing tasks do not automatically update. You need to decommission the task, modify the image tag, save the configuration, and publish the task again.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/2ae6b30c08aa576fffa064ec71f66b60.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/58116e8ec3fcddd7c3e2e0dd881af821.webp)

Save the configurations without modification.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/fa0f88682c594ff468f0a9cc56bce99e.webp)

After you publish the task, click Run to apply the new tag.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/79d68e9c390d5cfafa00ace678896f06.webp)

**4.3. Confirm that you want to use the new image**

On the Task Execution Overview page, find the task that you want to view, click Detail in the Operation column, and then click the Log tab. Find the log entry that starts with "Successfully pulled image". If the tag is the one that you configured, the image is updated.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/ca0fbdfd7e7d27124c23f93c0f042034.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/6d6a4163d35eb47a08bce48443bb6149.webp)

**Other questions**

**How do I connect to a DKE database?**

```bash
# Query the information about the console database connection.
kubectl exec -n sfm $(kubectl get pods -n sfm -l "app=data-engine-console" -o jsonpath=
'{.items[0].metadata.name}') -- sh -c 'env | grep -E "postgres_host|postgres_port"'
kubectl exec -n sfm $(kubectl get pods -n sfm -l "app=data-engine-console" -o jsonpath=
'{.items[0].metadata.name}') -- sh -c 'env | grep knDataEngine'

# Query the information about the workflow database connection.
kubectl exec -n sfm $(kubectl get pods -n sfm -l "app=data-engine-console" -o jsonpath=
'{.items[0].metadata.name}') -- sh -c 'env | grep -E "postgres_host|postgres_port"'
kubectl exec -n sfm $(kubectl get pods -n sfm -l "app=data-engine-console" -o jsonpath=
'{.items[0].metadata.name}') -- sh -c 'env | grep knWorkflow'

# The following information is returned. The suffixes of knDataEngine and knWorkflow are different.
_AUTOCONF_postgres_host=pc-xxx.pg.polardb.rds.aliyuncs.com
_AUTOCONF_postgres_port=3433
_AUTOCONF_postgres_database_knDataEngine=kn_data_engine_ctl
_AUTOCONF_postgres_username_knDataEngine=polar_admin
_AUTOCONF_postgres_password_knDataEngine=xxx
```

<a id="section-4-2-2-7"></a>

#### 4.2.2.7. Video data processing FAQ

**Output dataset**

**Result subset not created**

**Error message**

The pipeline log shows an empty execution result.

```text
2025-09-11 17:09:02.367 | INFO     | data_mixer_operators.utils.trace_utils:36 - ==|> P
ROCESS_DATA took 52.0905 seconds <|==
2025-09-11 17:09:02.368 | INFO     | data_mixer_operators.core.executor:243 - All OPs are done in 52.091s.
2025-09-11 17:09:02.368 | INFO     | data_mixer_operators.core.executor:246 - Exporting 
dataset to disk...
2025-09-11 17:09:02.369 | WARNING  | data_mixer_operators.core.exporter:224 - Dataset is empty, skipping export.
     ,----.          ___        _ __     ,--.--------.                  
  ,-.--` , \  .-._ .'=.'\    .-`.' ,`.  /==/,  -   , -\  ,--.-.  .-,--. 
 |==|-  _.-` /==/ \|==|  |  /==/, -   \ \==\.-.  - ,-./ /==/- / /=/_ /  
 |==|   `.-. |==|,|  / - | |==| _ .=. |  `--`\==\- \    \==\, \/=/. /   
/==/_ ,    / |==|  \/  , | |==| , '=',|       \==\_ \    \==\  \/ -/    
|==|    .-'  |==|- ,   _ | |==|-  '..'        |==|- |     |==|  ,_/     
|==|_  ,`-._ |==| _ /\   | |==|,  |           |==|, |     \==\-, /      
/==/ ,     / /==/  / / , / /==/ - |           /==/ -/     /==/._/       
`--`-----``  `--`./  `--`  `--`---'           `--`--`     `--`-`      
```

**Cause**

Take the following processing task log as an example: After the image_aspect_ratio_filter operator finishes execution, it returns an empty dataset with the message "OP [image_aspect_ratio_filter] returns empty dataset". A comparison of the input dataset and the operator parameter configuration reveals that all input images are in portrait orientation, but the minimum aspect ratio of the operator is 1. As a result, the system filters out all input data.

```text
2025-09-11 17:09:01.682 | INFO     | data_mixer_operators.manager.download_manager:130 
- Downloading[opentrek] took 0.000992 seconds.
2025-09-11 17:09:01.695 | INFO     | data_mixer_operators.manager.download_manager:436 
- use cache skip download.
2025-09-11 17:09:01.696 | INFO     | data_mixer_operators.manager.download_manager:130 
- Downloading[opentrek] took 0.000856 seconds.
2025-09-11 17:09:01.708 | INFO     | data_mixer_operators.manager.download_manager:436 
- use cache skip download.
2025-09-11 17:09:01.709 | INFO     | data_mixer_operators.manager.download_manager:130 
- Downloading[opentrek] took 0.000853 seconds.
image_aspect_ratio_filter_compute_stats (num_proc=4): 100%|##########| 280/280 [00:01<00:00, 245.00 examples/s]
image_aspect_ratio_filter_process (num_proc=4):   0%|          | 0/280 [00:00<?, ? 
examples/s]
image_aspect_ratio_filter_process (num_proc=4):  25%|##5       | 70/280 [00:00<00:00, 613.39 examples/s]
image_aspect_ratio_filter_process (num_proc=4): 100%|##########| 280/280 [00:00<00:00, 
994.38 examples/s]
2025-09-11 17:09:02.245 | WARNING  | data_mixer_operators.core.data:257 - OP [image_aspect_ratio_filter] returns empty dataset.
```

**Solution**

Modify the parameter configuration of the operator based on your actual requirements.

**Result sample size smaller than expected**

**Symptom**

The video parsing result contains 8 keyframes, but the result subset contains only 2 samples after the frame extraction template finishes execution.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/bef3517b4240c76e88a04f21b163412d.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/cfa23349c08d829bbcda3a5c6c1811ac.webp)

**Cause**

In addition to the frame extraction operator, the frame extraction template also includes operators such as image blur filtering and image aspect ratio filtering. These filtering operators removed the missing samples.

**Solution**

Check the number of samples that each operator returns in the processing task log to identify which operator reduced the sample count, and then adjust the request parameters of the operator based on your actual requirements. Search for "Done in" in the log to quickly locate the operator execution results.

```text
[2025-09-17 11:06:52.543] 2025-09-17 11:06:52.542 | INFO     | 
data_mixer_operators.utils.trace_utils:36 - ==|> VideoParseOfflineMapper took 1286.2090seconds <|==
[2025-09-17 11:06:52.575] 2025-09-17 11:06:52.574 | INFO     | 
data_mixer_operators.core.data:261 - OP [video_parse_offline_mapper] Done in 1286.211s. 
Left 20 samples.
```

**Audio extraction, conversion, and upload -audio_extract_mapper FFmpeg execution failure**

**Error message**

The processing task log shows "Output file #0 does not contain any stream".

```text
2025-09-08 18:04:12.006 | ERROR    | data_mixer_operators.utils.exception_utils:13 - Traceback (most recent call last):
  File "/home/admin/data-mixer-
operators/data_mixer_operators/ops/mapper/audio_extract_mapper.py", line 156, in process
    raise RuntimeError(f"FFmpeg执⾏失败 (代码: {process.returncode}): 
{stderr_bytes.decode(errors='ignore')}")
RuntimeError: FFmpeg执⾏失败 (代码: 1): ffmpeg version 4.4.2-0ubuntu0.22.04.1 Copyright (c) 2000-2021 the FFmpeg developers
  built with gcc 11 (Ubuntu 11.2.0-19ubuntu1)
  configuration: --prefix=/usr --extra-version=0ubuntu0.22.04.1 --toolchain=hardened --libdir=/usr/lib/x86_64-linux-gnu --incdir=/usr/include/x86_64-linux-gnu --arch=amd64 --enable-gpl --disable-stripping --enable-gnutls --enable-ladspa --enable-libaom --enable-libass --enable-libbluray --enable-libbs2b --enable-libcaca --enable-libcdio --enable-libcodec2 --enable-libdav1d --enable-libflite --enable-libfontconfig --enable-libfreetype --enable-libfribidi --enable-libgme --enable-libgsm --enable-libjack --enable-libmp3lame --enable-libmysofa --enable-libopenjpeg --enable-libopenmpt --enable-libopus --enable-libpulse --enable-librabbitmq --enable-librubberband --enable-libshine --enable-libsnappy --enable-libsoxr --enable-libspeex --enable-libsrt --enable-libssh --enable-libtheora --enable-libtwolame --enable-libvidstab --enable-libvorbis --enable-libvpx --enable-libwebp --enable-libx265 --enable-libxml2 --enable-libxvid --enable-libzimg --enable-libzmq --enable-libzvbi --enable-lv2 --enable-omx --enable-openal --enable-opencl --enable-opengl --enable-sdl2 --enable-pocketsphinx --enable-librsvg --enable-libmfx --enable-libdc1394 --enable-libdrm --enable-libiec61883 --enable-chromaprint --enable-frei0r 
--enable-libx264 --enable-shared
  libavutil      56. 70.100 / 56. 70.100
  libavcodec     58.134.100 / 58.134.100
  libavformat    58. 76.100 / 58. 76.100
  libavdevice    58. 13.100 / 58. 13.100
  libavfilter     7.110.100 /  7.110.100
  libswscale      5.  9.100 /  5.  9.100
  libswresample   3.  9.100 /  3.  9.100
  libpostproc    55.  9.100 / 55.  9.100
Input #0, mov,mp4,m4a,3gp,3g2,mj2, from '/tmp/dm_video_4vo7cz01.tmp':
  Metadata:
    major_brand     : mp42
    minor_version   : 0
    compatible_brands: mp42isom
    creation_time   : 2018-11-14T02:30:13.000000Z
    encoder         : mp4creator 1.4.4
  Duration: 00:01:32.03, start: 0.000000, bitrate: 276 kb/s
  Stream #0:0(eng): Video: mpeg4 (Simple Profile) (mp4v / 0x7634706D), yuv420p, 1280x720 [SAR 1:1 DAR 16:9], 275 kb/s, 30 fps, 30 tbr, 90k tbn, 30 tbc (default)
    Metadata:
      creation_time   : 2018-11-14T02:30:13.000000Z
      vendor_id       : [0][0][0][0]
Output #0, wav, to '/tmp/dm_audio_ozay80n_.wav':
Output file #0 does not contain any stream
```

**Cause**

The input video file does not contain audio, which causes the operator execution to fail.

**Solution**

Use a built-in operator to filter out videos without audio in batches.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/bee5720f31d23504b8a71ecc4e1f0b91.webp)

**ASR model unavailable**

**Symptom**

The FunASR model drop-down list is empty and no model service is available.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/cd6d111c6a7332f9552f5e585d6287d0.webp)

**Cause**

No ASR service is deployed, or a service is deployed but not registered with OpenTrek Agent Dev.

**Solution** Go to AI Studio and use the public image cpu-funasr to deploy an online service. We recommend that you configure 16 vCPUs and 32 GB of memory for a single instance (no GPU required), which supports 13 concurrent requests. The following section describes only the key steps. For detailed operations, refer to the AI Studio documentation.

1. Deploy an online service in AI Studio.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/cef01437bd392a276edf138493f0a61d.webp)

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/f688af2b280e411aafa92bc29d6e953a.webp)

2. Register the AI Studio model service with OpenTrek Agent Dev.

   ![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/29a7478d3670e316b867dc940d7bd418.webp)

<a id="section-4-3"></a>

## 4.3. Model integration

**Troubleshoot AIStudio model connectivity failures**

- Check whether the network between the OP tenant zone and the AIStudio Model Service is connected. Run a curl command from the Application Agent pod to access the AIStudio VPC Endpoint and verify that Domain Name Resolution and Network connectivity function properly. If errors such as UnknownHost occur, the network is not connected. In this case, check whether both services reside in the same VPC. The Network deployment Architecture is as follows.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/95f2452610721505f563ab956a7cf440.webp)

- Use the model provider service code in OpenTrek Agent Dev to check whether the AIStudio Model Service is Running in the AIStudio console. If the Model Service is disabled or deleted, the Status is abnormal and you must Restore the service.

- Use the Model Service API key in OpenTrek Agent Dev to check the validity of the API key in the AIStudio console.

**Troubleshoot an empty model selection list in OpenTrek Agent Dev model integration**

Check the current logon method. You must Log In to OpenTrek Agent Dev through Role-based Authorization access.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/afdf1d28a904ef6c4025d654a135c419.webp)

Go to the AIStudio console and check whether the Model Online Service List contains any Running Model Service.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/3229a371bcc3933986abe00c88d20da8.webp)

**Troubleshoot an empty API key list in OpenTrek Agent Dev model integration**

Log In to the AIStudio console with the Resource Set Administrator Role of the current account and check whether the API key has the corresponding Model Service Binding.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/6915e7d1d23227d1a93bf8be4839630a.webp)

**Check the AIStudio Online Service status**

Use the service ID to Query the AIStudio Online Service and check the Model Service Status.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/12acc0cdb10a047c73d9f77d97d73db4.webp)

Check whether the AI Gateway is enabled. In the Access Setting section, verify that the AI Gateway is configured and that the VPC Endpoint exists.

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/172b587d33522a3b889b1695def410c7.webp)

API key validity check

![](en-opentrek-dev-operations-guide-v3.18.6-2607-20260902.assets/6915e7d1d23227d1a93bf8be4839630a.webp)
