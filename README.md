# Issue-Reproducer

You can use this repository as template to fast setup an
Axon Ivy Engine with any external system. 

The Axon Ivy Engine runs with a license and has been connected
to a real system database. In front of Axon Ivy Engine there
is a reverse proxy which provides access over HTTP and not-trusted HTTPS.

# Ivy Configuration

Modify `ivy/ivy.yaml` to change the config of the Axon Ivy Engine.

# Ivy Logging

Modify `ivy/log4j2.xml` to change the logging.

# Deploy iar/app

Adapt the `ADD` command in `ivy/Dockerfile`.

# SSO

- Go to `ivy/ivy.yaml` and set `SSO.Enabled` to `true`.
- Comment in `#proxy_set_header X-Forwarded-User guest;` in `nginx/proxy.conf`. This will auto-login you always as `guest`
- Create a user called `guest` in default security context.
