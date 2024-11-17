### Initialize and create the chart:
```
curl -Lo  helmfile_0.169.1_linux_amd64.tar.gz https://github.com/helmfile/helmfile/releases/download/v0.169.1/helmfile_0.169.1_linux_amd64.tar.gz
tar -xvzf helmfile_0.169.1_linux_amd64.tar.gz
chmod +x helmfile
sudo mv helmfile /usr/local/bin/
helmfile --version
```

### Install helm diff plugin:
```
helm plugin install https://github.com/databus23/helm-diff
helm plugin list
```

### Initialize and create the chart:
```
helm create nginx-pod-chart
```

### Deploy configurations with Helmfile:
```
helmfile -e dev apply
helmfile -e prod apply
```

### Uninstall (destroy) Releases with Helmfile:
```
helmfile -e dev destroy
helmfile -e prod destroy
```
