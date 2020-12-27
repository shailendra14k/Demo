# Custom default wildcard application subdomain for OpenShift 4.x

* Create manifests
```sh
openshift-install create manifests --dir=/ocp4.6/DEMO
mkdir manifests_bk && mkdir openshift_bk
cp -R manifests/ manifests_bk
cp -R openshift/ openshift_bk
```

* Update the manifest file
vi cluster-ingress-02-config.yml
```yaml
apiVersion: config.openshift.io/v1
kind: Ingress
metadata:
  creationTimestamp: null
  name: cluster
spec:
  domain: apps.ocp4.consulting.local
status: {}
```

* openshift-install create ignition-configs --dir=/ocp4.6/DEMO
