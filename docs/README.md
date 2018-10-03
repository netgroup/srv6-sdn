Segment Routing (SR) is a form of source routing. The SR architecture works by including a list of _segments_ in the packet headers. A segment can represent a _topological_ instruction (e.g. a node to be crossed) or a _service_ instruction (e.g. an operation to be executed on the packet). 

The Segment Routing architecture can be implemented using MPLS or IPv6 as data plane. We focus on the IPv6 implementation, called _SRv6_, in which the _segments_ are identified by IPv6 addresses. It is natural to consider an SDN based approach to control SR based services in a Service Provider network. A centralized logic can take decisions concerning the Segment Lists that need to be applied to implement the services, then the SDN controller can interact with the edge nodes to enforce the application of such Segment Lists. The possibility for the SDN controller to interact only with edge nodes to setup and reconfigure complex services is extremely appealing from the point of view of the simplicity and efficiency of the solution.

We present hereafter our open source architecture:

![alt text](https://raw.githubusercontent.com/netgroup/srv6-sdn/master/docs/srv6_node.png)

### Scientific papers, technical reports, IETF drafts, Slides

- P.L. Ventre, M.M. Tajiki,, S. Salsano and C. FilsFils, "[SDN Architecture and Southbound APIs for IPv6\\Segment Routing Enabled Wide Area Networks]()", submitted to IEEE Transaction on Network and Service Management (TNSM)

### pyroute2 extensions to support SRv6

[pyroute2](https://github.com/svinota/pyroute2) is a lightweight netlink library written in python. We submitted a patch which adds the support for _SRv6_ basic functionality. We use pyroute2 as "Southbound" of our _SRv6Manager_

Changelog:
- Introduces IPRoute support for SRv6 tunnel
- Adds encap and inline modes
- Supports hmac functionality for SRH
- Initial parsing of human friendly form
- Add seg6_encap_info for RTA_ENCAP mgmt

The extension is available from 0.5 release.

### SRv6 SDN Architecture and Southbound APIs

TODO: Add the links to these repos:

- **srv6-controller** is a collection of modules implementing different functionalities of a SDN controller
- [SRv6 Southbound API evaluation](https://github.com/mohammad59mt/srv6-southbound-api-evaluation) is a library for performance evaluation of the SRv6 Southbound APIs.

### Videos 

TODO: Upload videos and add links

### The Team

- Stefano Salsano
- Pier Luigi Ventre
- Mohammad M. Tajiki