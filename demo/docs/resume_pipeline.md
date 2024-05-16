# Resuming a Run

Seqera Platform enables you to use Nextflow's resume functionality to resume a workflow run with the same parameters, using the cached results of previously completed tasks and only executing failed and pending tasks.

## 1. Resume

![Resuming a run](assets/sp-cloud-resume-a-run.gif)

To resume a failed or cancelled run:

- Click on the three dots next to the Run
- Select 'Resume' from the options menu
- Edit the parameters before launch, if desired
- If you have the appropriate permissions, you may edit the compute environment if desired

**Notes:**

- Unlike a relaunch, you cannot edit the Pipeline to launch or the work directory during a run resume.
- When changing the compute environment, the new compute environment must have a work directory that matches the root path of the original pipeline work directory. For example, if the original pipeline work directory is `s3://foo/work/12345`, the new compute environment must have access to `s3://foo/work`.

## 2. Monitor progress

Check the Runs page for the newly submitted run and monitor progress. In the Run details page, the status of tasks will be updated in real time as they progress from 'Submitted' to 'Running' to 'Succeeded' or 'Failed'. If you are resuming a run that had tasks that were completed successfully, you will see a number of tasks shown as 'Cached'.

![Cached processes](assets/sp-cloud-cached-processes.gif)
