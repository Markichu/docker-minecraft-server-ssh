This docker image provides an extended fork of [itzg/docker-minecraft-server](https://github.com/itzg/docker-minecraft-server) which has been modified to include an embedded SSH server within the docker container.

To simply use the latest stable version with SSH, run

    docker run -d -it -p 25565:25565 -p 22:22 -e EULA=TRUE -e SSH=TRUE markichu/minecraft-server-ssh

-p 25565:25565 exposes the containers 25565 port to your local machines 25565 port. This is necessary to allow other players to join the Minecraft server.

-p 22:22 exposes the containers 22 port to your local machines 22 port. This is necessary to allow SSH connection into the container.

-e EULA=TRUE agrees to the EULA to allow the server to pass Mojang’s EULA requirements.

-e SSH=TRUE enables the SSH server to run with the default username and password of `user` and `pass`.

## SSH Environment Variables

### Enable/Disable SSH

Enable or Disable SSH by editing the `SSH` environment variable. This is set to `FALSE` by default.

To enable SSH simply add the `SSH=TRUE` environment variable.

### Change SSH Username

Set a custom SSH username by setting the `SSH_USER` environment variable. By default, the SSH username is `user`.

For example, `SSH_USER=admin`.

### Change SSH Password

Set a custom SSH password by setting the `SSH_PASS` environment variable. By default, the SSH password is `pass`.

For example, `SSH_PASS=password`.

## Other Environment Variables

For modifying the Docker image in any other way. The upstream repository outlines environment variables to do almost anything you could want to do. Please see [itzg/docker-minecraft-server](https://github.com/itzg/docker-minecraft-server).

## Support itzg

The original author and many other brilliant contributors have created a perfect Minecraft Docker image. Please consider [buying them a coffee]( https://www.buymeacoffee.com/itzg) or [donating to them on paypal]( https://paypal.me/itzg).
