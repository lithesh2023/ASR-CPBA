# ASR-CPBA
ASR for Car Parking Booking Application

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

### Following are the scope of the application :-
- **Search and Compare**-Forusers,theonlinesystemoffersaconvenient way to search for available parking slots, Compare the slots based upon the features like, floor, distance from entry/exit gate etc.

- **Booking**-Booktheparkinginadvance(maximum2daysadvance)and navigate to the designated spot using integrated navigation features. Users can also make cashless payments for parking fees through secure online transactions, eliminating the need for physical tickets and reducing waiting times.
- **History** –Booking history,
- **ParkingManagement(AddParkingslots/pricing/billing–admin features)**
- **Integratedrivingdirection(O)**
- **IntegrationwithChatsystem**
- **IntegrationwithIoT(O)**

## Intended Audience
### Following are the intended audiences for the system –
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
### Following are the intended business goals the Car Parking Booking application is planning to address -
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

## Context Diagram
  <img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/4c8f9a00-1c86-49d7-b060-44d7d2b9bc48">

## Component Diagram
  
<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/e018d1de-5928-4490-a7fb-689b9d113a27"><img width="128" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/39d58ee4-7220-460e-ad45-15bac43066f9">


## Container Diagram
<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/2fca5f07-4262-4cad-a898-0fc4b5cebcdb">


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

### Git Actions(CI) : Workflow
  
- Workflow code: [https://github.com/lithesh2023/car-parking-booking-app- ui/blob/main/.github/workflows/CI.yml](https://github.com/lithesh2023/car-parking-booking-app-%20ui/blob/main/.github/workflows/CI.yml)
- See the below screenshots for the same

<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/0e9f22fd-dc4b-45a1-889d-1262df614ac8">

<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/abd47469-e17d-4c61-a9b2-f77b857cda63">

<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/61541716-8dc3-453b-9b86-49e69bf6e107">

- Deployed the docker image to Docker hub through workflow
  
1. Docker Repo:
<img width="247" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/f8aa937f-60e8-4e13-a2d0-10828f99ce39">

### Flux-CD
We have used following repositories to automate the deployment to Kubernetes.
litheshp/car-parking-booking-app-react
 Repo Link: [https://hub.docker.com/repository/docker/litheshp/car-parking-booking-app-react/general](https://hub.docker.com/repository/docker/litheshp/car-parking-booking-app-react/general)
  
1. Application Repo as Source: [https://github.com/lithesh2023/car-parking-booking-app-ui](https://github.com/lithesh2023/car-parking-booking-app-ui)

   <img width="143" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/f556728e-3f84-4733-919d-ebdc2f531b5f">

2. Environmental Repo : [https://github.com/lithesh2023/flux-image- updates/tree/main/clusters/my-cluster](https://github.com/lithesh2023/flux-image-%20updates/tree/main/clusters/my-cluster)
   
   <img width="107" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/a720eb91-df9e-4093-ba84-2f661cf8fcf5">

### The steps used for Flux
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
 
## Database ER Diagram
 ![image](https://github.com/lithesh2023/ASR-CPBA/assets/138496677/eb1d5379-e7b6-4e9e-b181-922e420ddba6)

###  UI Application
We have developed few screens for the UI application.
- UI Application: [https://github.com/lithesh2023/car-parking-booking-app-ui](https://github.com/lithesh2023/car-parking-booking-app-ui)
- Technology Used: React
### UI Screenshots
   <img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/10f684de-eae6-4560-a157-3373294f049b">
   <img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/9e774891-2443-49e7-a120-410ce0e60b53">
   <img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/6a33a140-1652-4cdf-b38c-467339e4b1ea">


### User Profile Service
-  User Profile Service: [https://github.com/lithesh2023/User_Profile_Service](https://github.com/lithesh2023/User_Profile_Service)
-  Swagger end points for User profile service: [http://localhost:5000/api-docs/](http://localhost:5000/api-docs/)
- Database Used: Mongodb
- Technology Used: Nodejs with express
  
### Login/Signup Options

1. Application specific Login
2. Facebook Authentication
3. Google Authentication

**Screenshots**
<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/ac4a0063-f198-4ff5-b83d-5db176760007">
<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/d6754a50-f6c9-4874-a841-0ba2271c18d5">
 
### Payment Service
- User Profile Service: [https://github.com/lithesh2023/Payment_Service](https://github.com/lithesh2023/Payment_Service)
- Swagger end points for User profile service: [http://localhost:3000/docs/](http://localhost:3000/docs/)
- Database Used: TBD
- Technology Used: Next.js

 **Screenshots**
 <img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/ef323a5c-5791-4ba5-8e32-6b14e3108986">


- Booking Service: [https://github.com/lithesh2023/Booking_Service](https://github.com/lithesh2023/Booking_Service)
- Swagger end points for User profile service: TBD
- Database Used: TBD
- Technology Used: Next.js
  
### Report Service
- Report Service: [https://github.com/lithesh2023/Report_Service](https://github.com/lithesh2023/Report_Service)
- Swagger end points for User profile service: TBD
- Database Used: TBD
- Technology Used: TBD

###  Parking Management
- Parking Management Service: [https://github.com/lithesh2023/Parking_Management](https://github.com/lithesh2023/Parking_Management)
- Swagger end points for User profile service: TBD
- Database Used: TBD
- Technology Used: TBD
  
###  Navigation Service
- Navigation Service: [https://github.com/lithesh2023/Navigation_Service](https://github.com/lithesh2023/Navigation_Service)
- Swagger end points for User profile service: TBD
- Database Used: TBD
- Technology Used: TBD


  
