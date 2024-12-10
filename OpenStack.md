## OpenStack
OpenStack is an open-source cloud computing platform that enables the deployment and management of infrastructure as a service (IaaS). It provides a suite of interrelated services to manage computing, storage, and networking resources in a data center. OpenStack allows users to create and manage large groups of virtual private servers in a data center.

## Uses of OpenStack
- DevOps
- Data Processing
- Web Hosting
- Public and Private Cloud Deployment

## Pros of OpenStack
- Flexibility: OpenStack can be customized to meet specific needs, making it adaptable for various use cases, from public clouds to private clouds.
- Scalability: Easily scales up or down depending on demand, allowing organizations to handle varying workloads efficiently.
- Interoperability: OpenStack supports a range of operating systems and hypervisors, making it compatible with various infrastructures.

## Installation of OpenStack
Step - 1: Start by installation of the OpenStack snap
```
sudo snap install openstack --channel 2024.1/beta
```

Step - 2: Type the following code for preparation of the machine
```
sunbeam prepare-node-script
```

Step - 3: Deploy the OpenStack cloud using the cluster bootstrap command
```
sunbeam cluster bootstrap --accept-defaults
```

Step - 4: Configure it using this command
```
sunbeam configure --accept-defaults --openrc demo-openrc
```

Step - 5: LauncH a Virtual Machine
```
sunbeam launch ubuntu --name test
```

Step - 6: Connect to the VM over the SSH using the following command
```
Access instance with `ssh -i /home/ubuntu/.config/openstack/sunbeam ubuntu@10.20.20.200`
```
