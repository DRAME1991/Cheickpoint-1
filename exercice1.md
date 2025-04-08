# Exercice 1 
 
1-lsblk 

2- fdisk /dev/sdb ensuite
   n = nouvelle partition; type p; numero 1; taille +6G
  n pour le swap; typ p; numero 2; reste du disque 

3- changement de type de la partition 2 
  t = change le type
    2 numero de partition 
   code 82 (swap linux)
   w = ecrit les modification 

4- verification avec lsblk /dev/sdb 

5- Formatage des partitions en ext4 
  mkfs.ext4 -l DATA /dev/sdb1

6- Partion SWAP 
 1mkswap -L SWAP /dev/sdb2

7- Activer/desactiver les SWAP 
 7.1 swapon /dev/sdb2
 7.2 swapoff /dev/sda5 
