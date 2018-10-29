Steps für FTP aus yt Video https://www.youtube.com/watch?v=c11rYDqJFcY
configuration file: http://vsftpd.beasts.org/vsftpd_conf.html

Rechner 1: Server
1. ifconfig IP: bei eth0
2 sudo apt-get install vsftpd
3. nano /etc/vsftpd.conf
4. Config nach Belieben und gebrauch ändern; zBsp: listen= yes, #listenipv6, anonymous_enable=YES, local_enable=YES, write_enable=Yes, local_umask=022, anon_upload, mkdir, dirmessage_enable, use_localtime,xerflog_enable=yes, connect from port10, ftpd banner, pam_service, secure_chroot,  
5. service vsftpd restart
6. adduser name
7. in /home mit ls user überprüfen
9.1 in name test.txt erstellen

Rechner 2: Client
8. ftp ip von server
9.2 Kommandos: ls
10. put file name, file neuer name
