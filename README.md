# Jenkins Slaves on Demand in Kubernetes Cluster

[![](https://img.shields.io/github/license/jnonino/jenkins-kubernetes-slaves)](https://github.com/jnonino/jenkins-kubernetes-slaves)
[![](https://img.shields.io/github/issues/jnonino/jenkins-kubernetes-slaves)](https://github.com/jnonino/jenkins-kubernetes-slaves)
[![](https://img.shields.io/github/issues-closed/jnonino/jenkins-kubernetes-slaves)](https://github.com/jnonino/jenkins-kubernetes-slaves)
[![](https://img.shields.io/github/languages/code-size/jnonino/jenkins-kubernetes-slaves)](https://github.com/jnonino/jenkins-kubernetes-slaves)
[![](https://img.shields.io/github/repo-size/jnonino/jenkins-kubernetes-slaves)](https://github.com/jnonino/jenkins-kubernetes-slaves)

This repository is a PoC that shows how to use slaves on demand on Jenkins based on Docker in Kubernetes Cluster.

## How to use it

1- Make sure you have a Jenkins deployed in a Kubernetes Cluster and the Cloud configuration for use the Kubernetes cluster.  
2- Please install Jenkins Pipeline plugin.  
3- Create a Multibranch Pipeline job and point to this repository.  
