### This repository shows how to write Dockerfile, docker-compose.yml and deployment.yaml files for a Flask project.
# Clone The Repository
1. Run `git clone https://github.com/berkguzel/Dockerfile-dockercompose-deployment.git` in your shell.
## Docker
1. Go into the file where Dockerfile is, run the `docker build -t #yourtag` .
1. Run `docker run -d -p 5000:5000 #yourtag` .
1. Run `curl localhost:5000`.

## Docker Compose
1. Go into the correct directory and run `docker-compose build` .
1. Run `docker-compose up -d` .
1. Run `curl localhost:5000` .

## Kubernetes
1. Go into the correct directory and run `kubectl apply -f deployment.yaml` .
1. Run `curl localhost:5000` .

## Helm 
1. `helm install --dry-run --debug ./mychart/ --generate-name`
2. `helm install /*name*/ ./mychart/ --set service.type=NodePort`
3. Run the commands showen by Helm CLI