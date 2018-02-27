# k8s-demo
my kubernetes hacking, learnings and notes....

There are a lot more reliable information on the internet about kubernetes. These are my notes as I learn and play with k8s for work and funnies.

# gke notes
I was getting a little fustrated because I couldn't do a simple nslookup|host|dig on the GKE instance. Well if I would have RTFM I would have know it was running CoreOS and I had to use toolbox. More information can be found [here](https://cloud.google.com/container-optimized-os/docs/how-to/toolbox).

[kubectl cheatsheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

# kubernetes dashboard
To access the dashboard run:
```kubectl proxy```
and it is available locally at http://localhost:8001/ui
I authenticated with the bearer token located in  ~/.kube/config

# sample apps
I created very simple demo k8s app that is made up of a frontend and a backend service. The frontend service lets a user select a lanuage and sends that to the backend service, which use Google Translate to translate "Hello World" in the selected language. More information on these services can be found here:

[frontend translate service](https://github.com/anners/translate-fe)

[backend translate service](https://github.com/anners/translate-be)

![translate diagram](/images/k8s-translate-diagram.png)

# kubernetes architecture
The kubernetes site does a much better job of describing the
[architecture](https://github.com/kubernetes/community/blob/master/contributors/design-proposals/architecture/architecture.md) than I currently can. I have tried to diagram what I think the architecture of the nodes and control plane (aka master) look like. Again, I am still learning so this might not be completely correct.

![kubernetes architecture](/images/k8s-arch-diagram.png)
