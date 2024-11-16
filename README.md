# TP Kubernetes
Au cours de ce TP, vous allez commencer par installer un cluster K8S avec l'outil RKE (Rancher Kubernetes Engine). Ensuite, vous allez manipuler différents objets K8S (Workloads, Pods, Volumes etc). Vous finirez par déployer une application hautement disponible et auto-réparatrice composée de deux services distincts qui utilisent des volumes et des secrets.

**Attention!** Afin d'être évalué, vous devez rédiger un rapport où vous mettrez les réponses aux questions posées et la description de tous les objets créés au cours du TP. Veillez à bien utiliser les noms demandés pour les objets Kubernetes. 

--------

## Creation de l'infrastructure
Dans cette section, vous devez créer trois machines virtuelles dans OpenStack avec les caractéristiques suivantes:
- 4 vCPU
- 8Go RAM
- 20Go d'espace disque
- Réseau `vlan1374` ou `vlan1368` (Assurez-vous que toutes les machines virtuelles font partie du même réseau!)

Une machine sera le *Control Plane* et deux autres seront des *Worker Nodes*.

Afin de créer des machines avec 20Go d'espace disque, vous allez commencer par créer trois **Volumes** dans l'OpenStack avec l'image **Ubuntu Server 22.04.3 LTS - Docker Ready** comme **Volume Source**. Ensuite, vous allez créer trois machines avec 4 vCPU, 8 Go de RAM, réseau `vlan1374` ou `vlan1368` et avec les volumes précédemment créés comme sources de démarrage (**Boot Source**).

