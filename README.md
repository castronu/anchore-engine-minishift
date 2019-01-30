Install minishift:

```
brew cask install --force minishift
```


```
minishift start  --routing-suffix 127.0.0.1.nip.io --vm-driver=xhyve --memory=8192 --cpus=4 --disk-size=50g  --openshift-version v3.10.0
```

```
oc adm policy add-scc-to-user anyuid -z default

```

```
oc adm policy add-scc-to-user anyuid system:serviceaccount:anchore-engine:analysis-anchore-policy-validator-init-ca
```

```
find . | grep ".yaml" | xargs -I {} oc apply -f {}
```

```
anchore-cli --u admin --p foobar system status

anchore-cli --u admin --p foobar image list
anchore-cli --u admin --p foobar  image add docker.io/library/debian:latest
```


 
