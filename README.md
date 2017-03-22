# nginx-log-rotation
# pirates_vpn

root@machine:~# mkdir /script
#
root@machine:~# cd /script/
#
root@machine:~# wget https://raw.githubusercontent.com/piratesvpn/nginx-log-rotation/master/nginx_log_rotate.sh

### Archiving Nginx access log ###

# add crontab
sudo crontab -e 
# copy this to cron

## Rotate logs daily at 8 am (Assign your own time)
00 08 * * * sh /script/nginx_log_rotate.sh
## Delete the zipped log archives once a week (Set this as per your requirement)
55 07 * * 1 rm -rf /var/log/nginx/archive/*


