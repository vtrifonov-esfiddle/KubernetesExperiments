# nginxPersistentVolume

- creates hostPath persistent volume
- creates claim using the volume
- creates nginx deployment using the claim
- exposed on node port 32605

```
cd nginxPersistentVolume
kubectl apply -f .\deployment-pv-volume.yaml
kubectl apply -f .\deployment-pv-claim.yaml
kubectl apply -f .\nginx-deployment.yaml
copy index.html "\\$env:COMPUTERNAME\c\Users\$env:USERNAME\.docker\Volumes\deployment-pv-volume"
start-process http://localhost:32605
```
