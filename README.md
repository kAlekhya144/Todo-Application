# Multi Containers App

This is a repo for new users getting started with Docker.

You can try it out using the following command.

```docker compose up -d```

And open http://localhost:3000 in your browser.

https://hub.docker.com/repository/docker/kolaalekhya/todo-app/tags - docker hub image

before proceeding with deployment, make sure to check the database connection ( config/keys )

App & DB are present in different namespaces, DNS entrypoint (mongodb://todo-database.db-ns.svc.cluster.local:27017/todoapp) to communicate internally.

kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.2.1/deploy/static/provider/cloud/deploy.yaml - ingress controller

kubectl apply -f todo-database -n db-ns
kubectl apply -f todo-app
kubectl apply -f todo-ingress

<img width="437" height="127" alt="image" src="https://github.com/user-attachments/assets/60f09a27-6b7d-47d5-9f25-808557c03598" />

and then open http://todo.app.com/ in your browser 
