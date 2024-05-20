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
<!-- <img src="assets/seqera-biotech-stack.png" alt="Seqera biotech stack" style="float: right; width: 50%; margin-left: 30px; margin-bottom: 20px;"> -->

This guide provides a walkthrough of a standard Seqera Platform demonstration. The demonstration will describe how to add and run a pipeline in the Platform, examine the run details, as well as highlight key features such as pipeline optimization, Data Explorer and Data Studios.

The demonstration will focus on using the [nf-core/rnaseq](https://github.com/nf-core/rnaseq) pipeline as an example to execute a Nextflow pipeline on Seqera Cloud via the AWS Batch cloud executor.

<div style="clear: both;"></div>

---

## Requirements

:octicons-checkbox-16: [Seqera Cloud](https://cloud.seqera.io/login) account

:octicons-checkbox-16: Access to a Workspace in Seqera Cloud

:octicons-checkbox-16: :fontawesome-brands-aws: Access to an [AWS Batch Compute Environment](https://docs.seqera.io/platform/23.4.0/compute-envs/aws-batch) created in that Workspace

:octicons-checkbox-16: Publicly available [nf-core/rnaseq](https://github.com/nf-core/rnaseq) pipeline repository

:octicons-checkbox-16: [Input samplesheet](./samplesheet_test.csv) to run the nf-core/rnaseq pipeline on Seqera Cloud

---

## Walkthrough

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

