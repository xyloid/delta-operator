# Outline

## CRD with ClientSet

```golang
type PodInfo struct {
    podname string
    nodename string
    cpu_limit float32
    cpu_request float32
}
```

### Initialize Project

```bash
MODULE=kubernetes.io/delta-operator
go mod init $MODULE
kubebuilder init --domain kubernetes.io
kubebuilder edit --multigroup=true
```

### Generate Resources and Manifests

```bash
kubebuilder create api --group kubeflux --version v1 --kind PodInfo
```
**Edit type**

```
make manifests
```


## Pod Controller

