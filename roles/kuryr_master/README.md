## OpenStack Kuryr

Install Kuryr components (kuryr-controller, kuryr-cni) on Master and worker
nodes

## Requirements

* Ansible 2.2+
* Centos/ RHEL 7.3+

## Current Kuryr restrictions when used with Openshift

* Openshift Origin only
* OpenShift on OpenStack Newton or newer (only with Trunk ports)

## Key Ansible inventory Kuryr master configuration parameters

* ``openshift_use_kuryr=True``
* ``openshift_use_openshift_sdn=False``
* ``os_sdn_network_plugin_name='cni'``
* ``kuryr_cni_link_interface=eth0``
* ``kuryr_openstack_auth_url=keystone_url``
* ``kuryr_openstack_user_domain_name=Default``
* ``kuryr_openstack_user_project_name=Default``
* ``kuryr_openstack_project_id=project_uuid``
* ``kuryr_openstack_username=kuryr``
* ``kuryr_openstack_password=kuryr_pass``
* ``kuryr_openstack_pod_sg_id=pod_security_group_uuid``
* ``kuryr_openstack_pod_subnet_id=pod_subnet_uuid``
* ``kuryr_openstack_pod_service_id=service_subnet_uuid``
* ``kuryr_openstack_pod_project_id=pod_project_uuid``
* ``kuryr_openstack_worker_nodes_subnet_id=worker_nodes_subnet_uuid``


## Example OpenShift on OpenStack deployment

![Screenshot](roles/kuryr/kuryr_openshift_on_openstack.png)
