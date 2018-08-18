# unifi2mqtt
> Connect Ubiquiti UniFi controller to MQTT 📡

### Usage in docker

```
docker pull riro/unifi2mqtt
docker run --detach --name unifi2mqtt --restart always --env unifi-host=192.168.100.11 --env unifi-post=8443 --env unifi-user=someuser --env unifi-password=secret --env unifi-site=default --env insecure=true --env url=mqtt://192.168.100.12 riro/unifi2mqtt
docker logs -f unifi2mqtt

Pass options to docker image as environment variables like: docker run --env insecure=true

Options:
  unifi-host      unifi hostname or address         [default: "127.0.0.1"]
  unifi-port      unifi port                               [default: 8443]
  unifi-user      unifi user                            [default: "admin"]
  unifi-password  unifi password                                [required]
  unifi-site      unifi site                          [default: "default"]
  insecure        allow ssl connections without valid certificate
  verbosity       possible values: "error", "warn", "info", "debug"
                                                         [default: "info"]
  name            instance name. used as topic prefix   [default: "unifi"]
  url             mqtt broker url            [default: "mqtt://127.0.0.1"]
```

## License

MIT © [Sebastian Raff](https://github.com/hobbyquaker)

[mit-badge]: https://img.shields.io/badge/License-MIT-blue.svg?style=flat
[mit-url]: LICENSE
