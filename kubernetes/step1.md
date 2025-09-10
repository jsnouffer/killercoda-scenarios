#### Let's walk through manifests in `~/mkdocs` ----->

#### Create new namespace

```
kubectl create namespace dso-demo
```{{exec}}

<br>

#### Create deployment

```
kubectl create -f ~/mkdocs/deployment.yaml -n dso-demo
```{{exec}}

```
kubectl create -f ~/mkdocs/cm.yaml -n dso-demo
```{{exec}}

<br>

#### Check status of namespace

```
kubectl get pods -n dso-demo -o wide
```{{exec}}

<br>

#### Let’s curl the root of the nginx!

```
curl http://POD-IP:8000
```

<br>

#### What do you think happens if this container restarts?

```
kubectl delete pods -n dso-demo --all
```{{exec}}

<br>

#### Let’s curl again...

```
curl http://POD-IP:8000
```

<br>

#### Retrieve the new pod IP

```
kubectl get pods -n dso-demo -o wide
```{{exec}}

<br>

#### Let’s curl with the new pod IP

```
curl http://POD-IP:8000
```

<br>

#### Is this practical?
#### Let’s add a service object

```
kubectl create -f ~/mkdocs/service.yaml -n dso-demo
```{{exec}}

<br>


#### Let’s get the service IP

```
kubectl get svc -n dso-demo
```{{exec}}

<br>

#### Let’s curl with the service IP

```
curl http://SERVICE-IP
```

<br>

#### Let's delete the pod again

```
kubectl delete pods -n dso-demo --all
```{{exec}}

<br>

#### And, let’s curl with the service IP again

```
curl http://SERVICE-IP
```