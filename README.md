# Demo

oc new-project demo

oc import-image ubi8/openjdk-8 --from=registry.redhat.io/ubi8/openjdk-8 --confirm

oc new-build --name=getpayment --image-stream=openjdk-8 --binary=true --labels=application=getpayment

oc start-build getpayment --from-file=getpayment-1.0.0.jar --follow

oc new-app getpayment

###
oc new-build --name=getbalance --image-stream=openjdk-8 --binary=true --labels=application=getbalance

oc start-build getbalance --from-file=getbalance-1.0.0.jar --follow

oc new-app getbalance

###
oc new-build --name=getotp --image-stream=openjdk-8 --binary=true --labels=application=getotp

oc start-build getotp --from-file=getopt-1.0.0.jar --follow

oc new-app getotp
