# preset

## Project Generator Commands

```bash
> kubebuilder init --domain x-helm.dev --skip-go-version-check
> kubebuilder edit --multigroup=true
> kubebuilder create api --group charts --version v1alpha1 --kind ChartPreset
> kubebuilder create api --group charts --version v1alpha1 --kind VendorChartPreset --namespaced=false
> kubebuilder create api --group charts --version v1alpha1 --kind ClusterChartPreset --namespaced=false
> kubebuilder create api --group store --version v1alpha1 --kind ChartRegistry --namespaced=false
```

## Test Examples

```bash
> k apply -f config/crd/bases/
customresourcedefinition.apiextensions.k8s.io/chartpresets.charts.x-helm.dev created
customresourcedefinition.apiextensions.k8s.io/clusterchartpresets.charts.x-helm.dev created
customresourcedefinition.apiextensions.k8s.io/vendorchartpresets.charts.x-helm.dev created
customresourcedefinition.apiextensions.k8s.io/chartregistries.store.x-helm.dev created

# Test charts are available in: https://github.com/kubepack/chartpreset-testdata

> k apply -f cd ../chartpreset-testdata/charts/hello/presets/
custerchartpreset.charts.x-helm.dev/ha-deployment created
custerchartpreset.charts.x-helm.dev/nodeport-service created
custerchartpreset.charts.x-helm.dev/unified created

> k get clusterpresets
NAME               AGE
ha-deployment      8s
nodeport-service   8s
unified            8s
```
