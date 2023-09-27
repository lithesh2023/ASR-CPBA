# Car Parking Booking Application 
ASR document for Car Parking Booking Application

## Car parking booking Application

### Team members
1. Anil Kumar Upadhyay
2. Janmejay Pattanaik
3. Lenin Govindan
4. Lithesh Pulikkool
5. Narendiran Parassouramin
6. Vivek Lingesan
   
## Purpose and Scope
Car Parking Booking system is a reliable system which is implemented to full fill all the requirements. The booking system is responsible for the implementation of standard administrative function, such as sending booking code and acknowledgement, updating parking lots and generating the essential reports. The objective of the proposed system is to manage the car parking operations more efficiently, to improve the services for customers, to allow customers to be able to check the status of parking lot, to reduce time and save fuel when customer finding parking space, to prevent human mistakes such as inaccurate car parking slots, location etc. It provides a user-friendly platform for users, parking staff, and administrators to streamline the entire parking process efficiently.
Objective of the application is to resolve –
- Parking Congestion
- Delays trying to find a Parking Spot
- Lack of Structured Parking due to unavailability of knowledge of empty Parking Spaces
- Wastage of Fuel and Time resulting in some form of personal loss
- Ease of Payment

***Following are the scope of the application***
- **Search and Compare**-Forusers,theonlinesystemoffersaconvenient way to search for available parking slots, Compare the slots based upon the features like, floor, distance from entry/exit gate etc.

- **Booking**-Booktheparkinginadvance(maximum2daysadvance)and navigate to the designated spot using integrated navigation features. Users can also make cashless payments for parking fees through secure online transactions, eliminating the need for physical tickets and reducing waiting times.
- **History** –Booking history,
- **Parking Management(AddParkingslots/pricing/billing–admin features)**
- **Integrate driving direction(O)**
- **Integration with Chatsystem**
- **Integration with IoT(O)**

## Intended Audience
***Following are the intended audiences for the system***
1. CarOwners(Registered/Unregisteredusers)
2. Admin
   - MallOwner(O)
   - Malla dministrator
   - Mall supervisor

## Business Context
**Stakeholders**
   1. Client
   2. Product Owner (PO)
   3. Application Architect
   4. FSE developers
   5. Data Base Architect
   6. QA Testers

## Business Goals
***Following are the intended business goals the Car Parking Booking application is planning to address**
   1. Reduce parking congestion.
   3. Delays trying to find a Parking Spot
   4. Lack of Structured Parking due to unavailability of knowledge of empty Parking Spaces
   5. Wastage of Fuel and Time resulting in some form of personal loss
   6. Ease of Payment

## Constraints
 	 
<img width="680" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/3654281a-71ea-4105-a140-4f577731bdc6">



## Architecturally Significant Requirements 
  
<img width="680" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/c8b0f0c6-baed-4955-88bc-0731d5e9947b">
    
## Quality Attribute Requirements
<img width="680" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/7d7dab8f-330b-467b-b02f-c8714486f889">


## Influential Functional Requirements

1. Payment gateway
2. Chat application external
3. History

## Non-Functional Requirements:

* ﻿﻿The application has to run 24*7
* ﻿﻿There will be 50k-100k DAU and around 30-4omillion MAU.
* There will be average 10-15k bookings happening in one day.
*  The app has to be always up and running without any downtime in case of disaster.
*  Each booking completion should take max 2 seconds.
* ﻿﻿Any search operation on the app should take max 1 seconds.
*  All the payments and user data should be securely stored and accessed.

## Context Diagram
  <img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/4c8f9a00-1c86-49d7-b060-44d7d2b9bc48">

## Component Diagram
  
<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/e018d1de-5928-4490-a7fb-689b9d113a27"><img width="128" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/39d58ee4-7220-460e-ad45-15bac43066f9">


## Container Diagram
<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/2fca5f07-4262-4cad-a898-0fc4b5cebcdb">

## Deployment Diagram

