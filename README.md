# CronJob

```yaml
apiVersion: argoproj.io/v1alpha1
kind: Application 
metadata: 
  name: cronjob 
spec:
  destination: 
    namespace: '' 
    server: https://kubernetes.default.svc 
  source: 
    path: . 
    repoURL: https://github.com/KAnggara/CronJob.git
    targetRevision: HEAD 
  sources: [] 
  project: cronjob 
  syncPolicy: 
    automated: 
      prune: true 
      selfHeal: true 
      enabled: true 
    syncOptions: 
      - CreateNamespace=true
```
