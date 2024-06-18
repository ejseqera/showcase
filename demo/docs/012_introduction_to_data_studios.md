After running a pipeline, you may want to perform tertiary analysis using platforms like Jupyter Notebook or RStudio. Setting up the infrastructure for these platforms, including accessing pipeline data, results, and necessary bioinformatics packages, can be complex and time-consuming.

Data Studios streamlines this process for Seqera Platform users by allowing them to add interactive analysis environments based on templates, similar to how they add and share Pipelines and Datasets.

The Seqera Platform manages all the details, enabling users to easily select their preferred interactive tool and analyze their data within the platform.

## Data Studio Setup

### Create a Data Studio

#### 1. Add a Data Studio {#hidden-heading}

To create a Data Studio, click on the 'Add data studio' button and select from any one of the three currently available templates.


/// details | Click to show animation
    type: example

![Add a data studio](assets/create-data-studio.gif)
///

#### 2. Select a compute environment {#hidden-heading}

Currently, only AWS Batch is supported.

#### 3. Mount data using Data Explorer {#hidden-heading}

Select data to mount into your data studios environment using the Fusion file system in Data Explorer. This data will be available at `/workspace/data/<dataset>`.

For example, to take a look at the results of your nf-core/rnaseq pipeline run, you can mount the value of the `outdir` parameter specified in the [earlier step when launching the pipeline](./005_launching_pipelines.md).


/// details | Click to show animation
    type: example

![Mount data into studio](assets/mount-data-into-studio.gif)
///

#### 4. Resources for environment {#hidden-heading}

Enter a CPU or memory allocation for your data studios environment (optional). The default is 2 CPUs and 8192 MB of memory.

Then, click Add!

The data studio environment will be available in the Data Studios landing page with the status 'stopped'. Click on the three dots and **Start** to begin running the studio.


/// details | Click to show animation
    type: example

![Start a studio](assets/start-studio.gif)
///


![Connect to a studio](assets/connect-to-studio.png){ .right .image}

### Connect to a Data Studio

To connect to a running data studio session, select the three dots next to the status message and choose **Connect**. A new browser tab will open, displaying the status of the data studio session. Select **Connect**.
<br>
<div style="clear: both;"></div>

### Collaborate in Data Studio

Collaborators can also join a data studios session in your workspace. For example, to share the results of the nf-core/rnaseq pipeline, you can share a link by selecting the three dots next to the status message for the data studio you want to share, then select **Copy data studio URL**. Using this link other authenticated users with the "Connect" role at minimum, can access the session directly.
<div style="clear: both;"></div>

![Stop a studio session](assets/stop-a-studio.png){ .right .image}
### Stop a Data Studio

To stop a running session, click on the three dots next to the status and select **Stop**. Any unsaved analyses or results will be lost.<br>
<div style="clear: both;"></div>

<br>



/// details | Advanced
    type: info    

For a more detailed use-case of performing tertiary analysis with the results of the nf-core/rnaseq pipeline in a Jupyter notebook, take a look at the [Analyse RNAseq data using Jupyter Notebooks](./013_data_studio_jupyter_example.md) section.
///
