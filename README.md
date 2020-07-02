## Authentication Config

### Generate htpasswd file
```
htpasswd -cBb auth/htpasswd user pass
```

## CapRover Config

### Nginx
Edit the default app nginx config, replacing it with the config in nginx.cong

### HTTP Port
Change the container HTTP port to 5000

### Environment Variables
Add the following environment variables

```
REGISTRY_AUTH=htpasswd
REGISTRY_AUTH_HTPASSWD_PATH=/auth/htpasswd
REGISTRY_AUTH_HTPASSWD_REALM=Registry Realm
```
