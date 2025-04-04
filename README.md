# Fix Failed Deployments Fast with Helm Rollback

This repository contains all resources demonstrated in the "Fix Failed Deployments Fast with Helm Rollback" tutorial from the DevOps Tips and Tricks YouTube channel.

## 📺 Video Tutorial

[![Helmm Rollback Tutorial](https://img.youtube.com/vi/tx9MDV6in9g/0.jpg)](https://youtu.be/tx9MDV6in9g?si=-l2D8m1Rp-ePS_Y1) 

## 📋 Overview
Learn how to recover from failed Kubernetes deployments quickly and effectively using Helm's powerful rollback capabilities. This tutorial covers:

Initial deployment with Helm
Upgrading Helm releases
Identifying and troubleshooting failed deployments
Executing rollbacks to restore stability
Advanced rollback options and best practices

## 🛠️ Prerequisites

Kubernetes cluster (local or remote)
Helm v3 installed
Basic understanding of Helm charts and Kubernetes

## 🚀 Quick Start

Clone this repository:
```bash
git clone https://github.com/your-username/helm-rollback-tutorial.git
cd helm-rollback-tutorial
```
Create a namespace for the demo:
```bash
kubectl create namespace helm-rollback-demo
```
Deploy the initial application:
```bash
helm install my-nginx bitnami/nginx --version 13.1.0 -n helm-rollback-demo
```
📝 Key Commands
View Release History
```bash
helm history my-nginx -n helm-rollback-demo
```
Perform a Rollback
```bash
helm rollback my-nginx 2 -n helm-rollback-demo
```
Rollback with Options
# Rollback with timeout
```bash
helm rollback my-nginx 2 --timeout 2m -n helm-rollback-demo
```

# Dry run (preview only)
```bash
helm rollback my-nginx 1 --dry-run -n helm-rollback-demo
```
# Force rollback
```bash
helm rollback my-nginx 2 --force -n helm-rollback-demo
```

## 🔍 Key Takeaways

Helm maintains a complete release history, enabling easy rollbacks
Each rollback creates a new revision in the history
Use helm history to view available revisions
The --dry-run flag lets you preview rollback effects
Helm rollback is your safety net for Kubernetes deployments

## 📚 Additional Resources

Official Helm Documentation
Kubernetes Documentation
Bitnami Helm Charts

## 🔗 Connect

Subscribe to DevOps Tips and Tricks: https://www.youtube.com/@devops-tips-and-tricks

Follow on X: https://x.com/devopstricks