![DeploymentDiagram](https://github.com/lithesh2023/ASR-CPBA/assets/138496677/f89ad327-b4a0-4537-8dd0-6f646fe14339)


## Branching Strategy
We are opting for Trunk Based branching (development) Strategy. This involves developers integrating their changes directly into a shared trunk (master) at least once a day. This shared trunk is always in a releasable state. Developers can pull from this trunk, create a local repository, and then push the code to the shared trunk.
This regular integration enables developers to view each other’s changes quickly and immediately react if there are any conflicts.

<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/ce735e92-4da7-44ef-9825-885a1955a7b2">

 Following are a few advantages for using TBD strategy –
- One of the most preferred branching strategies used for a microservice architecture. This is a fast workflow with minimal merging.
- True continuous integration as developers constantly keeps the trunk updated.
- Excellent choice for CI/CD pipelines with simpler workflows for automated testing
- Shorter feedback loops for developers as code changes are quickly visible.
- Lead to faster release cycles
- Smaller iterations allow teams to keep track of all the changes while reducing code conflicts and improving overall code quality.

## CICD pipeline
We have implemented CICD pipeline for our front-end app
Repo for the frond-end application (React): [https://github.com/lithesh2023/car-parking-booking-app-ui](https://github.com/lithesh2023/car-parking-booking-app-ui)

- Continues Integration (CI) – We have used Git Actions
- Continues Deployment (CD) - We have used Flux

**Git Actions(CI) : Workflow**
  
- Workflow code: [https://github.com/lithesh2023/car-parking-booking-app- ui/blob/main/.github/workflows/CI.yml](https://github.com/lithesh2023/car-parking-booking-app-%20ui/blob/main/.github/workflows/CI.yml)
- See the below screenshots for the same

<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/0e9f22fd-dc4b-45a1-889d-1262df614ac8">

<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/abd47469-e17d-4c61-a9b2-f77b857cda63">

<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/61541716-8dc3-453b-9b86-49e69bf6e107">

- Deployed the docker image to Docker hub through workflow
  
1. Docker Repo:
<img width="247" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/f8aa937f-60e8-4e13-a2d0-10828f99ce39">

**Flux (CD)**
We have used following repositories to automate the deployment to Kubernetes.
litheshp/car-parking-booking-app-react
 Repo Link: [https://hub.docker.com/repository/docker/litheshp/car-parking-booking-app-react/general](https://hub.docker.com/repository/docker/litheshp/car-parking-booking-app-react/general)
  
1. Application Repo as Source: [https://github.com/lithesh2023/car-parking-booking-app-ui](https://github.com/lithesh2023/car-parking-booking-app-ui)

   <img width="143" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/f556728e-3f84-4733-919d-ebdc2f531b5f">

2. Environmental Repo : [https://github.com/lithesh2023/flux-image-updates](https://github.com/lithesh2023/flux-image-updates)
   
   <img width="107" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/a720eb91-df9e-4093-ba84-2f661cf8fcf5">

**The steps used for Flux**
1. Bootstrap flux
   > flux bootstrap github --owner=$GITHUB_USER -—repository=car-parking-booking-env --branch=main --path=./clusters/my-cluster –personal!
3. Create source
   > flux create source git car-parking-booking-app-ui --url=https://github.com/lithesh2023/car-parking-booking-app-ui  -—branch=main --interval=1m --export > ./clusters/my-cluster/car-parking-booking-app-ui-source.yaml
5. Create kustomization
   > flux create kustomization car-parking-booking-app-ui --target-namespace=default --source=podinfo --path="./kustomize" --prune=true --wait=true --interval=30m --retry-interval=2m --health-check-timeout=3m --export > ./clusters/my-cluster/car-parking-booking-app-ui-kustomization.yaml
6. Created image policy and image registry for automatic deployment when the tag changed on docker image
 
See the below screenshots for flux system

1. Starting Minikube

   <img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/d84d1895-a2c8-474a-a0d0-f76808b83861">
   
3. Flux pre check

   <img width="300" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/16bda8ee-4e7c-4eed-ba89-1c60d3260a7e">
 
5. Flux reconciliation with source

   <img width="382" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/575e6e17-187f-4152-a79c-d238df712335">
   
7. All flux system

   <img width="979" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/755a4903-f3b5-44f6-b9a8-cc22c01bc4ce">
   
9. All Kubernetes details(deployment, service, replica,pods)

   <img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/14a1c65a-bcd3-472b-9d07-dc5a84096c82">
   
11. Access the UI app through tunnelling
 
    <img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/375aa937-1f23-48dd-8221-e4fb7fc31315">
 
## Database
### Migration module
Follow the steps in the readme file to create the databse and ralted tables.

Repo : [https://github.com/lithesh2023/parking-migration/tree/main](https://github.com/lithesh2023/parking-migration/tree/main)

### ER Diagram
![image](https://github.com/lithesh2023/ASR-CPBA/assets/138496677/98c78141-fe8f-4a21-8062-7b48256fe700)

##  UI Application
We have developed the UI application and integrated with the back-end microservices.
- UI Application: <img width="1123" alt="Screenshot 2023-09-11 at 5 26 39 PM" src="https://github.com/lithesh2023/ASR-CPBA/assets/16690487/109a48a2-185a-4204-a151-1c660168c0f2">

- Technology Used: React <br />
**UI Screenshots** <br />
  Sign Up <img width="1037" alt="Screenshot 2023-09-11 at 5 27 19 PM" src="https://github.com/lithesh2023/ASR-CPBA/assets/16690487/34b8289c-cac3-4389-b8fe-dc1d7aa80130">  <br />
  Log in <img width="1050" alt="Screenshot 2023-09-11 at 5 26 55 PM" src="https://github.com/lithesh2023/ASR-CPBA/assets/16690487/40414d6f-6881-44ab-84b4-7d435e04da63">  <br />
  My Vehicle <img width="1066" alt="Screenshot 2023-09-11 at 5 27 56 PM" src="https://github.com/lithesh2023/ASR-CPBA/assets/16690487/166c6837-95c9-41bb-a28c-cba922202a88">  <br />

## Microservices
### 1. User Profile Service
- Used for User registration, Authentication and Autherization. This is using Token based Authentication.
- User Profile Service: [https://github.com/lithesh2023/User_Profile_Service](https://github.com/lithesh2023/User_Profile_Service)
- Swagger end points for User profile service: [http://localhost:5000/api-docs/](http://localhost:5000/api-docs/)
- Database Used: Postgres SQL
- Technology Used: Nodejs with express
- CI/CD Pipeline :[https://github.com/lithesh2023/User_Profile_Service/actions/workflows/ci-cd.yml](https://github.com/lithesh2023/User_Profile_Service/actions/workflows/ci-cd.yml)

**Login/Signup Options**

   1. Application specific Login
 

**Screenshots**

<img width="1481" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/f6b4bbc5-089e-4704-a76b-83945ac18978">


<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/d6754a50-f6c9-4874-a841-0ba2271c18d5">
 
### 2. Payment Service
- Used for payment services for parking slot booking.
- User Profile Service: [https://github.com/lithesh2023/Payment_Service](https://github.com/lithesh2023/Payment_Service)
- Swagger end points for Payment service: [http://localhost:3000/docs/](http://localhost:3000/docs/)
- Database Used: Postgres SQL
- Technology Used: Next.js
- CI/CD Pipeline : [https://github.com/lithesh2023/Payment_Service/actions/workflows/CI_CD.yml](https://github.com/lithesh2023/Payment_Service/actions/workflows/CI_CD.yml)
  
 **Screenshots**
  
 <img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/ef323a5c-5791-4ba5-8e32-6b14e3108986">

### 3. Booking Service:

- Used for Booking related services. Booking parkig slot, Adding vehicle for user , Adding slots, Removing Vehicle, Delete Booking
- Booking Service: [https://github.com/lithesh2023/Booking_Service](https://github.com/lithesh2023/Booking_Service)
- End points for Booking Service:
  
  <img width="294" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/dfd78b28-ccf7-4194-bdc9-5ddbe281496b">
- Database Used: Postgres SQL
- Technology Used: Node.js
- CI/CD Pipeline : [https://github.com/lithesh2023/Booking_Service/actions/workflows/CI_CD.yml](https://github.com/lithesh2023/Booking_Service/actions/workflows/CI_CD.yml)


  
