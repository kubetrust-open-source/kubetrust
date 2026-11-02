# kubetrust

AI-automated attacks increase the speed and scale of intrusions, so defenders must understand the blast radius of a compromise and contain it early. Kubernetes allows all pod-to-pod traffic by default, and workloads are often over-privileged, so one compromised pod can reach much of the cluster.
The project lets Kubernetes operators map internal pod dependencies by combining static analysis (manifests, RBAC, network policies) with runtime traffic observation using eBPF. This shows both what each workload is allowed to reach and what it actually communicates with.
Expected result: an operator selects a pod and sees what it can reach, what its permissions allow it to do, and its resulting blast radius. This dependency map gives operators the evidence needed to plan segmentation, by showing which workloads belong together and which access paths are unnecessary. 
All the code will be released under Apache 2.0 licence
