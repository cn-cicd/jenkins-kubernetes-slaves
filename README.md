# Jenkins Slaves on Demand in Kubernetes Cluster

[![](https://img.shields.io/github/license/cn-cicd/jenkins-kubernetes-slaves)](https://github.com/cn-cicd/jenkins-kubernetes-slaves)
[![](https://img.shields.io/github/issues/cn-cicd/jenkins-kubernetes-slaves)](https://github.com/cn-cicd/jenkins-kubernetes-slaves)
[![](https://img.shields.io/github/issues-closed/cn-cicd/jenkins-kubernetes-slaves)](https://github.com/cn-cicd/jenkins-kubernetes-slaves)
[![](https://img.shields.io/github/languages/code-size/cn-cicd/jenkins-kubernetes-slaves)](https://github.com/cn-cicd/jenkins-kubernetes-slaves)
[![](https://img.shields.io/github/repo-size/cn-cicd/jenkins-kubernetes-slaves)](https://github.com/cn-cicd/jenkins-kubernetes-slaves)

This repository is a PoC that shows how to use slaves on demand on Jenkins based on Docker in Kubernetes Cluster.

## How to use it

1- Make sure you have a Jenkins deployed in a Kubernetes Cluster and the Cloud configuration for use the Kubernetes cluster.  
2- Please install Jenkins Pipeline plugin.  
3- Create a Multibranch Pipeline job and point to this repository.  
