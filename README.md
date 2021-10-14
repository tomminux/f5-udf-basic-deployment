# ..:: Basic Deployment for the F5 UDF Demo Environment ::..

## Description

When you deploy this blueprint, you will end up in a basic environment you can use to develop DEMOs for customers and parters or to create more complex blueprints for different use cases.

This is using UDF, so you can deploy it close to your location. 

## What is inside?

### Networking

The blueprint is ready to host ADC and App Security DEMOs with the classical three network configurations:

- Management :: 10.1.1.0/24
- External :: 10.1.10.0/24
- Internal :: 10.1.20.0/24


### F5 Gears

From F5, available in this bluprint:

- 1 x BIG-IP to publish infrastructure applications
- 1 x Volterra node, in case you would like to connect this to VoltMesh

### The rest

The infra-server.f5-udf.com box is a Ubuntu Server 20.04 running: 

- ansible
- dnsmasq (please see and manage it from /etc/hosts)
- k3s to host infrastructure applications
- k9s to manage Kubernetes/OCP cluster on the terminal
- Grafana
- Prometheus
- ELK
- Gitlab
- Firefox in a browser

The k3s cluster is running the calico overlay network and is already connected via CIS to the BIG-IP. You can acccess k9s application directly from the "access" tab in the BIG-IP UDF Component.

The linux-jumphost is a Ubuntu 20.04 running the xfce4 Desktop Environment and you can access it from an RDP client using username and password available in the documentaion of that UDF component. 


