# Normalize path

### Configuration

Enable the plugin in your Traefik configuration:

```
[experimental.plugins.normalizepath]
  modulename = "github.com/bchangiphc/normalizepath"
  version = "v0.0.1"
```

Create a Middleware. Note that this plugin does not need any configuration, however, values must be passed in for it to be accepted within Traefik.

```yaml
---
apiVersion: traefik.containo.us/v1alpha1
kind: Middleware
metadata:
  name: normalizepath
spec:
  plugin:
    lowercase:
      unused: var
```
