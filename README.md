# Step to build and deploy
## step to docker build 
![image](https://github.com/vijaymoorthy/Google-Kubernetes-Deployment-ServiceExample/assets/5792365/87f3bf55-f3c8-4cce-814a-b149fa369cc4)
## to connect and use kubectl 
![image](https://github.com/vijaymoorthy/Google-Kubernetes-Deployment-ServiceExample/assets/5792365/7049d326-eeb3-47ad-9f05-98bcaaf244d8)


## create and artifact registry and copy the artifact location name for next step
![image](https://github.com/vijaymoorthy/Google-Kubernetes-Deployment-ServiceExample/assets/5792365/2986bfa3-cf09-44ce-bddc-6cff348c9654) 

## Build and Push the image to google Artifact registry (blue,green, red)
![image](https://github.com/vijaymoorthy/Google-Kubernetes-Deployment-ServiceExample/assets/5792365/2e3a98b0-4f16-4100-bfe9-d7d011584846)

##Push green, red in similar fashion after changing code in python 
use the following steps 
 # in python  change Bgcolour to "limegreen","darkred"
 ![image](https://github.com/vijaymoorthy/Google-Kubernetes-Deployment-ServiceExample/assets/5792365/7b83f922-f00d-405e-9541-a7c8b545a3f5)
 #### for each code change build the image and push to artifact using 
 ### docker build . -t docker build . -t us-central1-docker.pkg.dev/freekubernetes/sample-poc-registry/myapp:<color>
 ### docker push us-central1-docker.pkg.dev/freekubernetes/sample-poc-registry/myapp:<color>
### following will be in artifacts 
 ![image](https://github.com/vijaymoorthy/Google-Kubernetes-Deployment-ServiceExample/assets/5792365/383ccaf5-f33c-4887-8c65-4cd679b376ab)
 
## use kubectl to run deployment and services
![image](https://github.com/vijaymoorthy/Google-Kubernetes-Deployment-ServiceExample/assets/5792365/a3af7c96-5950-4dc3-a22e-53d202964807)
## get service and check the browser 
![image](https://github.com/vijaymoorthy/Google-Kubernetes-Deployment-ServiceExample/assets/5792365/bebbe722-815f-46e4-a9c7-5e33bcfaa0f7)
![image](https://github.com/vijaymoorthy/Google-Kubernetes-Deployment-ServiceExample/assets/5792365/4917a0a0-3aa4-4234-b9c9-0252fc9ecd6a)
## to get the nodes and pods use this 
kubectl get pods -o=custom-columns=NODE:.spec.nodeName,NAME:.metadata.name
## to change the deployment from Blue to Green
### change the deployment yaml
![image](https://github.com/vijaymoorthy/Google-Kubernetes-Deployment-ServiceExample/assets/5792365/a6f7d72d-4eef-44fb-8230-ab0579755f8a)
### run kubectl apply 
#### kubectl apply -f myapp-deployment.yaml
new sceen with blue deploy
  ![image](https://github.com/vijaymoorthy/Google-Kubernetes-Deployment-ServiceExample/assets/5792365/c86c21eb-4c0b-43ea-8aab-2135c0fcdd2a)


  
















