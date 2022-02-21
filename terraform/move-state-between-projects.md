# Move State Between Projects

The [`terraform state mv`](https://www.terraform.io/cli/commands/state/mv) command allows for moving an existing remote resource
to be specified by a different instance resource address in Terraform. Said
another way, `state mv` can also move a resource's state _between_ Terraform
projects without tearing down or rebuilding the resource itself.

The following command moves the `packet_device.worker` resource into a module.

```shell
terraform state mv packet_device.worker module.worker.packet_device.worker
```

The command also accepts `-state` and `-state-out` options, which support moving
state into or out of a provided local file. These options can be especiall useful
if you can't specify a module to the move the state into or out of directly because
the Terraform projects cannot access one another.