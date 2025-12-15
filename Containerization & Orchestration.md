Containerization & Orchestration
1️⃣ Docker

Emti (What):
Oka app ni “small box” lo pack cheyadam. A box lo app ki kavalsina software, libraries anni untai.

Enduku Use Cheyali (Why):
App eppudu, ekkada run chesina same ga work avvali. Local machine lo test chesina app, server lo deploy chesinappudu kuda exactly same ga run avvali.

Ela Use Chestharu (How):

Dockerfile create chesi app instructions rayadam

docker build → app ni image ga convert cheyadam

Image ni central storage (Docker Hub / GHCR / AWS ECR) ki push cheyadam

Pull chesi staging/prod lo deploy cheyadam

Container run chesi app use cheyadam

Epudu Use Cheyali (When):
Build → Test → Deploy stages lo, app environment consistent ga undali ante.

Ekkada Use Cheyali (Where):
Local dev machine, CI/CD pipeline, cloud or on-prem servers

Docker – How It Works (Step-by-Step)

Dockerfile Create → Image Build

Dockerfile lo app ki kavalsina OS, libraries, dependencies, configuration define chestharu

Example: Ubuntu base + Python + app code

docker build → Image Creation

Docker command run chesi image ready chestharu

Image = ready-to-run app box

Push Image → Registry (Docker Hub / GHCR / AWS ECR)

Central registry lo versioned images store chestharu

Example: v1.0, v1.1

Pull Image → Staging / Production Deployment

CI/CD pipeline image pull chesi deploy chestundi

Same image eppudu, ekkada deploy chesina exact ga work avuthundi

Run Container → Isolated App Instance

Container lo app separate environment lo run avuthundi

Filesystem, libraries, dependencies container lo matrame untai, host system ki effect ledu

Tip:

Minimal base images use cheyandi → size thakkuva, faster deployment

2️⃣ Kubernetes

Emti (What):
Multiple Docker boxes (containers) ni manage cheyadaniki tool.

Enduku Use Cheyali (Why):

Auto scale cheyadam (demand ekkuva aithe extra containers start)

Rollback (new version lo problem ayithe previous version ki revert)

Zero downtime deploy (users ki problem raakunda app update cheyadam)

Ela Use Chestharu (How):

Deployment manifest / Helm chart prepare cheyadam

CI/CD pipeline → kubectl apply → deploy containers

Monitor chesi pods crash ayite auto restart

Scale cheyadam → manual lekunda auto

Epudu Use Cheyali (When):
App multiple containers lo untundante, microservices use chesthe

Ekkada Use Cheyali (Where):
Cloud (AWS/GCP/Azure) or on-prem Kubernetes cluster

Kubernetes – How It Works (Step-by-Step)

Deployment Manifest / Helm Chart Create

App ki kavalsina containers, replicas, networking, volume info define chestharu

Example: deployment.yaml lo app name, image, replicas, ports rayadam

CI/CD Pipeline → kubectl apply / Helm Deploy

Pipeline lo command run chesthu containers cluster lo deploy avuthai

Example: kubectl apply -f deployment.yaml

Monitor & Auto-Restart

Kubernetes pod crash ayithe auto restart chestundi

Health check probes → app status monitor

Auto-Scaling

Demand ekkuva aithe extra pods create

Load thakkuva aithe pods reduce → cost & performance optimize

Rollback / Version Management

New version lo problem vaste previous stable version ki revert

Example: kubectl rollout undo deployment <app>

Tip:

Small deployment units (microservices) use cheyandi → easier management

3️⃣ Container Registry

Emti (What):
Docker images ni store cheyadaniki central place

Enduku Use Cheyali (Why):
Version control, staging/prod lo deploy cheyali ante easy pull cheyadaniki

Ela Use Chestharu (How):

Image tag → docker push → registry

Pull → docker pull

Deploy → staging/prod

Epudu Use Cheyali (When):
App build ayyaka, deploy mundu

Ekkada Use Cheyali (Where):
Docker Hub, GHCR, AWS ECR

4️⃣ Real-Time Daily CI/CD Workflow (Containers & Orchestration)

What:

Developer → code rayi → Docker image create → push registry

QA → pull image → test cheyadam

DevOps → deploy Kubernetes → monitor

Why:

App eppudu same ga run avvali

Auto scaling → traffic ekkuva aithe app slow avvakunda

Rollback → problem vaste previous version ki revert

When:

Code push ayyaka

Nightly/weekly test

Emergency hotfix deploy

Where:
Local dev, CI/CD pipeline, staging, production

How:

Build Docker image → test

Push image → registry

Container Registry – How It Works (Step-by-Step)

Docker Image Tagging

Version define cheyadam → example: app:v1.0

Easy tracking & rollback

Push Image → Registry (Docker Hub / GHCR / AWS ECR)

Central place lo image store chestharu

Teams easy ga pull chesi deploy chesuko galru

Pull Image → Staging / Production Deployment

CI/CD pipeline or manual deployment lo image pull chestharu

Example: docker pull myapp:v1.0

Version Control & Updates

New version deploy ayyaka old version still available

Problem vasthe previous version ki revert easy

Integration with CI/CD

Automated pipeline lo image pull → deploy → verify

Same image eppudu same environment lo run avvali

Tip:

Always maintain tagged, versioned images → clarity & rollback easier

Deploy Kubernetes → verify

QA check → logs → re-deploy if needed
