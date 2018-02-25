# k8s-demo
my kubernetes hacking, learnings and notes....

# gke notes
I was getting a little fustrated because I couldn't do a simple nslookup|host|dig on the GKE instance. Well if I would have RTFM I would have know it was running CoreOS and I had to use toolbox. More information can be found [here](https://cloud.google.com/container-optimized-os/docs/how-to/toolbox).

[kubectl cheatsheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

# sample apps
I created very simple demo k8s app that is made up of a frontend and a backend service. The frontend service lets a user select a lanuage and sends that to the backend service, which use Google Translate to translate "Hello World" in the selected language. More information on these services can be found here:

[frontend translate service](https://github.com/anners/translate-fe)

[backend translate service](https://github.com/anners/translate-be)


# kubernetes dashboard
To access the dashboard run:
```kubectl proxy```
and it is available locally at http://localhost:8001/ui
I authenticated with the bearer token located in  ~/.kube/config
