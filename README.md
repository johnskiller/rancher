# rancher

## create ebs storage class
```
kubectl create -f ebs/
```

## create elb for ingress
```
kubectl create -f elb/
```

## deploy jenkins
resize the default disk size

```
vi jenkins/0-jenkins-pvc.yml
storage: 10Gi -> new size
```

```
kubectl create -f jenkins/
```

## deploy nexus
resize the default disk size

```
vi nexus/0-nexus-pvc.yml
storage: 10Gi -> new size
```

```
kubectl create -f nexus/
```
