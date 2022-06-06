## Problem Statement 1
Microservices are an architectural and organizational approach to software development where software is composed of small independent services that communicate over well-defined APIs. Microservices architectures make applications easier to scale and faster to develop, enabling innovation and accelerating time-to-market for new features.
Docker and Kubernetes are almost synonymous to 'microservices' as they help package and manage the different components of a project/ application, thereby easing up the implementation of a microservices architecture.


## Commands to create a pod and get it up using kubernetes

<h4>First, we need to create an image of the flaskapp using the flask-app-image.dockerfile. </h4>

To create an image of the flaskapp - docker build . -f flask-app-image.dockerfile -t imagename:tag 

To push the image to docker repo: 

docker login 

docker tag imagename YOUR_DOCKERHUB_NAME\imagename
  
docker push YOUR_DOCKERHUB_NAME\imagename <br>

<h4> Now, we create the required pods using the following commands </h4>

kubectl apply -f secret.yaml

kubectl apply -f services.yaml

kubectl apply -f deployments.yaml

kubectl apply -f configmap.yaml

kubectl get all

**Open localhost:4444**

**Open localhost:5555**


## Output Screenshots

**Create Post**

![first_ss](https://user-images.githubusercontent.com/85231677/161023101-db62dad5-940b-4d50-99f1-d4263bd2fe35.png)


**Post created successfully !**

![2nd_ss](https://user-images.githubusercontent.com/85231677/161023181-7ee5a707-d08e-467d-8768-0b6b488ed765.png)


**Edit the post**

![3rd_ss](https://user-images.githubusercontent.com/85231677/161023260-febe897b-cd01-414e-b6c0-1966cc061743.png)


**localhost:4444**

![4th_ss](https://user-images.githubusercontent.com/85231677/161023342-2e7cd725-e105-4b03-b409-75cff4796dd5.png)


**Database FrontEnd - localhost:5555**

![5th_ss](https://user-images.githubusercontent.com/85231677/161023400-886440ca-6b65-4caf-9cee-0a7ac1ccf924.png)


## Team Members -:

**B Pravena** - PES2UG19CS076

**Chandrahas L** - PES2UG19CS096

**Deepa Shree CV** - PES2UG19CS105

**Deepali Suraj Attavar** - PES2UG19CS106
