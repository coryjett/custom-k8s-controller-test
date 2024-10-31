https://medium.com/@disha.20.10/building-and-extending-kubernetes-a-writing-first-custom-controller-with-go-bc57a50d61f7

kubectl apply -f custom-resource-definition.yaml

kubectl apply -f custom-resource.yaml

mkdir k8s-controller
cd k8s-controller
go mod init k8s-controller

go get k8s.io/apimachinery@v0.22.0 k8s.io/client-go@v0.22.0 sigs.k8s.io/controller-runtime@v0.9.0

go build -o k8s-controller .
./k8s-controller

