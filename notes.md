# Docker 

## Networks

OVERLAY : multi instance docker
MAC/VLAN : visible sur le réseau comme une machine a part entière 
NONE : aucune visibilité 
Bridge : se connecte à internet sans exposer la machine 
Host : partage les interfaces réseaux de la machine 

## Volumes 
Volumes : persistance / gros volume 
Manipulation sur le système : BindMount 
Secret -> tmpfs (données temporaires) 


# KUBERNETES 
## Principes généraux
Master 

Kube-apiserver : api, envoie des commandes 

ETCD : Base de données sous la forme key => value 

Kube-Scheduler : Ordonnanceur ou mettre mettre les données 

Kube-Controller Manager -> Cartographie les différents workers et leurs états 

Workers 

Kubelet : qui va interagir avec Container Runtime Engine -> Docker 

Kube proxy : gestion de la mise en réseau 

## Objets
### POD 

Plus petite unité dans K8s 

Un pod c’est : 
1 ou plusieurs containers 
1 ip 
1 ou plusieurs volumes 
Un unique namespace 
Un network interne 

Le pod est l’hébergeur / l’empacteur 


### REPLICA SET 

Permet de maintenir un nombre minimal de POD  

### DEPLOYMENT 

Gérer les replicas set 




## Environnement  

Plain Key -> Value 

Config Map 

Secret 


## Réseau & Service 

NodePort : exposte directement pod à l’extérieur 

clusterIp : en interne uniquement 

LoadBalancer : uniquement sur cloud provider 

Ingress : NodePort + clusterIp permettant de jouer le role de reverse proxy / Nginx avec un port acceptable (contrairement au NodePort : port -> 30 000 ) ; configuration via des IngresRule 
