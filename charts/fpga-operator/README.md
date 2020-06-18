# InAccel FPGA Operator

Simplifying FPGA management in Kubernetes

## Installing the Chart

To install the chart with the release name `my-release`:

```console
$ helm repo add inaccel https://setup.inaccel.com/helm
$ helm install my-release inaccel/fpga-operator --set license=...
```

These commands deploy InAccel FPGA Operator on the Kubernetes cluster in the
default configuration.

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
$ helm uninstall my-release
```

The command removes all the Kubernetes components associated with the chart and
deletes the release.

## Parameters

The following table lists the configurable parameters of the InAccel FPGA
Operator chart and their default values.

| Parameter            | Default           |
| -------------------- |  ---------------- |
| `coral.image`        | `inaccel/coral`   |
| `coral.pullPolicy`   | `Always`          |
| `coral.resources`    |                   |
| `coral.tag`          | *APP VERSION*     |
| `license`            |                   |
| `monitor.image`      | `inaccel/monitor` |
| `monitor.port`       |                   |
| `monitor.pullPolicy` |                   |
| `monitor.resources`  |                   |
| `monitor.tag`        | `latest`          |

Specify each parameter using the `--set key=value[,key=value]` argument to
`helm install`.

Alternatively, a YAML file that specifies the values for the parameters can be
provided while installing the chart. For example,

```console
$ helm install my-release -f values.yaml inaccel/fpga-operator
```

> **Tip**: You can use the default [values.yaml](values.yaml)
