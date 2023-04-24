---
title:       "Talk about the infrastructure in the micro-service architecture: Service Mesh and Istio"
subtitle:    "Service Mesh model and introduction of Istio open source project"
description: "As a architectural model, micro-services divide complex systems into dozens or even hundreds of small services, each of which is responsible for achieving an independent business logic. These small services are easily understood and modified by a small team of software engineers, and bring flexibility in language and framework selection, shorten application development online time, and can be independently reduced and expanded according to different work loads and resource requirements. On the other hand, when the application is split into multiple micro-service processes, the method call within the process becomes a remote call between processes. Introduced the complexity of connecting, managing, and monitoring a large number of services. This article describes how the Service Mesh model responds to these challenges of the micro-service architecture, and Service Mesh’s star open source project Istio."
date:        2023-01-01 09:00:00
author:      "Eric Ngigi"
image:       "images/banner/chatgpt-terminal-images-003.jpg"
tags:        ["AI", "OpenSource"]
categories:  ["Tech"]
published: true
---

## Evolution of micro service architecture
As a architectural model, micro-services divide complex systems into dozens or even hundreds of small services, each of which is responsible for achieving an independent business logic. These small services are easily understood and modified by a small team of software engineers, and bring flexibility in language and framework selection, shorten application development online time, and can be independently reduced and expanded according to different work loads and resource requirements.

On the other hand, when the application is split into multiple micro-service processes, the method call within the process becomes a remote call between processes. Introduced the complexity of connecting, managing and monitoring a large number of services.
