OpenStack Volume Storage
========================

[![Actions Status](https://github.com/ome/ansible-role-openstack-volume-storage/workflows/Molecule/badge.svg)](https://github.com/ome/ansible-role-openstack-volume-storage/actions)
[![Ansible Role](https://img.shields.io/ansible/role/41992.svg)](https://galaxy.ansible.com/ome/openstack_volume_storage/)

Create an OpenStack volume and optionally attach it to an OpenStack instance.

Note this requires Ansible 2.3 features in `os_volume`.


Role Variables
--------------

Required variables:

- `openstack_volume_size`: Size of the volume in GB
- `openstack_volume_name`: The name of the volume
- `openstack_volume_device`: The device name of the volume in the instance (default: automatically determined by OpenStack)
- `openstack_volume_type`: The type of volume (default: automatically determined by OpenStack)
- `openstack_volume_source`: If defined, the name of an existing volume to clone. An intermediate volume snapshot will be created, named after `openstack_volume_name` and suffixed with `-source` and used as the source of the new volume.
- `openstack_volume_vmname`: If defined, the name of an existing instance the volume should be attached to. If `openstack_volume_source` is also specified, the snapshot used for the volume creation is cleaned up, if it exists, before attaching the volume to the instance.


Author Information
------------------

ome-devel@lists.openmicroscopy.org.uk
