#!/bin/bash
echo "##########Bienvenue sur mon projet sys###############"
echo "-------------------Choisir l'option à exécuter-----------------------"
echo "********##################**********###############"
echo "_____a) Informations sur les utilisateurs enregistrés il y a 3 jours______________"
echo "___________b) Acquisition,installation et lancement de xampp__________________"
echo "___________c) Archivage des elements du repertoire personnel__________________"
echo "___________d) Informations sur le disque, la memoire, le processeur et le swap________________"
echo "___________q/Q) Quitter_______________"
echo "******************************************************************"
echo "************ entrer votre option ****************"
read option
echo "******************************************************************"
echo "################## votre option est: $option ################ "
case "$option" in
a)
echo "---------------Informations sur les utilisateurs enregistrés il y a 3 jours-----------------"
for users in user=$(ls /home)
do
echo $users
done
exit 0;;
b)
echo "----------------- Acquisition,installation et lancement de xampp ------------------------------"
echo -e "installation de xampp"
  wget https://www.apachefriends.org/fr/download_success.html/xampp-linux-x64-5.6.30-1-installer.run;
	 echo -e "debut installation..."
	 sudo chmod +x ./xampp-linux-x64-5.6.3-0-installer.run
	sudo chmod 755 xampp-linux-*-installer.run
	sudo ./xampp-linux-*-installer.run
	
	 echo "demarrage..."
	sudo /opt/lampp/lampp start

exit 0;;
c)
echo "------------------- Archivage des elements du repertoire personnel ---------------------"
archivages()
{
mkdir -p /home/seed/archive
	find /home/seed/ -type f -mtime 2 -print>/home/seed/ficmodi
	while read line
	do
	cp $line archive
	done </home/seed/ficmodi
	tar -czvf archive.tar.gz archive
	mv archive.tar.gz /media/seed/usb/*/archive.tar.gz
}
exit 0;;
d)
echo "---------------- Informations sur le disque, memoire, processeur et swap --------------------------"
disk=$(sudo hdparm -i /dev/sda)
echo $disk
mem=$(cat /proc/meminfo)
echo $mem
cpu=$(cat /proc/cpuinfo)
echo $cpu
swap=$(cat /proc/swaps)
echo $swap
exit 0;;
q/Q)
echo "################ Quitter #############"
exit 0;;
*)
echo "------------------ Option à exécuter invalide consulter le menu svp... ---------------------"
echo "__________________ Merci de votre bonne comprehension!!! ___________________________"
exit 0;;
esac
echo "****************************************************************"
