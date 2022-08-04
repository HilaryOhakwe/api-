As requested to write a simple API and create an docker image from the API. Below is a screenshot of the Dockerfile
![image](https://user-images.githubusercontent.com/109979316/182938747-cd505d3a-d4e3-4328-894c-1c36d085f8de.png)

The API source code can be seen in my github repository.
![image](https://user-images.githubusercontent.com/109979316/182938991-1807355b-acc7-456e-94be-b43a9e911661.png)

I tried to use helm to deploy the kubernetes deployment file of the API however I had issue then I decided to use Azure pipeline to deploy to my AKS cluster.
![image](https://user-images.githubusercontent.com/109979316/182939368-3df1b60d-3648-4ca5-9c1f-92cc158f63d3.png)

I was able to build and push the API dockerfile image to Azure container registry and kubernetes service. I created a deployment and exposed a the deployment with a load balancer.


![image](https://user-images.githubusercontent.com/109979316/182939450-e80b8023-06d9-4b58-aad4-f754a3ebedea.png)


![image](https://user-images.githubusercontent.com/109979316/182939496-beeb7db8-19a3-410e-8ddb-08c3eba3a97d.png)


![image](https://user-images.githubusercontent.com/109979316/182939583-0b6b2a69-7e41-4b6b-92e5-963d9b1cf6e5.png)

I was able to access my API deployment from my browser using the load balancer API address and my container port.


![image](https://user-images.githubusercontent.com/109979316/182939684-0eb4c578-cf39-4b51-b220-407fe37eb543.png)


The next line of action is deploy nginx controller.

The first step to carry out is to create a namespace and add the nginx repository to helm.



![image](https://user-images.githubusercontent.com/109979316/182946435-2e84a1df-e8bc-4219-8c3e-df869663119d.png)


Download and install NGINX Ingress Controller in your cluster

![image](https://user-images.githubusercontent.com/109979316/182947376-76917563-f0d2-4f5f-9d87-9e4149bc0f8b.png)


Route Traffic to Your App

![image](https://user-images.githubusercontent.com/109979316/182949574-45c4c202-3db8-4b76-bd2d-363867ae4e62.png)









