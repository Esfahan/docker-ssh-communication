# docker-ssh-communication
Containers for test ssh communication

## Usage
### Generate ssh key

```bash
$ ./bin/create_key
```

### docker-compose up

```bash
$ docker-compose up -d --build
```

### Wait for the ssh process booting
Check the process with below command.

```bash
$ ./bin/sshd_statuses
```

## Test
### ssh connection
You can connect to the container with the own name.

```bash
$ sudo docker exec -it ssh_from /bin/bash -c 'ssh ssh_to'
```

### rsync

```bash
$ sudo docker exec -it ssh_from /bin/bash -c 'rsync -ra --omit-dir-times /code/data ssh_to:/code/ -v'
```
