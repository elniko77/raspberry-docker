# raspberry-docker-setup

En este repositorio voy a documentar la configuración de mi raspberry pi 4. La mayoría de cosas servirían para otras versiones.


### Montaje de disco
En mi caso estoy usando un externo usb3 de 1tb.

Obtener el id del disco
    
    $ sudo blkid /dev/sda1
    
    
Agregar en /etc/fstab el disco para que lo monte en el arranque (uid y gid 1001 es de mi usuario, nss)

    UUID="CC3A8A033A89EB32" /mnt/media ntfs defaults,auto,users,rw,nofail,umask=000 0 0

### Contenedores

* transmission: cliente para bajar torrents, mapeado a /mnt/media (disco externo)
* pihole: server dns
* samba: dos recursos compartidos, datos y torrents



    
    
