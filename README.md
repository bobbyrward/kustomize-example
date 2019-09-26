```
$ kubectl kustomize qa
apiVersion: v1
kind: PersistentVolume
metadata:
  name: qa-mms-app-efs
  namespace: mms-app
spec:
  accessModes:
  - ReadWriteMany
  capacity:
    storage: 10Gi
  cis:
    volumeHandle: fs-qaqaqa
  csi:
    driver: efs.csi.aws.com
    volumeHandle: fs-999aaa999
  persistentVolumeReclaimPolicy: Retain
  storageClassName: efs
  volumeMode: Filesystem
```

```
$ kubectl kustomize stage
apiVersion: v1
kind: PersistentVolume
metadata:
  name: stage-mms-app-efs
  namespace: mms-app
spec:
  accessModes:
  - ReadWriteMany
  capacity:
    storage: 10Gi
  cis:
    volumeHandle: fs-stagestagestage
  csi:
    driver: efs.csi.aws.com
    volumeHandle: fs-999aaa999
  persistentVolumeReclaimPolicy: Retain
  storageClassName: efs
  volumeMode: Filesystem
```

```
$ kubectl kustomize prod
apiVersion: v1
kind: PersistentVolume
metadata:
  name: prod-mms-app-efs
  namespace: mms-app
spec:
  accessModes:
  - ReadWriteMany
  capacity:
    storage: 10Gi
  cis:
    volumeHandle: fs-prodprodprod
  csi:
    driver: efs.csi.aws.com
    volumeHandle: fs-999aaa999
  persistentVolumeReclaimPolicy: Retain
  storageClassName: efs
  volumeMode: Filesystem
```
