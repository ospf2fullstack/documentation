# Documentation
Home Page content populated from my GitHub account at [ospf2fullstack/documentation](https://github.com/ospf2fullstack/documentation)

This site is deployed by creating a dockerfile that pull (git clone) my repository: 
`docker build -t ospf2fullstack/mkdocs:latest .`

Then docker push
`docker push ospf2fullstack/mkdocs:latest`

A replacement is then pushed for the deployment.yaml
`kubectl replace --force -f deployment.yaml -n mkdocs`

If the service needs to be redeployed: 
`kubectl create -f loadbalancer.yaml`, otherwise, replace, or leave alone... 
