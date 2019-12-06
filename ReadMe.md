## Traefik with nginx and odoo 12

this project provide the file needed for running nginx and odoo 12 behind traefik v2, it will allow you to get a domain with a valide ssl certificate

#### Requirements

this project need that `docker` and `docker-compose` installed, also you need a server (or a virtual instance, i tested it using a `vultr` instance) with an ipv4 address(it may work using ipv6 but i can't test it because i don't have an ipv6 address) and a domain (i generally use `namecheap`) than point your domain to the ipv4 of the instance from the UI of your domain provider using an `A` type `DNS` record 
