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
## *Create and Manage Users in Jenkins*
- #### link for the documentation https://www.javatpoint.com/create-and-manage-users-in-jenkins
### Install Role-based Authorization Strategy Plugin
- #### Open your Jenkins dashboard by visiting http://localhost:8080/jenkins
![image](https://user-images.githubusercontent.com/103022040/175924235-ec416b7a-642b-42e1-91f7-160746106358.png)
- #### Click on manage jenkins select manage plugin
![rolebased1](https://user-images.githubusercontent.com/103022040/175924829-d6e90cea-24c1-460f-8905-a750c332697f.JPG)
- #### Select availabe tab in manage plugin and type role-based and press enter
![image](https://user-images.githubusercontent.com/103022040/175925728-e3ed665b-1658-4c91-bc3c-bb0b8e08e43f.png)
- #### Now, select the plugin and click on 'Install without restart' button.
![jenkinsrolebase3](https://user-images.githubusercontent.com/103022040/175925939-21aaa8cd-7413-4b99-adf9-b92121c2ed5e.JPG)
### Enable Role-Based Strategy on Jenkins
- #### After Plugin installation, go to the 'Manage Jenkins' and then click on 'Configure Global Security'
![rolebased4](https://user-images.githubusercontent.com/103022040/175927529-93bb86c0-eb75-4468-bf8c-2a0b78253c70.JPG)
- #### On Authorization section, select 'Role-Based Strategy'. And click save.
![image](https://user-images.githubusercontent.com/103022040/175927885-1eda7fe9-4f42-46e7-ae4a-de0647bf8561.png)
- #### Click on manage user and create first user 
![rolebased8](https://user-images.githubusercontent.com/103022040/175928760-c1e3415f-13d6-4414-b1cd-c2bb46568000.JPG)
- #### Create first user and click on save button 
![rolebased9](https://user-images.githubusercontent.com/103022040/175928923-c38d3e76-57a3-4ba1-afd1-877801699e0d.JPG)
- #### Create another user
![rolebased12](https://user-images.githubusercontent.com/103022040/175929073-b1e14f3d-0e0f-465e-95f1-34eb7b79606f.JPG)
- #### The following user has been created
![rolebased13](https://user-images.githubusercontent.com/103022040/175929261-bc10d776-7262-4750-84c6-e36093208824.JPG)
### Managing User Roles on Jenkins
- #### Click on Manage Jenkins.Select Manage and Assign Roles. Note that, Manage and Assign Role will only be visible if you have installed the Role strategy plugin.
![rolebased14](https://user-images.githubusercontent.com/103022040/175929768-3591a562-743a-423d-ae82-4b2f19924c3a.JPG)
- #### Click on Manage Roles option to add new roles.
![rolebased16](https://user-images.githubusercontent.com/103022040/175930073-debda4f4-6a0b-493f-b6d9-d9ac1dce324c.JPG)
- #### To create a new role called "developer". Type "developer" in the Role to add option.Click on Add to create a new role.Now, select the appropriate permissions     ####  that you want to assign to the developer role.Then Click on Save button.
![rolebased17](https://user-images.githubusercontent.com/103022040/175930847-c5265859-8839-4caf-a762-d6d3878460c7.JPG)
## *Jenkins using Docker in Docker*
- #### Run the following command to run docker in docker 
![dockerin docker 1](https://user-images.githubusercontent.com/103022040/176106462-85414ce9-dfa4-4357-8992-f078758d7a68.JPG)
- #### We can check container running using docker ps command 
![dockerindocker2](https://user-images.githubusercontent.com/103022040/176106590-e5e2fe0d-4c66-405f-89e7-d16b9ab4dee9.JPG)
- #### Now we need to pull a jenkins image from docker hub
![dockerindocker4](https://user-images.githubusercontent.com/103022040/176107880-5ab08840-f58f-4439-854a-19765c96e710.JPG)
- #### Now we can see jenkins as a container using ps -a
![dockerindocker5](https://user-images.githubusercontent.com/103022040/176108026-32302b59-700c-4726-bb4e-2cef7d9ed657.JPG)
- #### We need to start the jenkins and run it as a container 
![dockerindocker6](https://user-images.githubusercontent.com/103022040/176108122-21431ff2-0950-43f4-9b0a-2fdb5fc5252b.JPG)









