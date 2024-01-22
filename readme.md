#Repo Privado

argocd app create helm-guestbook-dev  --repo https://gitlab.com/andredeabreugoncalves/qa --path helm-guestbook --dest-server https://172.21.13.242:6443 --dest-namespace default

#Repo Publico 

argocd app create helm-guestbook-dev  --repo https://github.com/jonathanbaraldi/argocd-example-apps --path helm-guestbook --dest-server https://172.21.13.242:6443 --dest-namespace default



argocd app set helm-guestbook-dev --values values-qa.yaml

argocd app get helm-guestbook-dev
argocd app sync helm-guestbook-dev