# argocd-generator
This action generates an ArgoCD application YAML file using the ArgoCD CLI.

```yaml
test: 
  runs-on: ubuntu-latest
  steps:
    - uses: actions/checkout@v4
    - name: Generate ArgoCD Application
      uses: my-org/my-repo/.github/actions/generate-argocd-application@main
      with:
        appName: 'my-app'
        repoUrl: 'https://github.com/my-org/my-repo.git'
        manifestsPath: './my/manifests'
        namespace: 'default'
        syncPolicy: 'automated'
        outputPath: '.'
```