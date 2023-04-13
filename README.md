# DockerTorClient
Using the Ubuntu Docker image and installing and using the tor client via the sock5 proxy service.

The below will spin up a Pod in your kubernetes cluster with the latest Ubuntu image from your defualt repo.  Then attach you to a interactive terminal.

```powershell
docker run --name "torclient" --hostname "torclient" --rm -it ubuntu:latest /bin/bash
```
> **__Tip:__** You can run it in k8s too
```powershell
kubectl run torclient --image "ubuntu:latest" --rm -it -- /bin/bash
```

You can run the following to see a replay of what I ran to setup and use the tor socks5 proxy via curl.

```bash
scriptreplay --timing time_tor_test.tm tor_test
```

> **__Tip:__** You can run the below on your typescript file (tor_test for me) to get what command where ran quickly

```bash
grep "^\#\s\w" tor_test
```
