# Jenkins
## Installation and setup of Jenkins
- Install jenkins and dependencies using linux command
![image](https://user-images.githubusercontent.com/103022040/167290421-5c76711b-122d-4bf5-bc4d-535e7c0f0f49.png)
- Once done copy password from given location to unlock jenkins 
![image](https://user-images.githubusercontent.com/103022040/167290495-101b16a2-45af-4357-b9fd-e0e084eadde8.png)
![image](https://user-images.githubusercontent.com/103022040/167290505-a23de276-e8bb-47cf-bcb5-a9b971991e2c.png)
- Customize jenkins and install suggested plugins
![image](https://user-images.githubusercontent.com/103022040/167290533-7a5d0af4-5363-480a-87fc-a097d4fa35e4.png)
- Create first admin users in Jenkins and fill details
![image](https://user-images.githubusercontent.com/103022040/167290663-aaed655e-c4be-4df1-9f77-0735ffcadb7a.png)
- Jenkins is ready to explore
![image](https://user-images.githubusercontent.com/103022040/167290722-807d9a42-5b3d-48a0-b3c5-f7fb3d257d72.png)
## Push image to docker hub using pipeline in jenkins from bit bucket
- Go to pipeline and write a script defining stage first to take a code from bit bucket
![image](https://user-images.githubusercontent.com/103022040/167294543-89c1ad27-9147-4afe-9969-d4bd267771ec.png)
- Here 'tk4' is a variable defined in jenkin credential with username and password
![image](https://user-images.githubusercontent.com/103022040/167294616-8f08a23e-29da-41a1-988a-964457a90b66.png)
- In second stage use following comand  to build docker image using docker file
![image](https://user-images.githubusercontent.com/103022040/167294755-84aa9082-d90b-4ca3-a753-ee8b2e3db7ab.png)
- In final stage push the image to docker hub as follows:
![image](https://user-images.githubusercontent.com/103022040/167294823-69eedf3c-6b2b-4aa4-8633-ea2ee71f8ae4.png)
- click on build now to check the stages 
![image](https://user-images.githubusercontent.com/103022040/167294892-f86a9c56-449d-4cdd-86b2-a8579bfac866.png)
- we can verify by checking in the docker hub
![image](https://user-images.githubusercontent.com/103022040/167294961-37a75d5c-6d28-4eef-8ae9-b07fc98db8a1.png)
## *Push image to git lab repository using pipeline in jenkins from bit bucket*
- #### Go to pipeline and write a script defining stage first to take a code from bit bucket
![image](https://user-images.githubusercontent.com/103022040/167294543-89c1ad27-9147-4afe-9969-d4bd267771ec.png)
- #### Here 'tk4' is a variable defined in jenkin credential with username and password
![image](https://user-images.githubusercontent.com/103022040/167294616-8f08a23e-29da-41a1-988a-964457a90b66.png)
- #### Build docker image using docker file 
![image](https://user-images.githubusercontent.com/103022040/167299838-e6f8abc0-d4b9-49f3-9395-4483f1da4b48.png)
- #### Generate a token in git lab use it as password and push image to git lab repository
![image](https://user-images.githubusercontent.com/103022040/167299924-0f6c0e45-12fe-472b-801c-6bed001c4874.png)
- #### Click on build now to check the stages 
![image](https://user-images.githubusercontent.com/103022040/167300007-a0371d84-c71f-47aa-8246-fbc9390a9436.png)
- #### We can verify by checking in git lab repository
![image](https://user-images.githubusercontent.com/103022040/167300052-1893d315-3c86-4505-bbe5-b59bb0b2ab84.png)

