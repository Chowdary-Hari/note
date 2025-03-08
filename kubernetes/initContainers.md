## init containers

```yaml
    spec:
      initContainers:
      - name: init-myservice
        image: busybox:1.28
        command: ['sh', '-c', "until nslookup mysql; do echo waiting for myservice; sleep 2; done"]
```
```yaml
    spec:
      initContainers:
      - name: init-myservice
        image: busybox:1.28
        command: ['sh', '-c', "until nslookup db-dev.daws78s.online; do echo waiting for myservice; sleep 2; done"]
```