## OpenStack Kuryr

Install Kuryr components (kuryr-controller, kuryr-cni) on Master and worker
nodes

## Requirements

* Ansible 2.2+
* Centos/ RHEL 7.3+

## Current Kuryr restrictions when used with Openshift

* Openshift Origin only
* OpenShift on OpenStack Newton or newer (only with Trunk ports)

## Key Ansible inventory configuration parameters

* ``openshift_use_kuryr=True``
* ``openshift_use_openshift_sdn=False``
* ``os_sdn_network_plugin_name='cni'``
* ``kuryr_cni_link_interface=eth0``

## Example OpenShift on OpenStack deployment

![Screenshot](roles/kuryr/kuryr_openshift_on_openstack.png)
