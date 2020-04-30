# linux

Test disk speed
dd if=/dev/zero of=rwc_test1 count=1024 bs=1M oflag=direct

Test Latency
mtr -rwc 20 --tcp --port 1433 hostname

Difference between folders
diff -qr dir1 dir2

To test secure POP3 or IMAP
openssl s_client -crlf -connect pop3.yourserver.com:995 #995 for pop3 and 993 for imap

CIFS Mount
sudo mount -t cifs -o user=username,vers=2.0 //remoteserver/share /home/share

Delete file within a date range
find . -type f -newermt ' 08 oct 2018 00:00:00' -not -newermt '31 dec 2018 00:00:00' -ls
find . -type f -newermt ' 08 oct 2018 00:00:00' -not -newermt '31 dec 2018 00:00:00' -delete


Use file as input to grep
grep -i -f inputfile.txt filetocheck.txt > output.log

find a process from a port numner
netstat -tulpn | grep portnumber

check folder size
du -sh folder/

#################
##Docker Basics##
#################

Pulls Image
docker-compose pull 

Stops / Starts Image 
docker-compose down
docker-composeup -d //-d for background

List running images
docker container ps

Inspect Image logs
docker container logs image-name

Check Network
docker network inspect network-name

