# Configure Tanzu Mission Control

###### Make sure you are connected to TMC via Consolidated

Run the below command to verify TMC context

```bash
tmc system context current
```

Create a ClusterGroup in TMC for this lab. Add your initials to the name of the cluster group
```bash
tmc clustergroup create -n <initials>-tkg-hol-cg -d 'TKG HOL Cluster Group'
```
Attach Shared Service Cluster to TMC, and apply the kubectl command generated by TMC Attach.

```bash
tmc cluster attach -n tkg-shared-svc-cluster -g <initials>-tkg-hol-cg

kubectl apply -f <k8s-attach-manifest>.yaml
```

Continue to Next Step: [Install Cert Manager](02-install-cert-manager.md)