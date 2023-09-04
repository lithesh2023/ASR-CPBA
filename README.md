# ASR-CPBA
Website for ASR Car Parking Booking Application

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
**SearchandCompare**-Forusers,theonlinesystemoffersaconvenient way to search for available parking slots, Compare the slots based upon the features like, floor, distance from entry/exit gate etc.
**Booking**-Booktheparkinginadvance(maximum2daysadvance)and navigate to the designated spot using integrated navigation features. Users can also make cashless payments for parking fees through secure online transactions, eliminating the need for physical tickets and reducing waiting times.
**History–Bookinghistory**,
ParkingManagement(AddParkingslots/pricing/billing–admin features)
Integratedrivingdirection(O)
IntegrationwithChatsystem
IntegrationwithIoT(O)
## Intended Audience
### Following are the intended audiences for the system –
1. CarOwners(Registered/Unregisteredusers) 2. Admin
- MallOwner(O)
- Malladministrator
- Mall supervisor
Business Context
**Stakeholders**
1. Client
2. Product Owner (PO)
3. Application Architect
4. FSE developers
5. Data Base Architect
6. QA Testers
**Business Goals**
### Following are the intended business goals the Car Parking Booking application is planning to address -
1. Reduce parking congestion.
3. Delays trying to find a Parking Spot
4. Lack of Structured Parking due to unavailability of knowledge of empty Parking Spaces
5. Wastage of Fuel and Time resulting in some form of personal loss
6. Ease of Payment

## Constraints



Context
4. Wastage of Fuel and Time resulting in some form of personal loss
5. Ease of Payment
Architecturally Significant Requirements
                    Need to get an confirmation from Stack Route team about the availability of the licenses Based upon the ROI projection, we can decide the investments
        
## Quality Attribute Requirements
   

## Influential Functional Requirements

1. Payment gateway
2. Chat application external
3. History

## Context Diagram
  <img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/4c8f9a00-1c86-49d7-b060-44d7d2b9bc48">

## Component Diagram
  
<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/e018d1de-5928-4490-a7fb-689b9d113a27">

## Container Diagram
<img width="452" alt="image" src="https://github.com/lithesh2023/ASR-CPBA/assets/138496677/2fca5f07-4262-4cad-a898-0fc4b5cebcdb">


## Branching Strategy
We are opting for Trunk Based branching (development) Strategy. This involves developers integrating their changes directly into a shared trunk (master) at least once a day. This shared trunk is always in a releasable state. Developers can pull from this trunk, create a local repository, and then push the code to the shared trunk.
This regular integration enables developers to view each other’s changes quickly and immediately react if there are any conflicts.

 Following are a few advantages for using TBD strategy –
- One of the most preferred branching strategies used for a microservice architecture. This is a fast workflow with minimal merging.
- True continuous integration as developers constantly keeps the trunk updated.
- Excellent choice for CI/CD pipelines with simpler workflows for automated testing
- Shorter feedback loops for developers as code changes are quickly visible.
- Lead to faster release cycles
- Smaller iterations allow teams to keep track of all the changes while reducing code conflicts and improving overall code quality.
## CICD pipeline
We have implemented CICD pipeline for our front-end app
Repo for the frond-end application (React): https://github.com/lithesh2023/car-parking-
### booking-app-ui
- Continues Integration (CI) – We have used Git Actions
- Continues Deployment (CD) - We have used Flux
### Git Actions(CI) : Workflow
  
- Workflow code: https://github.com/lithesh2023/car-parking-booking-app- ui/blob/main/.github/workflows/CI.yml
- See the below screenshots for the same
- Deployed the docker image to Docker hub through workflow 1. Docker Repo:

### Flux-CD
We have used following repositories to automate the deployment to Kubernetes.
litheshp/car-parking-booking-app-react
 Repo Link: https://hub.docker.com/repository/docker/litheshp/car-parking-booking-app-react/general
  
1. Application Repo as Source: https://github.com/lithesh2023/car-parking-booking-app- ui
  2. Environmental Repo : https://github.com/lithesh2023/flux-image- updates/tree/main/clusters/my-cluster
The steps used for Flux
1. Bootstrap flux
=$GITHUB_USER parking-booking-env     =   =
personal
2. Create source
3. Create kustomization
=car-
    flux bootstrap github --owner
--branch
main --path
-—repository
./clusters/my-cluster –
  flux create source git car-parking-booking-app-ui -- url=https://github.com/lithesh2023/car-parking-booking-app-ui -— branch=main --interval=1m --export > ./clusters/my-cluster/car- parking-booking-app-ui-source.yaml
  flux create kustomization car-parking-booking-app-ui --target-
   namespace
= =true
default --source
=
podinfo --path
     prune
--wait
=true =
--interval
=
30m --retry-interval
2m --
  health-check-timeout
3m --export > ./clusters/my-cluster/car-
 parking-booking-app-ui-kustomization.yaml
4. Created image policy and image registry for automatic deployment when the tag changed on docker image
See the below screenshots for flux system
1. Starting Minikube
="./kustomize" --
             =

 2. Flux pre check
3. Flux reconciliation with source
  4. All flux system
 
5. All Kubernetes details(deployment, service, replica,pods)
 6. Access the UI app through tunnelling
UI Application
We have developed few screens for the UI application.
• UI Application: https://github.com/lithesh2023/car-parking-booking-app-ui
• Technology Used: React
UI Screenshots
   
  User Profile Service
• User Profile Service: https://github.com/lithesh2023/User_Profile_Service
• Swagger end points for User profile service: http://localhost:5000/api-docs/
• Database Used: Mongodb
• Technology Used: Nodejs with express
  
Login/Signup Options
1. Application specific Login
2. Facebook Authentication
3. Google Authentication
Screenshots
 User Schema
 
Payment Service
• User Profile Service: https://github.com/lithesh2023/Payment_Service
• Swagger end points for User profile service: http://localhost:3000/docs/
• Database Used: TBD
• Technology Used: Next.js
Screenshots
   Booking Service
• Booking Service: https://github.com/lithesh2023/Booking_Service
• Swagger end points for User profile service: TBD
• Database Used: TBD
• Technology Used: Next.js
Report Service
• Report Service: https://github.com/lithesh2023/Report_Service
• Swagger end points for User profile service: TBD
• Database Used: TBD
• Technology Used: TBD
  
Parking Management
• Parking Management Service: https://github.com/lithesh2023/Parking_Management
• Swagger end points for User profile service: TBD
• Database Used: TBD
• Technology Used: TBD
Navigation Service
• Navigation Service: https://github.com/lithesh2023/Navigation_Service
• Swagger end points for User profile service: TBD
• Database Used: TBD
• Technology Used: TBD
  
