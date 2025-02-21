Nginx with Docker
```
Step 1: Run an Ubuntu Container
docker run -it -p 8080:80 ubuntu

```
Step 2: Update and Install Nginx

```
apt update && apt install -y nginx
```
Step 3: Verify Installation
```
uname -a
ls -lh  Lists files in the current directory
```

Step 4: Install Vim (for Editing Files)
```
apt install -y vim
```
Step 5: Access the Running Container
```
docker exec -it <container_name_or_id> /bin/bash
Replace <container_name_or_id> with the actual container’s name or ID.
```
Option 2: Find and Free the Port
```
netstat -ano | findstr :8080
Look for the PID (Process ID) in the last column. Then, stop the process using:
taskkill /PID <PID> /F
```
Check if Vim is still running:
```
ps aux | grep vim
kill -9 <PID>
Delete the swap file:
rm -f /etc/nginx/.nginx.conf.swp
```
Open nginx.conf again in Vim:
```
vim /etc/nginx/nginx.conf
```
nginx configuration basic configuration
```
events {
}

either
type {
  text/css css;
  text/html html;
}
or
include /etc/nginx/mime.type

http {

        server {
             listen 80;
             server_name _;
             root /etc/nginx/website;
        }

}
```
