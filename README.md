## Running Anthos on GKE

Basic Overview of Pulumi Deploying an Anthos Solution

```sh
     Type                                                                 Name                               Plan
     pulumi:pulumi:Stack                                                  google-demo-google-anthos
 +   ├─ gcp:projects:Service                                              service-4                          create
 +   ├─ gcp:projects:Service                                              service-5                          create
 +   ├─ gcp:projects:Service                                              service-3                          create
 +   ├─ gcp:projects:Service                                              service-6                          create
 +   ├─ gcp:projects:Service                                              service-8                          create
 +   ├─ gcp:serviceAccount:Account                                        gke-sa                             create
 +   ├─ gcp:container:Cluster                                             cluster                            create
 +   ├─ gcp:projects:Service                                              service-7                          create
 +   ├─ gcp:projects:IAMMember                                            service-account-1                  create
 +   ├─ gcp:projects:IAMMember                                            service-account-2                  create
 +   ├─ pulumi:providers:kubernetes                                       gkeK8s                             create
 +   ├─ gcp:projects:IAMMember                                            service-account-0                  create
 +   ├─ gcp:container:NodePool                                            demo-1-np                          create
 +   ├─ kubernetes:rbac.authorization.k8s.io/v1:ClusterRole               config-mgmt-operator-cluster-role  create
 +   ├─ kubernetes:rbac.authorization.k8s.io/v1:ClusterRoleBinding        config-mgmt-operator-cluster-role  create
 +   ├─ kubernetes:core/v1:ServiceAccount                                 service-account                    create
 +   ├─ kubernetes:core/v1:Namespace                                      cfgmgmt-namespace                  create
 +   ├─ kubernetes:apiextensions.k8s.io/v1beta1:CustomResourceDefinition  config-mgmg-operator-crd           create
 +   ├─ kubernetes:configmanagement.gke.io/v1:ConfigManagement            my-new-foobar-object               create
 +   └─ kubernetes:apps/v1:Deployment                                     config-mgmt-operator               create
 ```

