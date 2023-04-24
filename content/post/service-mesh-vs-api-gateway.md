---
title:       "Service Mesh and API Gateway's relationship discussion"
subtitle:    ""
description: "The relationship between API Gateway and Service Mesh is a problem I have been thinking about recently, and there have been some discussions with colleagues and friends in the community. This short article clearly summarizes the similarities between the two and their different uses in the micro-service architecture."
date:        2023-01-02 09:00:00
author:      "Eric Ngigi"
image:       "/images/banner/chatgpt-terminal-images-003.jpg"
tags:        ["AI", "OpenSource"]
categories:  ["Tech"]
---

## Service Mesh vs API Gateway

In the previous article about Service Mesh in [](https://medium.com/microservices-in-practice/service-mesh-for-microservices-2953109a3c9a)中,我提到了几个关于ServiceMesh and API Gateway, in this article, I intend to discuss the use of Service Mesh and API Gateway further.

In order to distinguish API Gateway from Service Mesh, let's first look at the key features of each.

## API Gateway: Exposing the service as a managed API to the outside


The main purpose of using API Gateway is to expose micro-services as managed API （ to the external system ）. Therefore, the API or border services we developed at the API Gateway level provide business functions to the outside world.

API/boundary services call downstream combinations or atomic microservices to provide business logic by combining/mixing multiple downstream microservices.

When the API/Edge service calls downstream services, a reliable communication method is required, using a circuit breaker, overtime, load balance/fault transfer and other reliable modes. Therefore, most API Gateway solutions have built these features.

API Gateway also built up support for the following characteristics, including: service discovery, analysis of （ visibility: performance indicators, monitoring, distributed logs, distributed call tracking ） and security.

API Gateway and API manage other components of the ecosystem closely, such as: API market/shop, API release portal.

## Service Mesh: Micro-service network communication infrastructure

Now let's take a look at how Service Mesh is different.

Service Mesh is a network communication infrastructure that can be used to strip the application layer's network communication function from your service code.

Using Service Mesh, you don’t have to implement models for reliable communication such as circuit breaks, overtime, etc. in the service code. Similarly, Service Mesh also provides other functions such as service discovery and service visibility.

![banner-01](/images/banner/chatgpt-terminal-images-001.jpg)
