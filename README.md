This repository acts as a knowledge base related to the RADON methodology, containing an overview and links of the RADON architecture, tools, actors and methodology.

# Table of Contents
* [RADON Architecture](#architecture)
* [RADON Actors and Stakeholders](#radon-actors-and-stakeholders)
* [RADON Methodology](#radon-methodology)
* [RADON Tools](#radon-tools)

# Architecture

The RADON framework provides a set of components that realize a set of tools, modules and services covering both the design and runtime phases of microservices and serverless-oriented application development and deployment.

## Architecture Diagram

![#radon-architecture](RADON-Architecture.png)


## Architecture Overview

The Architecture Diagram depicts the connections among the RADON components. The design time components interact with each other and with the runtime components in order to design, prototype, deploy and test applications built on serverless FaaS.

In this context a particular role is played by the RADON IDE. This component is be based on [Eclipse Che](#https://www.eclipse.org/che/) and provides a multi-user development environment to access the RADON artifacts. Indeed, as depicted in the Architecture diagram, the RADON IDE interacts also with the Template Library. This is done to access the reusable base types, abstractions and TOSCA extensions and make them available to the RADON tools (see Section 2.2), that require them to model a RADON application. Moreover, the RADON IDE  acts as the front-end of the RADON methodology, by enabling users to invoke RADON tools supporting both the design and runtime phases of application development.

# RADON Actors and Stakeholders



# RADON Methodology

# RADON Tools

## Defect Prediction Tool
### Overview
### Link 
### Sequence and Activity Diagrams
### Move to RADON Repository?

## Decomposition Tool
### Overview
### Link 
### Sequence and Activity Diagrams

## CDL and Verification Tool
### Overview
### Link 
### Sequence and Activity Diagrams

## Continuous Testing Tool
### Overview
### Link 
### Sequence and Activity Diagrams

## Orchestrator
### Overview
### Link 
### Sequence and Activity Diagrams

## Data Pipeline Plugins
### Overview
### Link 
### Sequence and Activity Diagrams

## Integrated Development Environment
### Overview
### Link 
### Sequence and Activity Diagrams

## Template Library
### Overview
### Link 
### Sequence and Activity Diagrams

## Graphical Modeling Tool (winery extension)
### Overview
### Link 
### Sequence and Activity Diagrams

## Monitoring System
### Overview
### Link 
### Sequence and Activity Diagrams

