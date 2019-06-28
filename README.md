# linux

Test disk speed
dd if=/dev/zero of=rwc_test1 count=1024 bs=1M oflag=direct

Test Latency
mtr -rwc 20 --tcp --port 1433 hostname

Difference between folders
diff -qr dir1 dir2

To test secure POP3 or IMAP
openssl s_client -connect pop3.yourserver.com:995 #995 for pop3 and 993 for imap
