## Launchpad

Each Workspace has a Launchpad that allows users to easily create and share Nextflow pipelines that can be executed on any infrastructure supported by the Platform e.g. all public clouds and most HPC schedulers. A Launchpad pipeline consists of a pre-configured workflow repository, compute environment, and launch parameters.

Users can create their own pipelines, share them with others on the Launchpad, or tap into over a hundred community pipelines available on nf-core and other sources.


/// details | Advanced
        type: info   
    
    Adding a new pipeline is relatively simple and can be included as part of the demonstration. See the [Adding a pipeline](./006_adding_a_pipeline.md) section.
///

## Launch the nf-core/rnaseq pipeline

### 1. Go to Launchpad

Navigate to the Launchpad in the `seqeralabs/showcase` Workspace and select `Launch` next to the `nf-core-rnaseq` pipeline to open the launch form.


/// details | Click to show animation
    type: example

 ![Launching a Pipeline](assets/sp-cloud-launch-form.gif)
///


### 2. Nextflow parameter schema

On clicking the launch button, a parameters page will become visible to allow you to fine-tune the pipeline execution. This parameters form is rendered from a file called [`nextflow_schema.json`](https://github.com/nf-core/rnaseq/blob/master/nextflow_schema.json) which can be found in the root of the pipeline Git repository. By adding a simple JSON-based schema describing pipeline parameters, the `nextflow_schema.json` allows pipeline developers to easily adapt their in-house Nextflow pipelines to be executed via the interactive web interface available on the Seqera Platform.

Please refer to the ["Best Practices for Deploying Pipelines with the Seqera Platform"](https://seqera.io/blog/best-practices-for-deploying-pipelines-with-seqera-platform/) blog for further information on how to automatically build the parameter schema for any Nextflow pipeline using tooling maintained by the nf-core community. 

### 3. Parameter selection

The following Platform-specific options can be adjusted if required:

- `Workflow run name`:

    A unique identifier for the run, pre-filled with a random name. This can be customized.

- `Labels`:

    Assign new or existing labels to the run. For example, Project ID or genome version.

Each pipeline including nf-core/rnaseq will have it's own set of parameters that need to be provided in order to run it. The following parameters are mandatory:

- `input`:

    Most nf-core pipelines have standardized the usage of the `input` parameter to specify an input samplesheet that contains paths to any input files (e.g. FastQ files) as well as any additional metadata required to run the pipeline. The `input` parameter can take a path to a samplesheet in the S3 bucket selected through Data Explorer. Alternatively, the Seqera Platform has a Datasets feature that allows you to upload structured data like samplesheets for use with Nextflow pipelines.

    For the purposes of this demonstration, click on the "Browse" button next to the `input` parameter, and search and select a pre-loaded Dataset called "rnaseq_samples".

    /// details | Click to show animation
        type: example

    ![Input parameters](assets/sp-cloud-launch-parameters-input.gif)
    ///
    

    /// details | Advanced
        type: info    
        
    Users can upload their own samplesheets and make them available as a Dataset by uploading them in the 'Datasets' tab. For more information please refer to the [Add a Dataset](./007_adding_a_dataset.md) section.
    ///

- `outdir`:

    Most nf-core pipelines have standardized the usage of the `outdir` parameter to specify where the final results created by the pipeline are published. `outdir` must be different for each different pipeline run, otherwise, your results will be overwritten. Since we want to publish these files to S3, we must provide the path to the appropriate storage location.

    For the `outdir` parameter, specify an S3 directory path manually, or select Browse to specify a cloud storage directory using Data Explorer.


    /// details | Click to show animation
        type: example
    
    ![Output parameters](assets/sp-cloud-launch-parameters-outdir.gif)
    ///

Users can easily modify and specify other parameters to customize the pipeline execution through the parameters form. For example, in the 'Read trimming options' section of the parameters page, change the `trimmer` to select `fastp` in the dropdown menu, instead of `trimgalore`, and click the "Launch" button!

![Read trimming options](./assets/trimmer-settings.png)
