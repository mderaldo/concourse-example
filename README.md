# Concourse Installing Example

#For Mac
This tutorial is for Mac users. You'll need to have the [docker][docker] installed in your machine.

#Generate Keys

As the example in the [concourse][concourse-site], you should to create the keys to connect the agents with the host, as follow:

```
mkdir -p keys/web keys/worker

ssh-keygen -t rsa -f ./keys/web/tsa_host_key -N ''
ssh-keygen -t rsa -f ./keys/web/session_signing_key -N ''

ssh-keygen -t rsa -f ./keys/worker/worker_key -N ''

cp ./keys/worker/worker_key.pub ./keys/web/authorized_worker_keys
cp ./keys/web/tsa_host_key.pub ./keys/worker
```

#Install Fly CLI


[concourse-site]: http://concourse.ci/
[docker]: https://docs.docker.com/docker-for-mac/install/#download-docker-for-mac
