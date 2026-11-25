Alibaba Cloud  
Apsara Stack  
OpenTrek AI Studio Product  
Introduction  
Product Version: V3.18.6  
Document Version: 20260630

**Table of Contents**

- [1.AI Studio](#section-1)
    - [1.1. Features](#section-1-1)
    - [1.2. Benefits](#section-1-2)
    - [1.3. Common scenarios](#section-1-3)
    - [1.4. Functions and features](#section-1-4)

<a id="section-1"></a>

# 1.AI Studio

AI Studio is a full-stack AI PaaS service platform for Apsara Stack. The platform provides AI developers with an AI engineering platform that includes dataset management, model development, model training, and model management.

<a id="section-1-1"></a>

## 1.1. Features

In terms of the functional architecture, AI Studio is divided into four layers: resources, model development and training, model service, and operation.

1. **AI resource layer:** You can use computing resources in the form of bare metal and EGS. You can use multiple types of local computing resources, such as Haoguang and Ascend, to meet the requirements of different computing power scenarios.

2. **Model development and training layer:** provides three model training methods: visual modeling, notebook modeling, and task modeling. It supports data sets of different storage types such as OSS Object Storage Service and CPFS file systems. It also supports mainstream model training frameworks such as TensorFlow, PyTorch, DeepSpeed, and Megatron. Comprehensive model training capabilities, such as integrated model development, training monitoring, training results recording, and deployment of trained models, are provided for standalone and distributed training scenarios.

3. **Model service layer:** supports online model service and batch inference, real-time monitoring of model service performance, and resource scaling configurations to ensure the stability of external services in a timely manner.

4. **AI operation:** You can Resource Management resources and training tasks at different levels and control metering and quotas to meet your requirements in intelligent computing operation scenarios.

<a id="section-1-2"></a>

## 1.2. Benefits

This topic describes the benefits of AI Studio.

**One cloud with multiple computing power**

Built on the AI computing power infrastructure provided by Apsara Stack, AI Studio allows users to select the appropriate computing power type for their specific scenarios. It supports multiple mainstream domestic GPU chips to meet various requirements for model training, inference, and other scenarios in government and enterprise environments.

**Systematic model training capabilities for the entire process**

AI Studio delivers integrated capabilities for the entire model training process through both single-machine and distributed training scenarios. These capabilities include model development, training monitoring, training result recording, and model listing.

**High availability**

Control services and model inference are designed with high availability. When a node of an online service or control service fails, other nodes automatically continue to provide services, ensuring uninterrupted operation.

**Open and efficient**

Models trained on the AI Studio platform or provided by users can be imported into the model marketplace through AI Studio, enabling users to efficiently manage and share models.

<a id="section-1-3"></a>

## 1.3. Common scenarios

AI Studio products can be applied to scenarios such as model development, model training, and model online services.

**Model Development**

Algorithm engineers or algorithm scientists can use Notebook modeling to develop models in the Notebook editor.

**Model Training**

Users can create task modeling tasks to perform standalone and distributed training on TensorFlow and PyTorch framework models. AI Studio can also monitor the resource usage and status during the training process to ensure the stability of the training process.

**Model Evaluation**

AI Studio supports issue evaluation tasks. After you associate an evaluation dataset with an evaluation task and set the relevant runtime environment, you can create an evaluation task. Model evaluation can be run at regular intervals.

**Elastic Algorithm Service (EAS)**

Deploy the model and provide the model API calling service.

<a id="section-1-4"></a>

## 1.4. Functions and features

This topic describes the features of AI Studio.

**Module**

**Description**

Displays the statistics on task modeling, online services, and datasets in

Overview

AI Studio. This allows you to intuitively and accurately understand the status of AI Studio.

- Supports manual annotation and automatic annotation.

- Supports annotation of image and text data. You can view and export annotation task results.

- Supports annotation task distribution for collaborative annotation and approval.

- Supports data processing algorithms.

Data Labeling

> **Note**
>
> Only classification algorithms for structured data are provided. Unstructured data is not supported.

Data Manag ement

Allows you to manage data in a centralized manner. You can upload processed training or evaluation data to a dataset and select the dataset during modeling or model evaluation. You can also view, upload, delete, and share datasets.

Dataset

> **Note**
>
> To upload data to a dataset, make sure that the data is transferred to Object Storage Service (OSS) or Cloud Parallel File Storage (CPFS).

Data

Allows you to increase the data volume of a dataset by using data

Generation

generation if the data in the dataset is insufficient.

Provides hundreds of AI algorithms that can be applied to various scenarios, such as product recommendation, financial risk control, or advertising prediction. Large-scale distributed training and workflow orchestration for streaming and batch processing are also supported. The following features are provided:

- Allows you to create, view, modify, clone, and run workflows.

- Allows you to view workflow tasks.

Visualized Modeling

- Allows you to create a workflow by using a preset template or a custom template.

- Provides built-in algorithm libraries.

- Supports instance monitoring, including the instance CPU, memory, GPU, and network monitoring. This feature depends on Prometheus and CloudMonitor.

- Allows you to deploy models as online services.

Provides an online interactive development environment. Notebook eliminates the need for users to prepare the development environment and helps users easily manage datasets, code, and models. The following features are provided:

- Allows you to create Notebook modeling instances.

Model

- Allows you to adjust resource quotas for instances.

Trainin

- Allows you to export instances as images.

g

- Allows you to change instance configurations.

- Allows you to view, stop, and start instances.

- Allows you to view instance events.

Notebook

- Supports Visual Studio Code and JupyterLab editors.

Modeling

> **Note**
>
> The same instance supports two types of editors. You can view the same file directory in two development environments.

- Supports SSH remote connections.

- Supports multi-person collaborative development.

- Supports instance monitoring, including the instance CPU, memory, GPU, and network monitoring. This feature depends on Prometheus and CloudMonitor.

- Allows you to save models.

Allows you to create standalone or distributed training tasks, and manage the lifecycle of tasks such as monitoring and deletion.

- Allows you to create, view, delete, start, and pause training tasks.

- Allows you to adjust resource quotas for tasks.

- Allows you to view task events and node events.

- Allows you to save models.

- Supports automatic fault tolerance. If a training task fails, the instance is restarted.

- Supports health checks. Before a training task starts, the computing power and network performance of the instances used for training are checked, and the instances with performance bottlenecks are restarted.

- Supports task monitoring, including the instance CPU, memory, GPU,

Task

and network monitoring. This feature depends on Prometheus and

Modeling

CloudMonitor.

- Allows you to view task logs.

- Supports checkpoint-based resumable training. You can select a checkpoint to resume a training task within seconds.

  > **Note**
  >
  > The checkpoint-based resumable training feature depends on CPFS.

- Allows you to adjust the priority of tasks. You can view the task list on the Task Modeling page and manually adjust the priority.

- Supports TensorBoard for visualized task running and analysis.

- Allows you to deploy models as model API services. This facilitates the development and usage of AI applications.

- Allows you to deploy, stop, and start online services.

- Allows you to view the details of services.

- Allows you to scale resources.

- Supports scaling.

- Allows you to upload a README file including online service

Online

descriptions. Only a PDF file can be uploaded.

Service

- Supports service monitoring, including the instance CPU, memory, GPU, and network monitoring. This feature depends on Prometheus and CloudMonitor.

- Supports resource inference of Elastic GPU Service. This features depends on Container Service for Kubernetes (ACK) and Elastic GPU Service.

Model

- Supports distributed inference by using an AI gateway.

Servic

- Allows you to perform throttling on online services.

e

Provides a unified access portal for multiple online services. Traffic allocation can be used to achieve smooth service publishing and unpublishing.

- Allows you to create, modify, and delete canary groups.

Canary Group

- Allows you to add multiple online services to a canary group.

- Allows you to perform throttling on online services by using canary groups.

Supports inference on multiple data entries and generates an inference result file.

Batch Inference

- Allows you to create, start, and pause batch inference tasks.

- Allows you to configure timing settings for batch inference tasks.

Allows you to perform model self-registration and model lifecycle management. The following features are provided:

- Allows you to upload, modify, deploy, share, enable, and disable models.

  > **Note**
  >
  > To upload a model, make sure that the model is transferred to OSS or CPFS.

Models

- Allows you to convert the format of a model from Megatron to Hugging Face or ModelScope, or from Hugging Face or ModelScope to Megatron.

- Allows you to manage model versions.

- Allows you to upload a README file including online service descriptions. Only a PDF file can be uploaded.

- Supports system models, custom models, and Model as a Service (MaaS) models.

Model Manag

Supports the following tuning methods: supervised fine-tuning (SFT),

ement

direct preference optimization (DPO), and group relative policy optimization (GRPO). You can specify the fine-tuning method and select appropriate fine-tuning data and parameters. The model performance

Model Tuning

after fine-tuning better meets your business requirements.

- Allows you to create model tuning tasks to optimize model training.

- Allows you to view, modify, stop, start, and delete tuning tasks.

Allows you to create an evaluation task after you specify the evaluation

Model

dataset and set the relevant environment. The evaluation algorithm and

Evaluation

evaluation result path need to be set in the evaluation code. You can create general evaluation tasks and scheduled evaluation tasks.

Allows you to convert the format of a foundation model from Megatron to

Model

Hugging Face or ModelScope for inference, or from Hugging Face or

Conversion

ModelScope to Megatron for training.

Allows you to create an AI resource pool to centrally manage the physical computing power required by the AI management platform and provide underlying computing power for model development, training, and tuning tasks.

- Allows you to create, view, modify, and delete AI resource pools.

AI Resource

- Supports GPU-accelerated cloud computing power that depends on ACK

Pool

and Elastic GPU Service, and supports GPUs such as A100 and Hygon K100.

- Supports bare metal computing power that depends on Bare Metal Computing Platform (BMCP) and ACK, and supports A100, Hygon K100,

AI

Ascend 910B, and APG810E.

Resour ce Manag ement

Allows you to allocate resources from a resource pool. After a resource quota is associated with a workspace, you can use the resource quota in the workspace for AI development and training. This way, you can use and manage resources in a flexible and efficient manner.

- Allows you to create, modify, and delete resource quotas.

Resource Quota

- Allows you to adjust specifications.

- Supports resource set sharing.

- Supports image, model, and computing power matching.

- Supports GPU sharing.

Agent

Allows you to deploy open source Dify instances based on your habits.

Develo

Dify Open

This provides end-to-end capabilities from model training and inference to

pment

Source

AI agent development and debugging, and accelerates the

Platfor

Edition

implementation of model services tailored to customer business scenarios.

m

Provides images of development and runtime environments for model development and training. This helps you quickly create development and training tasks.

- Allows you to upload, delete, modify, and share images.

  > **Note**

Image Repository

> Image upload depends on Container Registry Standard Edition or Advanced Edition.

- Allows you to manage image versions.

- Supports preset images.

AI

Allows you to compile the code that is required for training and manage

Asset

the code in a centralized manner by creating a code build. This improves

Manag

Code Build

the efficiency of code configuration in model training tasks. You can

ement

create, modify, delete, or share code builds.

Accelerates the loading of datasets and models during model training and

Data

inference. This improves the efficiency of training and inference. You can

Accelerator

create data accelerators to prefetch and cache datasets and model data stored in OSS.

<table>
  <tr>
    <td rowspan="2"></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Software Source</td>
    <td>Obtains software packages such as PyPI, YUM, Debian, and Conda packages from the Internet and caches them locally to form offline stores.Local offline stores can provide services without the need for Internet connections.</td>
  </tr>
  <tr>
    <td>Syste m Config uration s</td>
    <td>Synchronize Resources</td>
    <td>Allows you to synchronize inference images from the BMCP image center to the public image repository of AI Studio.</td>
  </tr>
</table>
