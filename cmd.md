kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 --decode && echo

kubectl port-forward svc/argocd-server 31363:443 -n argocd  