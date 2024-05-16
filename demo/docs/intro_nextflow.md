### Introduction to Nextflow

[Nextflow](https://www.nextflow.io/) is a workflow system for creating scalable, portable, and reproducible workflows.

Nextflow is both a workflow language and an execution runtime that supports a wide range of execution platforms, including popular traditional grid scheduling systems such as Slurm and IBM LSF, and cloud services such as AWS Batch, Google Cloud Batch, Azure Batch and Kubernetes.

#### Running a Nextflow pipeline

Nextflow provides a simple command line interface for managing and executing pipelines.

Let's take a look at how to run a basic, Nextflow pipeline using a simple [Hello World script](https://github.com/nextflow-io/hello).

1. [Install Nextflow](https://www.nextflow.io/docs/latest/install.html):

    ```bash
    curl -s https://get.nextflow.io | bash
    ```

2. You can then run the following command to run the Hello World pipeline:

    ```bash
    nextflow run https://github.com/nextflow-io/hello
    ```

#### Monitoring and finding logs

When you run a Nextflow pipeline via the CLI with `nextflow run`, it generates logs that can be used to monitor the execution of the pipeline. The logs are printed to the console, and detailed execution trace can be found in the work directory created by Nextflow. Each execution generates its own directory under work, where logs and output files are stored.

- **Execution Log**: The main log file (`nextflow.log`) is created in the directory where Nextflow is run. This file captures detailed information about the pipeline execution, including system errors and warnings.
- **Command Log**: Within the work directory, each process execution generates a `.command.log` file, which contains the standard output and error streams of the executed command.

#### Limitations of the Nextflow CLI

Monitoring and launching via CLI, though direct, poses challenges, especially with complex or large-scale pipelines that are not as simple as just running Hello World:

- **Scalability**: As the number of tasks increases, manually checking individual log files becomes impractical.
- **Real-Time Tracking**: The CLI does not offer an easy way to visualize real-time progress across multiple parallel tasks.
- **Aggregation**: Collecting and interpreting logs from various processes requires additional tools or scripts, complicating the workflow management.
- **Flexibility**: Switching between environments (i.e. your local computer to HPC, or cloud) requires the setup of access in the form of account keys and credentials to the environment on your CLI, followed by using the appropriate Nextflow configuration settings.