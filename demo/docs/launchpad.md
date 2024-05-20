# Launchpad
The Launchpad allows Users publish and access pipelines pre-configured with compute environments, credentials, to start running Nextflow workflows immediately. A pipeline consists of a pre-configured workflow repository, compute environment, and launch parameters.

Users can create their own pipelines, share them with others on the Launchpad, or tap into the hundreds of production-proven pipelines from nf-core and other sources to become productive immediately.

!!! Advanced

    Adding a new pipeline is also simple. Users name their pipeline, select a compute environment, and point to the Git repository that houses the pipeline code. 
    
    After supplying a working directory for scratch data and setting up optional pipeline parameters, the pipeline is ready for use by anyone with access to the workspace. 

    See further instructions in [Add a pipeline](./add_a_pipeline.md).

# Launch the nf-core/rnaseq pipeline

## 1. Go to Launchpad

Navigate to the Launchpad to begin executing the nf-core/rnaseq pipeline.

Select 'Launch' next to the pipeline of your choice to open the pipeline launch form.

![Launching a Pipeline](assets/sp-cloud-launch-form.gif)

### Nextflow Schema

Seqera Cloud looks for a [nextflow_schema.json](https://github.com/nf-core/rnaseq/blob/master/nextflow_schema.json) file in the root of the pipeline repository, to create a pipeline parameters form.

Pipeline developers can easily adapt in-house pipelines to Seqera's interactive web interface by adding a simple JSON-based schema describing workflow parameters.

Schemas can be built using an automated schema build tool maintained by the nf-core community. See more info in [this blog post](https://seqera.io/blog/best-practices-for-deploying-pipelines-with-seqera-platform/) on getting Nextflow pipelines ready for Seqera Platform.

## 2. Overview of the Launch form

Pipelines typically contain at least these three parameters:

**1. Workflow run name:** A unique identifier for the run, pre-filled with a random name. This can be customized.

**2. Labels:** Assign new or existing labels to the run.

**3. Input/output options:** Specify paths to pipeline input datasets, output directories, and other pipeline-specific I/O options. 

### 4. Specify an input
Inputs can be specified through a path, a Dataset, or a location of a file in the Cloud using the Data Explorer.

For the 'input' parameter, click on the text box and click on dataset titled 'rnaseq_samples'. This dataset provides a samplesheet as input to the pipeline, with information on sample names and locations to the raw reads.

!!! Advanced
    Users can upload their own samplesheets and make them available as a Dataset by uploading a CSV/TSV file in the 'Datasets' tab. 

    For more information on how to create a Dataset, see the [Add a Dataset](./add_a_dataset.md) section.

<!-- # TODO update this gif  -->
![Input parameters](assets/sp-cloud-launch-parameters-input.gif)

### 5. Specify an output directory
Many nf-core pipelines use the `outdir` parameter convention for specifying where the results should be saved. 

For the 'outdir' parameter, specify an S3 directory path manually, or select Browse to specify a cloud storage directory using Data Explorer.

![Output parameters](assets/sp-cloud-launch-parameters-outdir.gif)


### 6. Change trimming options
Users can easily modify and specify parameters for analysis through the parameters form.

For example, in the 'Read trimming options' section of the parameters, change the 'trimmer' to select 'fastp' in the dropdown menu, instead of 'trimgalore'.

![Read trimming options](./assets/trimmer-settings.png)

The remaining fields of the pipeline parameters form will vary for each pipeline, dependent on the parameters specified in the pipeline schema. When you have filled the necessary launch form details, select 'Launch'.
