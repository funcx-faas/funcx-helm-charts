# Helm Chart Repository for FuncX

Access these charts with 
```
helm repo add funcx http://funcx.org/funcx-helm-charts 
helm repo update
```

## How To Deploy New Versions of Charts Here
These notes are for the endpoint chart, but the same rules apply for the 
stack chart.

1. Make sure the version numbers are updated in `Chart.yaml`
2. In the directory above the chart (funcX/helm) issue the command: `helm package funcx_endpoint`
3. Move the generated zip file to this repository
4. `cd` to the directory above this repository
5. Create a branch in this repo
6. Issue command `helm repo index funcx-helm-charts --url http://funcx.org/funcx-helm-charts`
7. Check in the new zip file, and the regenerated `index.yaml`
8. Create a PR, merge into master 
9. Github-Pages will take it from there!

