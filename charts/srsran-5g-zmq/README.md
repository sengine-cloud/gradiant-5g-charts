# srsran-5g-zmq

![Version: 1.0.1](https://img.shields.io/badge/Version-1.0.1-informational?style=flat-square) ![AppVersion: 23.10.1](https://img.shields.io/badge/AppVersion-23.10.1-informational?style=flat-square)

Helm chart to deploy srsRAN 5G gNB on Kubernetes.

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| avrodriguez | <avrodriguez@gradiant.org> |  |

## Source Code

* <https://github.com/sengine-cloud/gradiant-5g-charts>
* <https://github.com/srsran/srsRAN_Project>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | common | 1.x.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| args | list | `[]` |  |
| command | list | `[]` |  |
| commonAnnotations | object | `{}` |  |
| commonLabels | object | `{}` |  |
| config.amf.bind_interface | string | `"eth0"` |  |
| config.amf.hostname | string | `"open5gs-amf-ngap"` |  |
| config.cell_cfg.band | int | `3` |  |
| config.cell_cfg.channel_bandwidth_MHz | int | `20` |  |
| config.cell_cfg.common_scs | int | `15` |  |
| config.cell_cfg.dl_arfcn | int | `368500` |  |
| config.cell_cfg.plmn | string | `"99970"` |  |
| config.cell_cfg.tac | int | `1` |  |
| config.ru_sdr.device_args | string | `"tx_port=tcp://127.0.0.1:2000,rx_port=tcp://127.0.0.1:2001,id=gnb,base_srate=23.04e6"` |  |
| config.ru_sdr.device_driver | string | `"zmq"` |  |
| config.ru_sdr.rx_gain | int | `75` |  |
| config.ru_sdr.srate | float | `23.04` |  |
| config.ru_sdr.tx_gain | int | `75` |  |
| config.slicing[0].sd | int | `1118481` |  |
| config.slicing[0].sst | int | `1` |  |
| containerPorts.gtpu | int | `2152` |  |
| containerSecurityContext.capabilities.add[0] | string | `"NET_ADMIN"` |  |
| containerSecurityContext.enabled | bool | `true` |  |
| containerSecurityContext.privileged | bool | `true` |  |
| customLivenessProbe | object | `{}` |  |
| customReadinessProbe | object | `{}` |  |
| customStartupProbe | object | `{}` |  |
| extraDeploy | list | `[]` |  |
| extraEnvVars | list | `[]` |  |
| extraEnvVarsCM | string | `""` |  |
| extraEnvVarsSecret | string | `""` |  |
| extraVolumeMounts | list | `[]` |  |
| extraVolumes | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| global.imageRegistry | string | `""` |  |
| global.storageClass | string | `""` |  |
| hostAliases | list | `[]` |  |
| image.srsran.debug | bool | `false` |  |
| image.srsran.digest | string | `""` |  |
| image.srsran.pullPolicy | string | `"IfNotPresent"` |  |
| image.srsran.registry | string | `"docker.io"` |  |
| image.srsran.repository | string | `"gradiant/srsran-5g"` |  |
| image.srsran.tag | string | `"23_10_1"` |  |
| initContainers | list | `[]` |  |
| kubeVersion | string | `""` |  |
| lifecycleHooks | object | `{}` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `5` |  |
| livenessProbe.initialDelaySeconds | int | `600` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `5` |  |
| nameOverride | string | `""` |  |
| namespaceOverride | string | `""` |  |
| nodeAffinityPreset.key | string | `""` |  |
| nodeAffinityPreset.type | string | `""` |  |
| nodeAffinityPreset.values | list | `[]` |  |
| nodeSelector | object | `{}` |  |
| podAffinityPreset | string | `""` |  |
| podAnnotations | object | `{}` |  |
| podAntiAffinityPreset | string | `"soft"` |  |
| podLabels | object | `{}` |  |
| podSecurityContext.enabled | bool | `false` |  |
| podSecurityContext.fsGroup | int | `1001` |  |
| priorityClassName | string | `""` |  |
| readinessProbe.enabled | bool | `true` |  |
| readinessProbe.failureThreshold | int | `5` |  |
| readinessProbe.initialDelaySeconds | int | `30` |  |
| readinessProbe.periodSeconds | int | `5` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `1` |  |
| replicaCount | int | `1` |  |
| resources.limits | object | `{}` |  |
| resources.requests | object | `{}` |  |
| schedulerName | string | `""` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automountServiceAccountToken | bool | `true` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.name | string | `""` |  |
| services.gtpu.annotations | object | `{}` |  |
| services.gtpu.clusterIP | string | `""` |  |
| services.gtpu.externalTrafficPolicy | string | `"Cluster"` |  |
| services.gtpu.extraPorts | list | `[]` |  |
| services.gtpu.loadBalancerIP | string | `""` |  |
| services.gtpu.loadBalancerSourceRanges | list | `[]` |  |
| services.gtpu.nodePorts.gtpu | string | `""` |  |
| services.gtpu.ports.gtpu | int | `2152` |  |
| services.gtpu.sessionAffinity | string | `"None"` |  |
| services.gtpu.sessionAffinityConfig | object | `{}` |  |
| services.gtpu.type | string | `"ClusterIP"` |  |
| sessionAffinity | string | `"None"` |  |
| sidecars | list | `[]` |  |
| startupProbe.enabled | bool | `false` |  |
| startupProbe.failureThreshold | int | `5` |  |
| startupProbe.initialDelaySeconds | int | `600` |  |
| startupProbe.path | string | `"/"` |  |
| startupProbe.periodSeconds | int | `10` |  |
| startupProbe.successThreshold | int | `1` |  |
| startupProbe.timeoutSeconds | int | `5` |  |
| topologySpreadConstraints | list | `[]` |  |
| ue.config.imei | string | `"353490069873319"` |  |
| ue.config.imsi | string | `"999700000000001"` |  |
| ue.config.k | string | `"465B5CE8B199B49FAA5F0A2EE238A6BC"` |  |
| ue.config.opc | string | `"E8ED289DEBA952E4283B54E88E6183CA"` |  |
| ue.config.resources | object | `{}` |  |
| ue.image.digest | string | `""` |  |
| ue.image.pullPolicy | string | `"IfNotPresent"` |  |
| ue.image.registry | string | `"docker.io"` |  |
| ue.image.repository | string | `"gradiant/srsran-4g"` |  |
| ue.image.tag | string | `"23_11"` |  |
| updateStrategy.type | string | `"RollingUpdate"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
