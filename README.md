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
kubebuilder create api --group flux --version v1alpha1 --kind PodInfo

Create Resource[y/n]y

Create Controller[y/n]y

```


**Edit type**

```
make manifests
```


## Pod Controller

```bash
kubebuilder create api --group flux --version v1alpha1 --kind Pod

Create Resource[y/n]n

Create Controller[y/n]y
```

```
make manifests
```

## Code Generator
