# Optimize the Pipeline

Seqera's pipeline optimization feature uses resource usage information from previous runs to minimize the resources used in your pipeline runs.

Optimization is available for pipelines once 1 successful run has been completed. This will be indicated by the grey-lightbulb icon turning into a black-hashed lightbulb that will allow you to view the optimized profile. 

This profile consists of Nextflow configuration settings for each process and each resource directive (where applicable): cpus, memory, and time. The optimized setting for a given process and resource directive is based on the maximum use of that resource across all tasks in that process.

Once optimization is selected, any subsequent runs of that pipeline on the Launchpad will inherit the optimized configuration profile, indicated by the black lightbulb icon with a checkmark. 

> **NOTE:** Optimizated profiles are generated off of one run at a time, defaulting to the most recent runs, and _not_ an aggregation of previous runs.


Navigate back to the Launchpad, click on the nf-core/rnaseq Pipeline added, and click on the 'Lightbulb' icon to view the optimized profile. You can configure which settings the optimization applies to and add a retry strategy.

![Optimized configuration](assets/optimize-configuration.gif)

You can verify the optimized configuration of a given run by inspecting the resource usage plots for that run and these fields in the run's task table:

| Description  | Key                    |
| ------------ | ---------------------- |
| CPU usage    | `pcpu`                 |
| Memory usage | `peakRss`              |
| Runtime      | `start` and `complete` |
