# 젯슨나노에 부족한 메모리를 위해 스왑으로 설정하기

free -m
swapon -s
sudo dd if=/dev/zero of=/var/swapfile bs=1G count=4
sudo mkswap /var/swapfile
sudo chmod 600 /var/swapfile
sudo vi /etc/fstab
-------------------------------------------------------------
/var/swapfile   /none   swap    swap    0 0
-------------------------------------------------------------
sudo swapon /var/swapfile
free -m
swapon -s
