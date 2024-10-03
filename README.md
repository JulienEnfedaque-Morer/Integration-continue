Julien.EM Papis.C

#Description
1.Le fichier vagrantfile permet d'installer une machine virtuel avec Gitlab pré-installé.

#Prerequis
1.	Installer Vagrant : https://developer.hashicorp.com/vagrant/install et Virtual box (ne pas dépasser la version 7.0 de VB)

#Installation
1.	Créer un répertoire pour le projet puis aller dedans avec "cd D:\chemin\du\projet".
2.	Inserer le fichier vagrantfile dans le répertoire
3.	à partir d'un invite de commande Powershell, écrire la commande "vagrant up" qui va télécharger la VM puis la lancer automatiquement avec virtualbox/VMWare 
4.	écrire la commande "vagrant ssh" pour acceder à la VM par SSH
5.	Lancer le gitlab avec la commande "sudo gitlab-ctl start"
6.	Vérifier que le module gitlab container registry est installé et actif avec la commande : "sudo gitlab-ctl status" 
