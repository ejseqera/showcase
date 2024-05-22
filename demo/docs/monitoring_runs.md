There are several ways to monitor run executions in and across Workspaces in Seqera Platform.

## Runs tab
The Runs tab contains all previous runs in a given Workspace.

![Viewing Runs](assets/sp-cloud-view-all-runs.gif)

## All runs view

If you go to the user menu on the right side of the inteface, you will be able to access the **All runs** page. 

This page provides a comprehensive overview of the runs accessible to a user across the entire Seqera instance. The default view will be all organizations and workspaces you have access to. You can filter these by selecting the dropdown next to **View** or searching for a run. You can filter based on the following entries:

- `status`
- `label`
- `workflowId`
- `runName`
- `username`
- `projectName`
- `after: YYYY-MM-DD`
- `before: YYYY-MM-DD`
- `sessionId`
- `is:starred`

For example:

```
rnaseq username:johndoe status:succeeded after:2024-01-01
```

![All Runs view](assets/all_runs_view.gif)

## Dashboard view

To be able to see how many runs are currently submitted, running, or have failed, you can make use of the Dashboard view. 

Go to your user menu again, and click on 'Dashboard'. This will provide an overview of runs in your personal and organization workspaces. The default view will be all organizations and workspaces you have acces to. You can filter for these by selecting the dropdown next to **View** and filter by time, including a custom date range up to 12 months.

You can also export this data in CSV format by clicking the **Export data** button.

![Dashboard view](./assets/dashboard_view.gif)
