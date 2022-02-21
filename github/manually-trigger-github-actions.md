# Manually Trigger GitHub Actions

I was recently using GitHub Actions for a few cron tasks and was puzzled
why the "Run Workflow" button wasn't available in the GitHub web interface.

This button allows for manually triggering the Action.

As it turns out, an Action must be configured to respond to the [`workflow_dispatch`](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#workflow_dispatch) event for this option to be available.

```yaml
on: workflow_dispatch
```

This configuration also enables manually triggering the Action from the GitHub CLI or API.