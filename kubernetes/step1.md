#### Let's walkthrough manifests in `~/step1` ----->

#### Create new namespace

```
kubectl create namespace dso-demo
```{{exec}}

<br>

#### Create deployment and service

```
kubectl create -f ~/step1 -n dso-demo
```{{exec}}

<br>

#### Check status of namespace

```
kubectl get pods -n dso-demo -o wide
```{{exec}}

<br>

#### Let’s curl the root of the nginx!

```
curl http://POD-IP
```

<br>

#### What do you think happens if this container restarts?

```
kubectl delete pods -n dso-demo --all
```{{exec}}

<br>

#### Let’s curl again...

```
curl http://POD-IP
```

<br>

#### Retrieve the new pod IP

```
kubectl get pods -n dso-demo -o wide
```{{exec}}

<br>

#### Let’s curl with the new pod IP

```
curl http://POD-IP
```

<br>

#### Is this practical?
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