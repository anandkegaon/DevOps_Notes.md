yum & apt in linux are packing manager which helps us to install the packages.

the same way in kubernetes for run number of .yml file (mainfest)as package we use helm 

helm is collection of manifest files in the form of packege using helm we can perform a task which is written inside the 

helm chart i.e yml files.

Helm charts is nothing but a combined manifest which can be presented to k8s cluster.

RELEASE : release is nothing but a chart versions ,when we executed the helm chart. If we run single chart multiple time then 
multiple release (versions) will get created , for each execution.

REPOSITORY : Storage where we can keep our helm charts local/remote which can be refered later like git/docker. 


Helm Template :

no hardcoded value is entered in the template so that we can refer a value from outside.
