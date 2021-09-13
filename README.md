Openstack Volume Storage
========================

[![Actions Status](https://github.com/ome/ansible-role-openstack-volume-storage/workflows/Molecule/badge.svg)](https://github.com/ome/ansible-role-openstack-volume-storage/actions)
[![Ansible Role](https://img.shields.io/ansible/role/41992.svg)](https://galaxy.ansible.com/ome/openstack_volume_storage/)

Create and attach a volume to an Openstack instance.

Note this requires Ansible 2.3 features in `os_volume`.


Role Variables
--------------

Required variables:

- `openstack_volume_size`: Size of the volume in GB
- `openstack_volume_vmname`: The name of the instance the volume should be attached to
- `openstack_volume_name`: The name of the volume
- `openstack_volume_device`: The device name of the volume in the instance (default: automatically determined by Openstack)
- `openstack_volume_type`: The type of volume


Author Information
------------------

ome-devel@lists.openmicroscopy.org.uk
