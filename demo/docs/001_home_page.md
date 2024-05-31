# Seqera Platform: Demonstration Walkthrough

---

## Overview

<!-- ![Seqera biotech stack](assets/seqera-biotech-stack.png){ .right .image} -->
<!-- <img src="assets/seqera-biotech-stack.png" alt="Seqera biotech stack" style="float: right; width: 50%; margin-left: 30px; margin-bottom: 20px;"> -->

This guide provides a walkthrough of a standard Seqera Platform demonstration. The demonstration will describe how to add and run a pipeline in the Platform, examine the run details, as well as highlight key features such as pipeline optimization, Data Explorer and Data Studios.

The demonstration will focus on using the [nf-core/rnaseq](https://github.com/nf-core/rnaseq) pipeline as an example to execute a Nextflow pipeline on Seqera Cloud via the AWS Batch cloud executor.

<div style="clear: both;"></div>

---

## Requirements

<div style="display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 20px;">
  <div style="flex-grow: 1;">
    <p>:octicons-checkbox-16: [Seqera Cloud](https://cloud.seqera.io/login) account</p>
    <p>:octicons-checkbox-16: Access to a Workspace in Seqera Cloud</p>
    <p>:octicons-checkbox-16: :fontawesome-brands-aws: Access to an [AWS Batch Compute Environment](https://docs.seqera.io/platform/23.4.0/compute-envs/aws-batch) created in that Workspace</p>
    <p>:octicons-checkbox-16: Publicly available [nf-core/rnaseq](https://github.com/nf-core/rnaseq) pipeline repository</p>
    <p>:octicons-checkbox-16: [Input samplesheet](./samplesheet_test.csv) to run the nf-core/rnaseq pipeline on Seqera Cloud</p>
  </div>
  <div style="margin-left: 20px;">
    <a href="https://cloud.seqera.io/login" class="md-button" style="display: block; margin-bottom: 10px;">
      <i class="fas fa-user"></i> Login to Seqera Platform
    </a>
    <a href="https://seqera.io" class="md-button" style="display: block;">
      Visit Seqera Main Site
    </a>
  </div>
</div>
