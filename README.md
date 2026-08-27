# k8s-homelab

Instructions:

1. Create the kind cluster with the configuration of the file:
`kind create cluster --config kind-config/cluster.yaml`

2. Deploy the kind version of ingress-nginx:
`k kustomize cluster-resources/ingress-nginx | k apply -f -`

3. Run:
`k kustomize argocd | k apply --server-side --force-conflicts -f -`
