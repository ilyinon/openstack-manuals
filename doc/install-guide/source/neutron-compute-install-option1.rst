Networking Option 1: Provider networks
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Install and configure the Networking components on a *compute* node.

Configure the Linux bridge agent
--------------------------------

The Linux bridge agent builds layer-2 (bridging and switching) virtual
networking infrastructure for instances including VXLAN tunnels for private
networks and handles security groups.

Edit the ``/etc/neutron/plugins/ml2/linuxbridge_agent.conf`` file.

#. In the ``[linux_bridge]`` section, map the public virtual network to the
   public physical network interface:

   .. code-block:: ini

      [linux_bridge]
      physical_interface_mappings = public:PUBLIC_INTERFACE_NAME

   Replace ``PUBLIC_INTERFACE_NAME`` with the name of the underlying physical
   public network interface.

#. In the ``[vxlan]`` section, disable VXLAN overlay networks:

   .. code-block:: ini

      [vxlan]
      enable_vxlan = False

#. In the ``[securitygroup]`` section, enable security groups, enable
   :term:`ipset`, and configure the Linux bridge :term:`iptables` firewall
   driver:

   .. code-block:: ini

      [securitygroup]
      ...
      enable_security_group = True
      enable_ipset = True
      firewall_driver = neutron.agent.linux.iptables_firewall.IptablesFirewallDriver

Return to
:ref:`Networking compute node configuration <neutron-compute-compute>`.