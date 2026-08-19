# argo-test

Configuration repository for [mini-argo](https://github.com/csakilan/mini-argo).

Nothing here is code. It is a set of plain Kubernetes manifests that a
`GitSource` points at. mini-argo clones this repository on an interval and
makes the cluster match whatever is in `manifests/`.

To change what runs in the cluster, edit a file here and push. Do not run
`kubectl apply`. That is the whole idea: the repository is the source of truth,
and anything applied by hand gets reverted on the next sync.
