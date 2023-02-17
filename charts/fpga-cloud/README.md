# InAccel FPGA Cloud

Simplifying FPGA management in Harvester

## Installing the Chart

To install the chart with the release name `my-fpga-cloud`:

```console
$ helm repo add inaccel https://setup.inaccel.com/helm
$ helm install my-fpga-cloud inaccel/fpga-cloud
```

These commands deploy InAccel FPGA Cloud on the Harvester cluster in the default
configuration.

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `my-fpga-cloud` deployment:

```console
$ helm uninstall my-fpga-cloud
```

The command removes all the Harvester components associated with the chart and
deletes the release.

## Parameters

The following table lists the configurable parameters of the InAccel FPGA Cloud
chart and their default values.

| Parameter                 | Description                                   | Default                 |
| ------------------------- | --------------------------------------------- | ----------------------- |
| `cloudInit.debug`         | Argument --debug to the entrypoint.           | `false`                 |
| `cloudInit.image`         | Container image name.                         | `inaccel/cloud-init`    |
| `cloudInit.pullPolicy`    | Image pull policy.                            |                         |
| `cloudInit.resources`     | Compute resources required by this container. |                         |
| `cloudInit.tag`           | Release version.                              | `latest`                |
| `kubevirtHack.debug`      | Argument --debug to the entrypoint.           | `false`                 |
| `kubevirtHack.image`      | Container image name.                         | `inaccel/kubevirt-hack` |
| `kubevirtHack.pullPolicy` | Image pull policy.                            |                         |
| `kubevirtHack.resources`  | Compute resources required by this container. |                         |
| `kubevirtHack.tag`        | Release version.                              | `latest`                |
| `replicas`                | Number of desired pods.                       |                         |

Specify each parameter using the `--set key=value[,key=value]` argument to
`helm install`.

Alternatively, a YAML file that specifies the values for the parameters can be
provided while installing the chart. For example,

```console
$ helm install my-fpga-cloud -f values.yaml inaccel/fpga-cloud
```

> **Tip**: You can use the default `values.yaml`
