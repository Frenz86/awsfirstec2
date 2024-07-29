# awsfirstec2

###############################
macchina6 

## Machine PUBLIC IP 18.134.158.156

`ssh-keygen -R 18.134.158.156`

`ssh -i mygpt.pem ubuntu@18.134.158.156`

#scp -i mygpt.pem -r your_local_folder ubuntu@13.42.65.228:/path/to/destination

##############################################################

##ssh config vscode
```
Host macchina6
    HostName 18.134.158.156
    User ubuntu
    IdentityFile "C:\Users\Frenz2\My Drive\Lesson\IFOA\IFTS-FSTACK\Less06\mygpt.pem"

```
##############################################################
