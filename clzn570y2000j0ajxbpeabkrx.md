---
title: "some notes of devops things"
datePublished: Fri Aug 09 2024 20:11:15 GMT+0000 (Coordinated Universal Time)
cuid: clzn570y2000j0ajxbpeabkrx
slug: some-notes-of-devops-things

---

what is cloud

> Cloud coputing is the on-demand availability of computer system resources, especially data storage and computing power, without direct active management by the user.

what is devops

devops is a culture or methodology wich uses contanarization,cicd,automation for boost sdlc. and bring together development teams and operational team

linux

\-&gt;91%

\-&gt;open source -operating system , fast, secure,light weight

\-&gt;architecture

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1723230679636/e91bc1f9-305d-4bd2-92ab-c31d15d43c4e.png align="center")

commands

[https://dilipkhunti.hashnode.dev/linux-part-2](https://dilipkhunti.hashnode.dev/linux-part-2)

what is virtualization

process of creating virtual instance of something , like hardware virtualization eg .. how can we create virtual machines by using virtual box and hyperviser (act like layer who creates vm )

what is containerization

we bundles an application’s code with all the files and libraries it needs to run on any infrastructure.

vm vs docker

light weight and fast and uses host operating system

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1723231367690/29a681c4-3172-4fe6-bbdc-a53cf91970ed.png align="center")

kubernates , k8

problems with docker

memory, resouces and short lived container nature and dont have autoscalling and auto healing properties

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1723231830421/2e4ba1ca-073e-4e89-ad1b-653c7544f20f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1723233613030/191b1e4c-fc3b-449e-b490-13dad4db8b58.png align="center")

**Docker registery(docker hub**

**) which hold s many predefined docker images**

it uses on top of docker to manages containers

by providing autohealing and auto scalling

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1723231648017/d8385187-bb41-448a-a4b4-d1809daf6373.png align="center")

inside pod we have multiple containers and we can call this multiples container as a cluster

and multiple pods is also called pods cluster

cicd

continuous integration and continuous deployment

jenkins is a softer to create cicd pipelines

in pipeline we takes code , buils , test ,deploy

we can use github webhooks to automates aur deployment process

iac

infrastucure as a code (terraform)

we write our code and terraform gives us enviroment and whole processed infrastucture

set up virtual machines , storage services , networking

Aws

amazon web services is a cloud provider

and provides 200 + webservices like ec2, s3, dynamodb ,rds

and majorly devided into 3 catogaries

iaas -like azure and ec2

paas -adobe and amazon elasticbean (used for create webapps)

saas -microsoft 365, gmail,whatsap

Monitoring

Grafana

and prometheus

configuration management -- we use software called ansible

we write yaml code for intall updates and do something when our system boots up

what is vpc (virtual private cloud )

virtualally isolated network in which we can set up our resouces

ssh - secured shell

aws

we can connect aws ec2 machines by ssh

iam - identity and accesss management

we have two users in aws account one is root and others are iam users

github and github commands

commit ,push ,pull

load balancing

ecs(elastic container service )

uses to deploy manage and scale contanarized applications

eks (elastic kubernates service)

manages kubernates service which make easy to use kubrnates in aws