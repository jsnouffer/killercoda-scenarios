#### Let's walkthrough manifests in `~/step2` ----->

#### Create new namespace

```
kubectl create namespace dso-demo-2
```{{exec}}

<br>

#### Create deployment and service

```
kubectl create -f ~/step2 -n dso-demo-2
```{{exec}}

<br>

#### Check status of namespace

```
kubectl get pods -n dso-demo-2 -o wide
```{{exec}}

<br>


#### Let’s get the service IP

```
kubectl get svc -n dso-demo-2
```{{exec}}

<br>

#### Let’s curl with the service IP

```
curl http://SERVICE-IP
```

<br>
