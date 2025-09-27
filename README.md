This is my old Nextcloud container setup if anyone finds it useful. It has

- Traefik reverse proxy with LetsEncrypt SSL certificates
- Nextcloud container with few tweaks. This a community maintained version of Nextcloud designed for expert use
- MariaDB database for better performance, though PostgreSQL probably would be even faster
- Redis memory caching to improve performance
- Collabora Code container to improve performance
- cloudflare-ddns dynamic DNS updates to update public DNS, if you want Nextcloud be accessed from internet

This setup assumes you have your own domain hosted in cloudflare so that Traefik can use DNS challenge when requesting Lets Encrypt certificate. The whole setup otherwise don't need to be exposed to internet.
You need Cloudflare API key from here: https://dash.cloudflare.com/?to=/:account/profile/api-tokens

Traefik also support other DNS providers, list can be found here: https://doc.traefik.io/traefik/v3.2/https/acme/

Sensitive credentials are separated under separate .env files.

