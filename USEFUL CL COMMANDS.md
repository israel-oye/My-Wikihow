## 1. Check if a postgres host is active
`pg_isready -h <host> -p <port>`

## 2. Check if a service is active on Linux
`sudo service <service>`
`systemctl <service> status`

## 3. Run commands in active docker container
`docker-exec -it <container-id> <command>`
