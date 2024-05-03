The CSI Driver expects a secret in the following format:

```
apiVersion: v1
kind: Secret
metadata:
  name: exoscale-csi-driver-credentials
  namespace: kube-system
type: Opaque
stringData:
  EXOSCALE_API_KEY: "EXOSCALE_API_KEY"
  EXOSCALE_API_SECRET: "EXOSCALE_API_SECRET"
```

The Key must have the following permissions:

['list-zones', 'get-block-storage-volume', 'list-block-storage-volumes', 'create-block-storage-volume', 'delete-block-storage-volume', 'attach-block-storage-volume-to-instance', 'detach-block-storage-volume', 'update-block-storage-volume-labels', 'resize-block-storage-volume', 'get-block-storage-snapshot', 'list-block-storage-snapshots', 'create-block-storage-snapshot', 'delete-block-storage-snapshot']
