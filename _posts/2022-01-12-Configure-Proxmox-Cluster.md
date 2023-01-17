---
title: Configuring a Proxmox Cluster
date: 2023-01-12 12:00:00
categories: [Proxmox]
tags: [Linux,Proxmox,Hypervisor,Servers]
---

# Configuring a Proxmox Cluster


A Proxmox cluster is a group of servers that are connected and configured to work together to provide highly available and scalable virtualization services. In this article, we will go through the steps of setting up a Proxmox cluster from scratch.

## Proxmox Cluster Prerequisites

Before we begin, there are a few prerequisites that need to be met:

    Two or more servers with Proxmox VE installed
    A shared storage solution, such as an NFS share or a shared iSCSI LUN
    A network connection between the servers, either through a LAN or a WAN

## Step 1: Configure the Network

The first step in setting up a Proxmox cluster is to ensure that the servers can communicate with each other over the network. This can be done through a LAN or a WAN connection.

If you are using a LAN connection, make sure that the servers are connected to the same network and that they can ping each other.

If you are using a WAN connection, you will need to configure a VPN or a direct connection between the servers.
##Step 2: Configure the Shared Storage

Next, we need to set up a shared storage solution for the cluster. This can be an NFS share or a shared iSCSI LUN.

### To set up an NFS share, follow these steps:

    On the server that will be hosting the NFS share, install the NFS server package.
    Create a directory that will be used as the NFS share.
    Edit the /etc/exports file and add a line for the NFS share, specifying the host and client access.
    Start the NFS server.

### To set up a shared iSCSI LUN, follow these steps:

    On the server that will be hosting the iSCSI LUN, install the iSCSI target software.
    Create a LUN on the server.
    Configure the iSCSI target and LUN on the server.
    On the other servers, install the iSCSI initiator software and connect to the iSCSI target.


## Step 3: Configure the Proxmox Cluster

Now that the network and shared storage are set up, we can move on to configuring the Proxmox cluster.

First, log in to the web interface of one of the servers and go to the "Cluster" tab.

Click on the "Add Node" button and enter the IP address of the other server.

Click on the "Add" button to add the server to the cluster. Repeat this process for any additional servers.

Once all the servers have been added to the cluster, you can create and manage virtual machines and containers using the web interface or the pvecm command-line tool.

## Proxmox Cluster Web Interface
Conclusion

In this article, we went through the steps of setting up a Proxmox cluster, including configuring the network, setting up shared storage, and adding the servers to the cluster. With a Proxmox cluster in place, you can enjoy highly available and scalable virtualization services.