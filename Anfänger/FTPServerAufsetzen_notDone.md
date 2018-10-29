# FTP Server

Einen FTP Server aufzusetzen gestaltet sich einfacher, als man sich erwarten würde.
Hier habt ihr eine simple Schritt für Schritt Anleitung:

**Rechner 1: Server**

1. Im Terminal muss ersteinmal die IPAdresse herausgefunden werden.
    Dazu tippt ihr einfach den Befehl 'ifconfig' ein und sucht bei eth0 die IP heraus.

2. Als nächstes installiert ihr euch vsftpd über diesen Befehl (wieder im Terminal)
    ```
    sudo apt-get install vsftpd
    ```

3. Über 
    ```
    nano /etc/vsftpd.conf
    ```
    könnt ihr die Konfigurationsdatei öffnen und verändern.

4. Config nach Belieben und gebrauch ändern, zBsp: 
    ```
    listen= yes, #listenipv6, anonymous_enable=YES, local_enable=YES, write_enable=Yes, local_umask=022, anon_upload, mkdir,            dirmessage_enable, use_localtime,xerflog_enable=yes, connect from port10, ftpd banner, pam_service, secure_chroot, 
    ```

5. ```
    service vsftpd restart
    ```
    
6. ```
    adduser deinName
    ```
    
7. in 
    ```
    /home/ls
    ```
    user überprüfen



**Rechner 2: Client**
//todo wie starte ich client richtig

8. ftp ip von server

9. in 
    ```
    home/deinName 
    ```
    test.txt erstellen

10. ```
    put file name, file neuer name
    ```


Um die Schritte besser nachzuvollziehen könnt ihr euch auch dieses Video ansehen:
 https://www.youtube.com/watch?v=c11rYDqJFcY

Hier findet ihr eine Übersicht für die Config-Datei:
 http://vsftpd.beasts.org/vsftpd_conf.html

Hier ist auch nochmal ein guter Anleitungsartikel:
 https://wiki.ubuntuusers.de/vsftpd/
