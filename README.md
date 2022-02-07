OpenStack Volume Storage
========================

[![Actions Status](https://github.com/ome/ansible-role-openstack-volume-storage/workflows/Molecule/badge.svg)](https://github.com/ome/ansible-role-openstack-volume-storage/actions)
[![Ansible Role](https://img.shields.io/ansible/role/41992.svg)](https://galaxy.ansible.com/ome/openstack_volume_storage/)

Create an OpenStack Cinder volume and optionally attach it to an OpenStack
instance.

Note this requires Ansible 2.3 features in `os_volume`.


Role Variables
--------------

Required variables:

- `openstack_volume_size`: Size of the volume in GB
- `openstack_volume_name`: The name of the volume
- `openstack_volume_device`: The device name of the volume in the instance (default: automatically determined by OpenStack)
- `openstack_volume_type`: The type of volume (default: automatically determined by OpenStack)
- `openstack_volume_source`: If defined, the name of an existing volume to use as the source of the volume creation.
- `openstack_volume_vmname`: If defined, the name of an existing instance the volume should be attached to.
- `openstack_volume_wait`: If set to `false`, do not wait for the volume creation to complete, skip the cleanup of the intermediate source volume snapshot if `openstack_volume_source` is defined and skip the volume attachment if `openstack_volume_vmname` is defined (default: true).

Author Information
------------------

ome-devel@lists.openmicroscopy.org.uk
