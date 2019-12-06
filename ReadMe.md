## Traefik with nginx and odoo 12

this project provide the file needed for running nginx and odoo 12 behind traefik v2, it will allow you to get a domain with a valide ssl certificate

#### Requirements

this project need that `docker` and `docker-compose` installed, also you need a server (or a virtual instance, i tested it using a `vultr` instance) with an ipv4 address(it may work using ipv6 but i can't test it because i don't have an ipv6 address) and a domain (i generally use `namecheap`) than point your domain to the ipv4 of the instance from the UI of your domain provider using an `A` type `DNS` record 

#### How to use

1. in the file `traefik.toml`, in `line 22` change `email` to the email you want to use for the creation of the SSL certificate (provided by `let's encrypt`), also change the `line 33, 36, 61 and 64` in file `docker-compose.yml` to your own domain (you may want to change some other line according to your need)
2. `cd ~ && git clone https://github.com/souhaiebtar/traefik_nginx_odoo.git traefik_odoo && cd traefik_odoo`
3. `touch acme.json && chmod 600 acme.json`
2. `docker-compose up -d`

#### To do

1. Automate the domain change (indicated in step 1 of [How to use](#### How to use))
2. some other stuff that i'm thinking about 🤔