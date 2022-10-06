# iotkubeadmin
1. Install Minikube in GCP VM -> https://www.linuxtechi.com/how-to-install-minikube-on-ubuntu/
2. Install Docker -> https://www.linuxtechi.com/install-use-docker-on-ubuntu/
3. Install ArgoCD - > https://argo-cd.readthedocs.io/en/stable/getting_started/
    kubectl create namespace argocd
    for UI -> kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
    For CLI -> kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/core-install.yaml
    
