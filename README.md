# iotkubeadmin
1. Install Minikube in GCP VM -> https://www.linuxtechi.com/how-to-install-minikube-on-ubuntu/
2. Install Docker -> https://www.linuxtechi.com/install-use-docker-on-ubuntu/
3. Install ArgoCD - > https://argo-cd.readthedocs.io/en/stable/getting_started/
    kubectl create namespace argocd
    for UI -> kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
    For CLI -> kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/core-install.yaml
    Ingress -> kubectl port-forward svc/argocd-server -n argocd 8080:443
    Password for Argoocd login -> kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
    export ARGOCD_OPTS='--port-forward-namespace argocd'
    Login -> argocd login localhost:8080 --grpc-web --insecure
    After GCP VM restart Minikube service needs to be restarted-> 
            minikube start
            kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
            kubectl port-forward svc/argocd-server -n argocd 8080:443
            
    
