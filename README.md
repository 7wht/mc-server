# dependencies: 

```
podman podman-compose
```


# copy tailscale-authkey-template to tailscale-authkey

```
cp tailscale-authkey-template tailscale-authkey
```

# add tailscale authkey to tailscale-authkey file

generate from https://login.tailscale.com/admin/settings/keys

```
echo "{your tailscale key} | tee tailscale-authkey"
```

# start minecraft server with

```
podman compose up
```


# connect to server console with

```
podman compose exec mc-server rcon-cli
```


# optionally copy plugins/ and server.properties to minecraft-data/

```
sudo chown -R $USER: minecraft-data/
cp -r plugins/ minecraft-data/
cp server.properties minecraft-data/
```
