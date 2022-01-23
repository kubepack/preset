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
