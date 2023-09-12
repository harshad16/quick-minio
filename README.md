Quick Minio Setup
=================

This repository contain the yaml file to quickly deploy a minio service on OpenShift cluster.

```oc apply -f minio.yml -n <namespace>```

Pre-requistes
-------------

Following requirements are needed.  
- Presistent Volume availability(atleast 2Gi)  
(If less please adjust the yaml file.)
- Resource: CPU: 250m ; Memory: 500Mi  

Host Route Setup
----------------

For host route setup with https availability,  
Recommend to do it from the route view of the openshift,  
that can be found under networking>routes.

or for simple http, use `oc expose svc/minio-sample`

Disclaimer: This is just for Testing use.  
Reference: https://min.io/docs/minio/kubernetes/upstream/index.html 