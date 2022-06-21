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
## Multibranch pipeline
- #### create a new project enter name and select multibranch pipeline
![image](https://user-images.githubusercontent.com/103022040/168459715-2f0c82f8-2c2d-4933-940e-782c097305d2.png)
- #### add the git source and clone the git project in general tab
 ![image](https://user-images.githubusercontent.com/103022040/168459764-122c753e-c37e-41b6-a82c-db5b376a0a44.png)
- #### add the credential 
![image](https://user-images.githubusercontent.com/103022040/168459854-8b673a72-c954-4d59-9b0e-7e9fb896e7e5.png)
- #### it is compulsory to have jenkins file 
![image](https://user-images.githubusercontent.com/103022040/168460058-474888fa-b50e-47f2-95aa-a80ea26f1362.png)
- #### this jenkins file contains the following code
![image](https://user-images.githubusercontent.com/103022040/168460088-0033084d-83ae-42dc-9674-13b825c13c8f.png)
- #### It contains the multiple branch
![image](https://user-images.githubusercontent.com/103022040/168460127-a74de377-809e-4703-95da-bac16ea837c5.png)
- #### When we scan it automatically detect the four branches 
![image](https://user-images.githubusercontent.com/103022040/168460275-c165d2ae-ca29-46d6-9419-9516a3ee2962.png)
- #### if we add a new branch slave right here 
![image](https://user-images.githubusercontent.com/103022040/168460353-2806a91b-944f-4f38-99ff-bf7a851a73f4.png)
- #### jenkins multilinepipeline automatically detect after scanning
![image](https://user-images.githubusercontent.com/103022040/168460397-6fbf7a10-d024-4249-b3e4-cea327cb9d9a.png)
- #### we can select which branch to scan in behaviour section 
![image](https://user-images.githubusercontent.com/103022040/168460485-3bcb2d5a-eb22-49f6-a29b-146ce083997c.png)
- #### when we scan it automatically detected only selected branches
![image](https://user-images.githubusercontent.com/103022040/168460666-e607594b-6950-4f8f-a03b-a84f3e611de9.png)
## Jenkins with https
- ####  Do this to generate one jenkins_keystore.jks in the home folder of ubuntu
![Capture1ststep](https://user-images.githubusercontent.com/103022040/174764084-1509784d-3d00-4881-9e7f-675d7bfc5506.JPG)
- #### Now, you can easily set up Jenkins to run on HTTPs while you are not making your own docket image:
![Capture2ndsteps](https://user-images.githubusercontent.com/103022040/174764712-6beb2d0b-8083-4406-9866-c1692a81d358.JPG)
- #### We can check a container is running 
![Capture3rdsteps](https://user-images.githubusercontent.com/103022040/174764971-1c1c9f09-4caa-47fd-a88b-364d191e08de.JPG)
- #### Jenkins running on https now we can check in local browser
![image](https://user-images.githubusercontent.com/103022040/174765801-b00be346-2922-4f45-8691-383591c60de0.png)
- #### link for this documentation https://intellipaat.com/community/11512/setup-secured-jenkins-master-with-docker





