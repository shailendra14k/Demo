Custom wildcard DNS for OpenShift 4.x

openshift-install create manifests --dir=/ocp4.6/DEMO

cp -R manifests/ manifests_bk
cp -R openshift/ openshift_bk

vi cluster-ingress-02-config.yml

openshift-install create ignition-configs --dir=/ocp4.6/DEMO
