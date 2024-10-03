Julien.EM Papis.C

#Description
1.Le fichier vagrantfile permet d'installer une machine virtuel avec Gitlab pré-installé.

#Prerequis
1.	Installer Vagrant : https://developer.hashicorp.com/vagrant/install et Virtual box (ne pas dépasser la version 7.0 de VB)

#Paramètre du Vagrantfile
1.Pour rediriger le port HTTP : config.vm.network "forwarded_port", guest: 80, host: 8080
2.Pour rediriger le port HTTPS :  config.vm.network "forwarded_port", guest: 443, host: 8443
3.Pour demander l'installation d'une VM ubuntu : config.vm.box = "generic/ubuntu2204"
4.Pour la pré-installation du gitlab :
  config.vm.provision "shell", inline: <<-SHELL
      sudo apt update
      sudo apt install -y curl openssh-server ca-certificates tzdata perl
      curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | sudo bash
      sudo EXTERNAL_URL="https://gitlab.example.com" apt-get install gitlab-ce
  SHELL 


#Mise en œuvre 
1.	Créer un répertoire pour le projet puis aller dedans avec "cd D:\chemin\du\projet".
2.	Inserer le fichier vagrantfile dans le répertoire
3.	à partir d'un invite de commande Powershell, écrire la commande "vagrant up" qui va télécharger la VM puis la lancer automatiquement avec virtualbox/VMWare 
4.	écrire la commande "vagrant ssh" pour acceder à la VM par SSH
5.	Lancer le gitlab avec la commande "sudo gitlab-ctl start"
6.	Vérifier que le module gitlab container registry est installé et actif avec la commande : "sudo gitlab-ctl status" 
