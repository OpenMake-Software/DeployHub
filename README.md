# Ortelius
Welcome to Ortelius. Ortelius is an open source project that aims to simplify the implementation of microservices. By providing a central catalog of services with their deployment specs, application teams can easily consume and deploy services across cluster. Ortelius tracks application versions based on service updates and maps their service dependencies eliminating confusion and guess work.  Unique to Ortelius is the ability to track your microservice inventory across clusters mapping the differences.  Ortelius serves Site Reliability Engineers and Cloud Architects in their migration to and ongoing management of a microservice implementation.

## Ortelius Goals
The goals of the Ortelius Open Source Project are: 

1) Simplify deployment automation across the life cycle in traditional, hybrid and microservice environments.
2) Allow organizations to achieve business agility by providing a clear path for fast and safe incremental releases with impact analysis and feedback loops. 
3) Give developers the power to control how their software is released across all environments by defining deployment configurations data that is separate from the definition.   
4) Deliver transparency into the deployment process by mapping component and microservice relationships with BOM and Difference Reports across deployed environments (clusters, cloud, physical).  
5) Establish a market place to share microservices with their deployment requirements and versions.

## Open Source Sub-Committees

### CD Environment - Development Infrastructure and Productivity

Create a CD process for managing pull requests, builds, tests and releases.  

Contributors:
- Anand Bhagwat
- Steve Taylor
- Sanjay Sheel

### Data Science and Visualization

Determine what reports and maps can currently be created and/or enhanced.  Begin looking at what data can be passed back to the CD pipelines for predictive reporting, risk assessment. (Think truth tables).

Contributors:
- Tracy Ragan

### Deployment Integrations

Create integrations with documentation and videos for the following CI/CD Solutions:

- Jenkins: 90% work completed
- Jenkins X
- Screwdriver
- Tekton (Tekton Catalog)
- Spinnaker
- Argo

Contributors:
- Steve Taylor

### Market Place and Domains

Enhance the current Domain structure to make it more like a Marketplace for sharing Microservices.  Think API marketplace.

Contributors:
- Christopher Hicks
- Steve Taylor
- Ayesha Khaliq

### UX and Testing

Review User Interface and make recommendations for improving with a focus on ease of use. Define test cases with automation.

Contributors:
- Tracy Ragan
- Parijat Kalita

### Documentation

Review documentation and re-write or clarify complexities.

Contributors:
- Tracy Ragan
- Divya Mohan

### Architecture

Work to begin breaking down the monolithic into services. Starting with logging as a good first step. Integration with Istio with Routing. Solving onboarding efforts (AWS scraping for existing microservice customers)

Contributors:
- Christopher Hicks
- Steve Taylor
- Ayesha Khaliq

### Development

Work on existing enhancements and bug fixes. Add them to the core Ortelius repository unless a doc change.

Contributors:
- Steve Taylor

### Product Management

- Website, branding, outreach 
- Review messaging, update logo, work on blogs. 
- Personas, Journey Maps, service maps, roadmaps, Value Canvas, Go-to-Market strategies, product metrics. 
- What problem or opportunity is being explored?
- How is the solution being framed to tackle this?
- What is being measured to determine if this is successful?
- Who are the people that this solution serves?
- How are they being informed about it?
- How are they learning to actually use or benefit from it?
- How are they involved in collaborating on the solution with us?
- What is the experience like for new collaborators getting started?
- How does the solution fit with both the immediate and wider ecosystem?
- Are there any roadblocks that can be removed in how we operate?
- What additional resources could be made available? Where would those resources help most?
- Where is the documentation being maintained on the project?
- Do we understand accessibility requirements? Are we meeting them?

Contributors:
- Tracy Ragan
- Neetu Jain
- Divya Mohan

## Project Management

Track progress, define process, work with Steve and Marky managing pull requests and releases dates.

Contributors: 
-Tracy Ragan
-Neetu Jain

## Ortelius as a SaaS option.
DeployHub Team is a hosted version of Ortelius. [Sign-up and use for free.](https://www.deployhub.com/free-team-sign-up/) 

## Ortelius On-Prem Installation
Ortelius on-prem runs as docker container.  In order to install it you need to have docker up and running.

### Docker Installation
#### [Docker for Windows](https://docs.docker.com/docker-for-windows/install/)
Requires Microsoft Windows 10 Professional or Enterprise 64-bit

#### [Docker for CentOS](https://docs.docker.com/install/linux/docker-ce/centos/)
Requires CentOS 64-bit 7.1 and higher on x86_64

#### [Docker for RedHat](https://docs.docker.com/install/linux/docker-ee/rhel/)
Require RHEL 64-bit 7.1 and higher on x86_64, s390x, or ppc64le (not ppc64).

#### [Docker for Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
Requires 64-bit version of one of these Ubuntu versions:
* Bionic 18.04 (LTS)
* Artful 17.10
* Xenial 16.04 (LTS)
* Trusty 14.04 (LTS)

#### [Docker for OS/X](https://docs.docker.com/docker-for-mac/install/)
Requires macOS El Capitan 10.11 and newer macOS releases are supported. We recommend upgrading to the latest version of macOS.

### [Test your Docker Install](https://docs.docker.com/get-started/#test-docker-installation)

#### Ortelius Image Pull
```
docker pull quay.io/ortelius/ortelius
```
### Ortelius Quick Start Guide
```
docker pull quay.io/ortelius/ortelius:latest
mkdir -p ~/ortelius/data
chmod 777 ~/ortelius/data
docker run -v ~/ortelius/data:/var/lib/pgsql/data:Z -p 7171:8080 -d --hostname docker_dh -v ~/.ssh:/keys:Z ${IMAGE_ID_OF_ortelius}
```
e.g.
```
docker run -v ~/ortelius/data:/var/lib/pgsql/data:Z -p 7171:8080 -d --hostname docker_dh -v ~/.ssh:/keys:Z IMAGE_ID
```
### Accessing Ortelius Homepage:
Homepage URL : http://localhost:7171/dmadminweb/Home

Login Credentials:

Admin Username: admin

Admin Password: admin

## Support

https://github.com/ortelius/ortelius/issues

