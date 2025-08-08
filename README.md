# filebrowser

### https://filebrowser.org/installation.html#bare-alpine-image  

```bash
version: "3"
services:
    filebrowser:
        environment:
            - PUID=$(id -u)
            - PGID=$(id -g)
        volumes:
            - /path/to/srv:/srv
            - /path/to/database:/database
            - /path/to/config:/config
        ports:
            - 8080:80
        image: filebrowser/filebrowser
```
## First Boot¶
Your instance is now up and running. File Browser will automatically bootstrap a database, in which the configuration and the users are stored. You can find the address in which your instance is running, as well as the randomly generated password for the user admin, in the console logs.
