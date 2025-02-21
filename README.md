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
