# ☸️ ArgoCD GitOps Lab

This repository contains the Kubernetes manifests and GitOps configuration for automating deployments using **ArgoCD**. 🚀

## 🏗️ Project Architecture
This project follows the **GitOps** methodology, where the state of the Kubernetes cluster is managed declaratively through this Git repository. 🛡️

* **Infrastructure:** Kubernetes (Local/Cloud) ☁️
* **Continuous Delivery:** ArgoCD 🔄
* **Manifests:** Standard Kubernetes YAML (Deployments, Services) 📄

## 📂 Repository Structure
* `./`: Contains the core Kubernetes manifest files. 📁
* `my-app-deployment.yaml`: Defines the application pods and replicas. 🏗️
* `my-app-service.yaml`: Defines the networking and access points. 🌐

## 🚀 Getting Started

### 1 Pre-requisites
* A running Kubernetes cluster. ☸️
* ArgoCD installed in the `argocd` namespace. 🛠️
* ArgoCD CLI configured on your local machine (**Your pc**) 💻

### 2️ Creating the Application in ArgoCD
Run the following command in your terminal to link this repository to your cluster:

```bash
argocd app create my-app \
  --repo [https://github.com/Avishka-2002/argocd-gitops-lab.git](https://github.com/Avishka-2002/argocd-gitops-lab.git) \
  --path ./ \
  --dest-server [https://kubernetes.default.svc](https://kubernetes.default.svc) \
  --dest-namespace default
