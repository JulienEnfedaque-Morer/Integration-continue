Julien.EM Papis.c

#Description
Le fichier vagrantfile permet d'installer une machine virtuel avec Gitlab pré-installé.

#Prerequis
1.	Installer Vagrant : https://developer.hashicorp.com/vagrant/install et Virtual box (ne pas dépasser la version 7.0 de VB)
2.	Créer un répertoire pour le projet puis aller dedans avec "cd D:\chemin\du\projet".

#Installation
1.	Inserer le fichier vagrantfile dans le répertoire
2.	à partir d'un invite de commande Powershell, écrire la commande "vagrant up" qui va télécharger la VM puis la lancer automatiquement avec virtualbox/VMWare 
3.	écrire la commande "vagrant ssh" pour acceder à la VM par SSH
4.	Lancer le gitlab avec la commande "sudo gitlab-ctl start"
5.	Vérifier que le module gitlab container registry est installé et actif avec la commande : "sudo gitlab-ctl status" 
