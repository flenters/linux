# linux

Test disk speed
dd if=/dev/zero of=rwc_test1 count=1024 bs=1M oflag=direct

Test Latency
mtr -rwc 20 --tcp --port 1433 hostname
