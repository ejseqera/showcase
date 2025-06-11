## Seqera Compute

Seqera Compute allows you to run pipelines and Studios in AWS without setting up infrastructure yourself. Seqera Compute automatically will provision and manage resources for you in the cloud. Using prepaid credits, you can start running analysis in the cloud within minutes.

## Create a Compute Environment

### 1. Create a new Compute Environment

In a workspace with Seqera Compute enabled, select Compute environments > Add compute environment.

#### Provide a name
Enter a descriptive name for this environment, such as `seqera_compute_1` (eu-west-1).

#### Select a Platform 
Under Platform, select "Seqera Compute".

#### Select a region
Select a target execution Region.

Seqera Compute is available in the following AWS regions:

**United States:**

- us-east-1 (Northern Virginia, USA)
- us-west-2 (Oregon, USA)
- us-east-2 (Ohio, USA)
- us-west-1 (Northern California, USA)

**Europe:**

- eu-west-1 (Ireland)
- eu-west-2 (London, UK)
- eu-central-1 (Frankfurt, Germany)
- eu-west-3 (Paris, France)

**APAC:**

- ap-southeast-1 (Singapore)

### 2. (Optional) Advanced options
Configure any advanced options, as needed.

#### 1. Work directory
Enter a relative Pipeline work directory path to be appended to the S3 storage bucket Seqera creates for this compute environment.

#### 2. Pre-run or post-run script
Enter pre- or post-run Bash scripts that execute before or after the Nextflow pipeline execution in your environment.

#### 3. Nextflow config
Enter Global Nextflow configuration settings for all pipeline runs launched with this environment. Values defined here are pre-filled in the Nextflow config file field in the pipeline launch form. These values can be overridden at pipeline launch.

#### 4. Environment variables
Specify custom Environment variables for the Head job and/or Compute jobs.

### 3. Add compute environment
Select Add to complete and you can now start running analysis in the cloud!


## Summary

You've successfully created a Seqera Compute environment that will:
- Automatically provision AWS infrastructure for your pipelines
- Manage resources and scaling based on your workload needs
- Provide cost-effective analysis using prepaid credits

## Additional resources
- [Managing your Seqera Compute credits](https://docs.seqera.io/platform-cloud/compute-envs/seqera-compute#manage-seqera-compute-credits)

