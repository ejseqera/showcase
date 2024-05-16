# Seqera Platform: Demonstration Walkthrough


<div style="display: flex; align-items: center; margin-bottom: 20px;">
  <div style="margin-right: 10px;">
    <a href="https://cloud.seqera.io/login" class="md-button" style="display: block; margin-bottom: 10px;">
      <i class="fas fa-user"></i> Login to Seqera Platform
    </a>
    <a href="https://seqera.io" class="md-button" style="display: block;">
      Visit Seqera Main Site
    </a>
  </div>
    <div style="flex: 1; margin-left: 200px;">
    <img src="assets/seqera-one-platform.png" alt="Seqera Biotech Stack" style="width: 100%; max-width: 750px;">
  </div>
</div>




---
## Overview

<!-- ![Seqera biotech stack](assets/seqera-biotech-stack.png){ .right .image} -->
<img src="assets/seqera-biotech-stack.png" alt="Seqera biotech stack" style="float: right; width: 50%; margin-left: 30px; margin-bottom: 20px;">

This guide provides a walkthrough of a standard Seqera Platform demonstration. The demonstration will describe how to add a pipeline to the Launchpad, launch a workflow with pipeline parameters, monitor a Run, and examine the run details in several different parts. The demonstration will also highlight key features such as the Pipeline Optimization, Data Explorer, and Compute Environment creation.

More specifically, this demonstration will focus on using the [nf-core/rnaseq](https://github.com/nf-core/rnaseq) pipeline as an example and executing the workflow on AWS Batch.

<div style="clear: both;"></div>

---

## Requirements

:octicons-checkbox-16: A [Seqera Platform Cloud](https://cloud.seqera.io/login) account

:octicons-checkbox-16: Access to a Workspace in Seqera Platform

:octicons-checkbox-16: :fontawesome-brands-aws: An [AWS Batch Compute Environment created in that Workspace](https://docs.seqera.io/platform/23.3.0/compute-envs/aws-batch)

:octicons-checkbox-16: The [nf-core/rnaseq](https://github.com/nf-core/rnaseq) pipeline repository

:octicons-checkbox-16: Samplesheet to create a Dataset on the Platform used to run minimal test RNAseq data (see [samplesheet_test.csv](./samplesheet_test.csv) file in this repository)

---

## Sections

[:material-check-circle:]() [Why use Seqera Platform?](./intro.md) <br/>
[:material-check-circle:]() [Overview of the Platform](./demo_overview.md) <br/>
[:material-check-circle:]() [Add a Pipeline to the Launchpad](./add_a_pipeline.md) <br/>
[:material-check-circle:]() [Add a Dataset to Seqera Platform](./add_a_dataset.md) <br/>
[:material-check-circle:]() [Launch a Pipeline](./launch_pipeline.md) <br/>
[:material-check-circle:]() [Monitoring your run](./monitor_run.md) <br/>
[:material-check-circle:]() [Monitoring views](./monitoring_views.md) <br/>
[:material-check-circle:]() [Examine run and task details](./run_details.md) <br/>
[:material-check-circle:]() [Resume a Pipeline](./resume_pipeline.md) <br/>
[:material-check-circle:]() [Data Explorer](./data_explorer.md) <br/>
[:material-check-circle:]() [Data Studios](./data_studios.md) <br/>
[:material-check-circle:]() [Optimize your Pipeline](./pipeline_optimization.md) <br/>
[:material-check-circle:]() [Automation on Seqera Platform](./automation.md) <br/>
[:material-check-circle:]() [Scaling Science on Seqera Platform](./summary.md) <br/>

