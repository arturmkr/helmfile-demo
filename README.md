Commands

Initialize and create the chart:
```
helm create nginx-pod-chart
```


Deploy configurations with Helmfile:
```
helmfile -e dev apply
helmfile -e prod apply
```