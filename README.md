This repository acts as a knowledge base related to the RADON methodology, containing an overview and links to the RADON architecture, tools, actors and methodology.

Please check out the [RADON YouTube channel](https://www.youtube.com/channel/UCgoXX6JZ6bDqTxVBRm4KWnQ/videos) for videos!

# Table of Contents
* [RADON Architecture](#radon-architecture)
* [RADON Actors and Stakeholders](#radon-actors-and-stakeholders)
* [RADON Methodology](#radon-methodology)
* [RADON Tools](#radon-tools)

# RADON Architecture

The RADON framework provides a set of components that realize a set of tools, modules and services covering both the design and runtime phases of microservices and serverless-oriented application development and deployment.

![#radon-architecture](RADON-Architecture.png)

The Architecture Diagram depicts the connections among the RADON components. The design time components interact with each other and with the runtime components in order to design, prototype, deploy and test applications built on serverless FaaS. Such interaction(s) are defined by the [RADON Workflows](#radon-methodology) in the context of  the RADON methodology.

In this context a particular role is played by the RADON IDE. This component is be based on [Eclipse Che](#https://www.eclipse.org/che/) and provides a multi-user development environment to access the RADON artifacts. Indeed, as depicted in the Architecture diagram, the RADON IDE interacts also with the Template Library. This is done to access the reusable base types, abstractions and TOSCA extensions and make them available to the RADON tools (see Section 2.2), that require them to model a RADON application. Moreover, the RADON IDE  acts as the front-end of the RADON methodology, by enabling users to invoke RADON tools supporting both the design and runtime phases of application development.

For more information on the RADON Architecture, please refer to the deliverable document 
[D2.3 – Architecture & Integration Plan I](http://radon-h2020.eu/wp-content/uploads/2019/11/D2-3_Architecture-and-integration-plan-I.pdf)

# RADON Actors and Stakeholders

RADON intends to deliver a DevOps-inspired methodology. On that basis, RADON proposes to identify a few reference DevOps actors. A RADON actor defines a role -- not a single human or software -- therefore the same person can potentially act as multiple RADON actors and the same role could be split across multiple actors. The RADON actors are as follows:

* Software Designer: this actor is responsible of the application architecture and data lifecycle design.
* Software Developer (Dev): responsible for business logic coding and testing.
* Operations Engineer (Ops): responsible for delivery on the infrastructure and infrastructure testing.
* QoS Engineer: responsibility for ensuring performance/reliability/security/privacy/access control properties of the application,
* Release Manager: team leader that authorizes major changes and their release to production.

For more information on RADON actors, please refer to the deliverable document [D2.1 - Initial Requirements and Baselines](http://radon-h2020.eu/wp-content/uploads/2019/07/D2.1-Initial-requirements-and-baselines.pdf)

# RADON Methodology

The RADON DevOps methodology consolidates the user workflow for using RADON tools and the DevOps paradigm for software delivery and evolution. In the context of a DevOps lifecycle, we have defined several workflows as abstractions to organize and present the possible interactions of the different tools within the RADON framework and with the identified actors. DevOps actors as described above are fundamental to reason about the existing development and operations roles and re-assign them for the continuous delivery of software in the context of RADON. 

Furthermore, the defined workflows help understand and further refine the application development lifecycle with the RADON framework, considered as an iterative process involving Design, Development (Deployment) and Runtime.  The defined workflows will be described below.

# RADON Tools

## Defect Prediction Tool

| Items | Contents | 
| --- | --- |
| **Short Description** | The Defect Prediction tool  focuses on Infrastructure-as-Code (IaC) correctness. Recall that IaC is machine-readable code that manages and provisions infrastructure -- e.g., TOSCA or Ansible YAML files. The defect prediction tool helps RADON users to find suspicious defective Infrastructure-as-Code (IaC) scripts enabling DevOps operators to focus on such critical scripts before deployment and during Quality Assurance activities. | 
| **Documentation** | WIP -- [D2.3 – Architecture & Integration Plan I](http://radon-h2020.eu/wp-content/uploads/2019/11/D2-3_Architecture-and-integration-plan-I.pdf) |
| **Stand-Alone Tutorial** | WIP | 
| **Video**| WIP |
| **Repository** |[APIs](https://github.com/radon-h2020/radon-defect-prediction-api); [Web Application](https://github.com/radon-h2020/radon-defect-prediction-web) |
| **Licence**| Apache License, Version 2.0 |
| **Contact**| <ul><li>Damian A. Tamburri (d.a.tamburri@tue.nl)</li><li>Stefano Dalla Palma (s.dalla.palma@jads.nl)</li></ul> |

## Decomposition Tool


| Items | Contents | 
| --- | --- |
| **Short Description** | The decomposition tool is present to help RADON users in finding the optimal decomposition solution for an application based on the microservices architectural style and the serverless FaaS paradigm. It supports three typical usage scenarios: (1) architecture decomposition, (2) deployment optimization, (3) accuracy enhancement. | 
| **Documentation** | WIP |
| **Stand-Alone Tutorial** | WIP | 
| **Video**| WIP |
| **Repository** | WIP |
| **Licence**| License |
| **Contact**| <ul><li>Lulai Zhu ([@zhululai](https://github.com/zhululai))</li><li>Giuliano Casale ([@gcasale](https://github.com/gcasale))</li></ul> |


## Constraint Definition Language and Verification Tool

| Items | Contents | 
| --- | --- |
| **Short Description** | The Verification Tool (VT) provides the functionality for verifying that the current RADON model conforms to the CDL specification defined by the CDL tool. The VT will be available as a plugin in the IDE, and will be supported by a “VT backend”, which will run in a container. In cases where the current RADON model does not conform to the CDL specification, the VT can be used to suggest corrections to the model. If the model does conform, the VT can be used to suggest improvements to it with respect to the preferences expressed as soft constraints in the CDL specification. The VT can also be used to find an optimal (preferred) completion of a partial RADON model, with respect to the CDL specification, and to learn new constraints for the CDL. | 
| **Documentation** | http://radon-h2020.eu/wp-content/uploads/2020/01/D4.1-Constraint-definition-language-I.pdf |
| **Stand-Alone Tutorial** | https://radon-vt-documentation.readthedocs.io/ | 
| **Video**| https://youtu.be/pJWetOzY2Zc |
| **Repository** | WIP |
| **Licence**| Please fill in this form to request a license: https://imperial.eu.qualtrics.com/jfe/form/SV_1HthWM3xILQM6ih |
| **Contact**| <ul><li>Mark Law (mark.law09@imperial.ac.uk)</li><li>Alessandra Russo (a.russo@imperial.ac.uk)</li></ul> |

## Continuous Testing Tool

| Items | Contents |
| --- | --- |
| **Short Description** | The Continuous Testing Tool (CTT) provides the functionality for defining, generating, executing, and refining continuous tests of application functions, data pipelines and microservices, as well as for reporting test results. While targeting to provide a general framework for continuous quality testing in RADON, a particular focus of CTT is on testing workload-related quality attributes such as performance, elasticity, and resource/cost efficiency.  |
| **Documentation** | [D2.3 – Architecture & Integration Plan I](http://radon-h2020.eu/wp-content/uploads/2019/11/D2-3_Architecture-and-integration-plan-I.pdf) |
| **Stand-Alone Tutorial** | https://continuous-testing-tool.readthedocs.io/ |
| **Video**| https://youtu.be/35VN2edyvsc |
| **Source code** | <ul><li>https://github.com/radon-h2020/radon-ctt (CTT Server)</li><li>https://github.com/radon-h2020/radon-ctt-agent (CTT Agent)</li><li>https://github.com/radon-h2020/radon-particles (Includes CTT-related types)</li></ul> |
| **Licence**| [Apache License, Version 2.0](https://opensource.org/licenses/Apache-2.0) |
| **Contact**| <ul><li>Thomas F. Düllmann ([@duelle](https://github.com/duelle)) </li><li>Andre van Hoorn ([@avanhoorn](https://github.com/avanhoorn)) </li></ul> |

## Orchestrator

| Items | Contents | 
| --- | --- |
| **Short Description** | The orchestrator puts the application into the runtime environment, enforcing the state described by application blueprint (CSAR) onto the targeted provider(s). The common operations are deployment, scaling and cleanup or un-deploy and are executed on different target environment as staging, development and production.  | 
| **Documentation** | https://xlab-si.github.io/xopera-docs/ |
| **Stand-Alone Tutorial** | https://xlab-si.github.io/xopera-docs/examples.html | 
| **Video**| https://www.youtube.com/watch?v=cb1efi3wnpw |
| **Repository** | https://github.com/radon-h2020/xopera-opera |
| **Licence**|  [Apache License, Version 2.0](https://github.com/radon-h2020/xopera-opera/blob/master/LICENSE) |
| **Contact**| <ul><li>Matija Cankar ([@cankarm](https://github.com/cankarm))</li></ul> |

## Data Pipeline Plugins

| Items | Contents | 
| --- | --- |
| **Short Description** | A module that extends the orchestrator with the capability to control the life cycle of data pipelines, introducing the ability to automate the movement and transformation of data.| 
| **Documentation** | WIP, [D5.5: Data Pipeline Orchestration I](http://radon-h2020.eu/wp-content/uploads/2020/01/D5.5-Data-Pipeline-Orchestration-I.pdf) |
| **Stand-Alone Tutorial** | WIP, [RADON Toy example-datapipeline demo](https://github.com/radon-h2020/demo-lambda-thumbgen-tosca-datapipeline) | 
| **Video**| WIP |
| **Repository** | WIP |
| **Licence**| [Apache License, Version 2.0](https://opensource.org/licenses/Apache-2.0) |
| **Contact**| <ul><li>Chinmaya Dehury [chinmaya.dehury@ut.ee](chinmaya.dehury@ut.ee)</li><li>Pelle Jakovits [pelle.jakovitsh@ut.ee](pelle.jakovitsh@ut.ee)</li><li>Satish Srirama [Satish Srirama](satish.srirama@ut.ee)</li></ul> |

## Integrated Development Environment

| Items | Contents | 
| --- | --- |
| **Short Description** | The RADON IDE is based on Eclipse Che, and provides standard functionalities to support development activities (e.g. debugging functionalities and error checking capabilities) along with specific functionalities to achieve the RADON needs. It provides a shared space where different teams can access the RADON artifacts according to their authorizations and an access point for the interactions with the tools involved in the RADON architecture. | 
| **Documentation** | WIP |
| **Stand-Alone Tutorial** | WIP | 
| **Video**| WIP |
| **Repository** | WIP |
| **Licence**| License |
| **Contact**| <ul><li>Stefania D'Agostini (stefania.dagostini@eng.it)</li></ul> |

## Template Library

| Items | Contents | 
| --- | --- |
| **Short Description** | The template library is a repository of application runtime management definitions including the blueprints, high-level system abstractions, application abstractions (including data pipeline components) and TOSCA language extensions. One of the specific parts of Template Library is the FaaS abstraction layer that holds the definitions required to deploy a particular application component to different cloud providers. | 
| **Documentation** | WIP |
| **Stand-Alone Tutorial** | WIP | 
| **Video**| WIP |
| **Repository** | WIP |
| **Licence**| License |
| **Contact**| <ul><li>Matija Cankar ([@cankarm](https://github.com/cankarm))</li></ul>  |

## Graphical Modeling Tool (Eclipse Winery)

| Items | Contents | 
| --- | --- |
| **Short Description** | The Graphical Modeling Tool (GMT) is developed based on Eclipse Winery, which is a web-based environment to graphically model TOSCA-based application topologies. It includes (i) a component to manage TOSCA types and templates, (ii) a Topology Modeler that enables to graphically compose application topologies and specify configuration properties, and (iii) a file-based backend to store, import, and export TOSCA entities. | 
| **Documentation** | [User Guide](https://eclipse-winery.readthedocs.io/) / RADON Deliverables: [D4.5](http://radon-h2020.eu/wp-content/uploads/2020/01/D4.5-Graphical-Modelling-Tools.pdf), [D4.3](http://radon-h2020.eu/wp-content/uploads/2019/11/D4.3-RADON-Models-I.pdf) |
| **Stand-Alone Tutorial** | [Getting Started](https://eclipse-winery.readthedocs.io/en/latest/user/getting-started.html)  | 
| **Video**| [Link](https://youtu.be/xEjarBWcdK0?t=81) |
| **Repository** | <https://github.com/radon-h2020/winery> (fork) / <https://github.com/eclipse/winery> |
| **Licence**| Dual licensed under the Apache License 2.0 and Eclipse Public License 2.0. |
| **Contact**| <ul><li>Michael Wurster (@miwurster, wurster@iaas.uni-stuttgart.de)</li><li>Vladimir Yussupov (yussupov@iaas.uni-stuttgart.de)</li></ul> |

## Delivery Toolchain

| Items | Contents | 
| --- | --- |
| **Short Description** | The delivery toolchain is a set of tools configured at one place with one goal - to deliver the application to the production site. To achieve the final step, delivery, with a success, a set of previous steps needs to be successfully accomplished. Delivery toolchain provides the single point of configuration management including CI/CD, monitoring and orchestration. | 
| **Documentation** |  RADON Deliverables [D5.1](http://radon-h2020.eu/wp-content/uploads/2020/01/D5.1-Runtime-Environment-1.pdf) |
| **Stand-Alone Tutorial** | WIP | 
| **Video**| WIP |
| **Repository** | WIP |
| **Licence**|  Apache License, Version 2.0 |
| **Contact**| <ul><li>Matija Cankar ([@cankarm](https://github.com/cankarm))</li></ul> |
