Setup a Minikube environment in a windows 10 home laptop
========================================================

Steps
======
    1) Install WSL-2 from the powershell
    2) Install docker desktop for windows 
    3) Install chocolatey (Windows package manager) from https://chocolatey.org/ 
    4) Install minikube using windows powershell in administrative mode using chocolatey 
       using the command "choco install minikube -y"
    5) Then start minikube using the command "minikube start"
       one can also pass various command line parameters to minikube like below
       
       "   minikube start --addons=dashboard --addons=metrics-server --addons="ingress" --addons="ingress-dns"   "
       
       
